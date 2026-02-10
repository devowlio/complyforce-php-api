# Complyforce PHP SDK

<img align="right" src="https://assets.devowl.io/git/complyforce/logo-full-black.png" alt="Complyforce logo" height="90" />

Complyforce is an AI-assisted website compliance auditing service that identifies services, cookies, and data processing, and checks them against your consent setup for GDPR/ePrivacy (and related national) compliance issues. It generates legally evaluable compliance reports (including machine-readable output) that can be triggered and accessed via an API for integration into your product.

The Complyforce PHP SDK provides seamless integration with the Complyforce API. This library is designed to simplify API interactions and provide tools for efficient implementation.

Detailed API documentation is available at [complyforce.com/api/docs](http://complyforce.com/api/docs).

## Requirements

- PHP 7.4+ or 8.x
- Extensions: `curl`, `json`, `mbstring`

## Installation

```sh
composer require complyforce/api
```

## Usage

### Configuration

Set up the SDK with your Complyforce API key. You can [generate an API key](https://vendor.complyforce.com/api-keys) in the Complyforce Vendor Dashboard.

```php
use DevOwl\ComplyforceApiClient\Api\VendorAPIKeyApi;
use DevOwl\ComplyforceApiClient\Configuration;
use GuzzleHttp\Client;

$apiKey = "your_api_key_here";

$config = new Configuration();
$config->setApiKey("x-api-key", $apiKey);

$client = new Client();
$vendorApi = new VendorAPIKeyApi($client, $config);
```

### Private deployments

If you are a large scale enterprise customer using a private Complyforce deployment, set an explicit base URL. The major version of this SDK package mirrors the API version. Make sure you use the correct SDK version for the compatible API version.

```php
$config->setHost("https://your-instance.complyforce.com/v1");
```

### Response handling

All API methods return model instances on success and throw `ApiException` on non-2xx responses or network errors.

```php
use DevOwl\ComplyforceApiClient\ApiException;

try {
    $result = $vendorApi->vendorApiKeyValidateGet();
    echo $result?->getVendorName() . PHP_EOL;
} catch (ApiException $e) {
    // Access response body or headers for error details
    $body = $e->getResponseBody();
    $headers = $e->getResponseHeaders();
}
```

### Async and raw HTTP info

Each endpoint also provides:

- `*Async()` methods that return a Guzzle promise.
- `*WithHttpInfo()` methods that return `[$data, $statusCode, $headers]`.

```php
[$data, $status, $headers] = $vendorApi->vendorApiKeyValidateGetWithHttpInfo();
```

## API Methods

Each method below maps directly to an API endpoint. For detailed payloads, see the [Complyforce API docs](http://complyforce.com/api/docs).

### vendorApiKeyValidateGet()

Validates the API key and returns the vendor name if authorized.

```php
$apiKeyValidate = $vendorApi->vendorApiKeyValidateGet();
if ($apiKeyValidate && $apiKeyValidate->getVendorName()) {
    echo "Authenticated as " . $apiKeyValidate->getVendorName() . PHP_EOL;
} else {
    echo "Authentication failed" . PHP_EOL;
}
```

### orderPost()

Accepts an order for a website scan with one, several, all, or the most relevant subpages. You can specify scan type, requested URLs, and the channel UUID. You can create a channel in _Brand & Channel > [Name of brand] > Create channel_ in the [Complyforce Vendor Dashboard](https://vendor.complyforce.com/).

**Scan types (details in the [API docs](https://complyforce.com/api/docs#tag/order/GET/order))**
| scanType | What it does | When to use |
| --- | --- | --- |
| `single` | Scans one specific page. | You need a specific or fast overview of data protection issues. |
| `multiple` | Scans at least two specific pages. | You want targeted coverage of important known pages and processes (e.g. product page, checkout, company profile). |
| `mostRelevant` | Finds and scans up to 10-15 representative subpages. | You need an analysis that can uncover most problems. |
| `all` | Scans all pages found via the sitemap. | You need a comprehensive data protection analysis of the entire website. |

```php
use DevOwl\ComplyforceApiClient\Api\OrderApi;
use DevOwl\ComplyforceApiClient\Model\OrderBody;
use DevOwl\ComplyforceApiClient\Model\OrderCreate;
use DevOwl\ComplyforceApiClient\Model\OrderCreateChannel;

$channelUuid = "your-channel-uuid";

$orderApi = new OrderApi($client, $config);

$orderCreate = new OrderCreate();
$orderCreate->setScanType("single");
$orderCreate->setScanUrlsRequested(["https://example.com"]);

$channel = new OrderCreateChannel();
$channel->setUuid($channelUuid);
$orderCreate->setChannel($channel);

$orderBody = new OrderBody();
$orderBody->setOrder($orderCreate);

$postedOrder = $orderApi->orderPost($orderBody);
echo "Order created " . $postedOrder->getOrder()?->getUuid() . PHP_EOL;
```

### orderGet()

Retrieves order data, current status and status updates, as well as report link and summary for completed orders.

```php
$orderUuid = "your-order-uuid";

$readOrder = $orderApi->orderGet($orderUuid, "true", "false");
print_r($readOrder->getOrder());
```

### orderProgressGet()

Fetches scan progress of the order as a percentage.

You can also receive the order progress by a webhook. Configure the webhook at _Brand & Channel > [Name of brand] > [Name of channel] > Edit > Webhooks_ in the [Complyforce Vendor Dashboard](https://vendor.complyforce.com/).

```php
$orderUuid = "your-order-uuid";

$readOrderProgress = $orderApi->orderProgressGet($orderUuid);
print_r($readOrderProgress);
```

### orderReportGet()

Retrieves full report data and report link for completed orders.

```php
use DevOwl\ComplyforceApiClient\Api\OrderReportApi;

$orderUuid = "your-order-uuid";

$orderReportApi = new OrderReportApi($client, $config);

try {
    $readOrderReport = $orderReportApi->orderReportGet($orderUuid);
    print_r($readOrderReport);
} catch (ApiException $e) {
    $errors = $e->getResponseBody();
    if (is_array($errors) && ($errors[0]["code"] ?? null) === "OrderNotCompletedOrCompletedPartially") {
        echo "Order not completed yet" . PHP_EOL;
    } else {
        throw $e;
    }
}
```

### orderReportDelete()

Deletes an existing order report prior to its expiry date.

```php
use DevOwl\ComplyforceApiClient\Model\OrderReportDeleteRequest;
use DevOwl\ComplyforceApiClient\Model\OrderReportDeleteRequestOrder;

$deleteOrder = new OrderReportDeleteRequestOrder();
$deleteOrder->setUuid($orderUuid);

$deleteRequest = new OrderReportDeleteRequest();
$deleteRequest->setOrder($deleteOrder);

$orderReportApi->orderReportDelete($deleteRequest);
echo "Order report deleted" . PHP_EOL;
```

## Support

Need integration support? Our developers can build an individual solution with you. [Contact our support team](https://vendor.complyforce.com/documentation) via the Complyforce Vendor Dashboard!
