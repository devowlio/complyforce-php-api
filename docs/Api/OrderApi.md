# DevOwl\ComplyforceApiClient\OrderApi

All URIs are relative to *https://api.complyforce.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**orderGet**](OrderApi.md#orderget) | **GET** /order | Get order
[**orderPost**](OrderApi.md#orderpost) | **POST** /order | Create order
[**ordersGet**](OrderApi.md#ordersget) | **GET** /orders | Get orders overview

# **orderGet**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse200 orderGet($orderUuid, $statusUpdates, $report)

Get order

Retrieve order data, current status and status updates, as well as report link and summary for completed orders.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$orderUuid = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 
$statusUpdates = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 
$report = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 

try {
    $result = $apiInstance->orderGet($orderUuid, $statusUpdates, $report);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderUuid** | [****](../Model/.md)|  |
 **statusUpdates** | [****](../Model/.md)|  | [optional] [default to false]
 **report** | [****](../Model/.md)|  | [optional] [default to true]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **orderPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse201 orderPost($body)

Create order

Accepting an order for a website scan with one, several, all, or the most relevant subpages.  #### Scan types (with examples) <details> <summary>Single page scan</summary> <p>Scans a single page of one website. Provide specific information about this page or a rough overview if the website's front page is scanned.</p>  **Request** ```json {   \"order\": {     \"scanType\": \"single\",     \"scanUrlsRequested\": [       \"https://shop.example.com/login\"     ],     \"channel\": {       \"uuid\": \"b5c03f6a-8fa8-4c24-8ec8-2d0f3388f4f1\"     }   } } ```  **Response** ```json {   \"order\": {     \"uuid\": \"d5c0c97f-4f80-4a27-8c1c-0e5a4d4ad00\",     \"scanType\": \"single\",     \"scanFeaturesRequested\": [       \"browseAgentVisionAi\",       \"orderPreparationUrlsEnrichment\"     ],     \"scanDomain\": \"shop.example.com\",     \"scanUrlsRequested\": [       \"https://shop.example.com/login\"     ],     \"scanPriority\": 50,     \"status\": \"created\",     \"createdAt\": \"2025-01-01T12:00:00.000Z\",     \"statusUpdates\": [       {         \"id\": \"1\",         \"uuid\": \"e1b4dcd4-2e50-4b3d-a6f5-3c13b5c7e20\",         \"status\": \"created\",         \"updatedAt\": \"2025-01-01T12:00:00.000Z\",         \"createdAt\": \"2025-01-01T12:00:00.000Z\"       }     ]   } } ``` </details>  <details> <summary>Multiple pages scan</summary> <p>Scans at least two pages of one website. Allows you to check specific parts of a website.</p>  **Request** ```json {   \"order\": {     \"scanType\": \"multiple\",     \"scanUrlsRequested\": [       \"https://shop.example.com/login\",       \"https://shop.example.com/checkout\"     ],     \"channel\": {       \"uuid\": \"b5c03f6a-8fa8-4c24-8ec8-2d0f3388f4f1\"     }   } } ```  **Response** ```json {   \"order\": {     \"uuid\": \"d5c0c97f-4f81-4a27-8c1c-0e5a4d4ad01\",     \"scanType\": \"multiple\",     \"scanFeaturesRequested\": [       \"browseAgentVisionAi\",       \"informationObligationAgentLlmAi\",       \"orderPreparationUrlsEnrichment\"     ],     \"scanDomain\": \"shop.example.com\",     \"scanUrlsRequested\": [       \"https://shop.example.com/login\",       \"https://shop.example.com/checkout\"     ],     \"scanPriority\": 50,     \"status\": \"created\",     \"createdAt\": \"2025-01-01T12:01:00.000Z\",     \"statusUpdates\": [       {         \"id\": \"2\",         \"uuid\": \"e1b4dcd4-2e51-4b3d-a6f5-3c13b5c7e21\",         \"status\": \"created\",         \"updatedAt\": \"2025-01-01T12:01:00.000Z\",         \"createdAt\": \"2025-01-01T12:01:00.000Z\"       }     ]   } } ``` </details>  <details> <summary>Most relevant pages scan</summary> <p>Finds and scans up to 15 subpages of one website that best represent the functionality of the website. Allows you to get a comprehensive view of the website without having to check all subpages.</p>  **Request** ```json {   \"order\": {     \"scanType\": \"mostRelevant\",     \"scanUrlsRequested\": [       \"newsroom.example.com\"     ],     \"channel\": {       \"uuid\": \"b5c03f6a-8fa8-4c24-8ec8-2d0f3388f4f1\"     }   } } ```  **Response** ```json {   \"order\": {     \"uuid\": \"d5c0c97f-4f82-4a27-8c1c-0e5a4d4ad02\",     \"scanType\": \"mostRelevant\",     \"scanFeaturesRequested\": [       \"informationObligationAgentLlmAi\",       \"orderPreparationUrlsEnrichment\"     ],     \"scanDomain\": \"newsroom.example.com\",     \"scanUrlsRequested\": [],     \"scanPriority\": 50,     \"status\": \"created\",     \"createdAt\": \"2025-01-01T12:02:00.000Z\",     \"statusUpdates\": [       {         \"id\": \"3\",         \"uuid\": \"e1b4dcd4-2e52-4b3d-a6f5-3c13b5c7e22\",         \"status\": \"created\",         \"updatedAt\": \"2025-01-01T12:02:00.000Z\",         \"createdAt\": \"2025-01-01T12:02:00.000Z\"       }     ]   } } ``` </details>  <details> <summary>All pages scan</summary> <p>Finds all pages of one website based on the website's sitemap and scans them. Provides a complete view of the website. Fallbacks to home page menu extraction and search index data (if additional feature is allowed to use), if no sitemap exists.  `scanUrlsLimit` define the maximum pages to scan (default: `500`). You can overwrite the limit to up to `10000`. If the number of pages found is exceeded, the order will be canceled and scanning will not be billed (costs for additional features may still apply).</p>  **Request** ```json {   \"order\": {     \"scanType\": \"all\",     \"scanUrlsRequested\": [       \"careers.example.com\"     ],     \"scanUrlsLimit\": 1000,     \"channel\": {       \"uuid\": \"b5c03f6a-8fa8-4c24-8ec8-2d0f3388f4f1\"     }   } } ```  **Response** ```json {   \"order\": {     \"uuid\": \"d5c0c97f-4f83-4a27-8c1c-0e5a4d4ad03\",     \"scanType\": \"all\",     \"scanFeaturesRequested\": [       \"browseAgentVisionAi\",       \"consentComplianceAgent\",       \"archivingAgent\",       \"orderPreparationUrlsEnrichment\"     ],     \"scanDomain\": \"careers.example.com\",     \"scanUrlsRequested\": [],     \"scanUrlsLimit\": 1000,     \"scanPriority\": 50,     \"status\": \"created\",     \"createdAt\": \"2025-01-01T12:03:00.000Z\",     \"statusUpdates\": [       {         \"id\": \"4\",         \"uuid\": \"e1b4dcd4-2e53-4b3d-a6f5-3c13b5c7e23\",         \"status\": \"created\",         \"updatedAt\": \"2025-01-01T12:03:00.000Z\",         \"createdAt\": \"2025-01-01T12:03:00.000Z\"       }     ]   } } ``` </details>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');// Configure API key authorization: signedMainContract
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\OrderBody(); // \DevOwl\ComplyforceApiClient\Model\OrderBody | 

try {
    $result = $apiInstance->orderPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->orderPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\OrderBody**](../Model/OrderBody.md)|  |

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

[apiKey](../../README.md#apiKey), [signedMainContract](../../README.md#signedMainContract)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **ordersGet**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2002 ordersGet($vendorUuid, $cursor, $limit, $dateFrom, $dateTo, $billingId, $status, $brandUuid, $channelUuid)

Get orders overview

List orders for the authenticated vendor. Supports cursor-based pagination and optional filters by date range, billing, status, brand and channel.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\OrderApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$vendorUuid = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Vendor UUID. User must be assigned to this vendor.
$cursor = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Cursor for pagination. Omit for first page.
$limit = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Max number of orders per page (default and max: 100).
$dateFrom = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Filter orders created on or after the start of this calendar day (YYYY-MM-DD), interpreted in UTC.
$dateTo = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Filter orders created on or before the end of this calendar day (YYYY-MM-DD), interpreted in UTC.
$billingId = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Filter by vendor billing ID (numeric primary key).
$status = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Filter by order status.
$brandUuid = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Filter by vendor brand UUID.
$channelUuid = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Filter by vendor brand channel UUID.

try {
    $result = $apiInstance->ordersGet($vendorUuid, $cursor, $limit, $dateFrom, $dateTo, $billingId, $status, $brandUuid, $channelUuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderApi->ordersGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **vendorUuid** | [****](../Model/.md)| Vendor UUID. User must be assigned to this vendor. |
 **cursor** | [****](../Model/.md)| Cursor for pagination. Omit for first page. | [optional]
 **limit** | [****](../Model/.md)| Max number of orders per page (default and max: 100). | [optional]
 **dateFrom** | [****](../Model/.md)| Filter orders created on or after the start of this calendar day (YYYY-MM-DD), interpreted in UTC. | [optional]
 **dateTo** | [****](../Model/.md)| Filter orders created on or before the end of this calendar day (YYYY-MM-DD), interpreted in UTC. | [optional]
 **billingId** | [****](../Model/.md)| Filter by vendor billing ID (numeric primary key). | [optional]
 **status** | [****](../Model/.md)| Filter by order status. | [optional]
 **brandUuid** | [****](../Model/.md)| Filter by vendor brand UUID. | [optional]
 **channelUuid** | [****](../Model/.md)| Filter by vendor brand channel UUID. | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

