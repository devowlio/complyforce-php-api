# DevOwl\ComplyforceApiClient\OrderReportApi

All URIs are relative to *https://api.complyforce.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**orderReportDelete**](OrderReportApi.md#orderreportdelete) | **DELETE** /order/report | Delete order report
[**orderReportGet**](OrderReportApi.md#orderreportget) | **GET** /order/report | Get order report

# **orderReportDelete**
> orderReportDelete($body)

Delete order report

Deletes the stored compliance report for an order. Authenticate with a vendor API key (`x-api-key`).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\OrderReportApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\OrderReportDeleteRequest(); // \DevOwl\ComplyforceApiClient\Model\OrderReportDeleteRequest | 

try {
    $apiInstance->orderReportDelete($body);
} catch (Exception $e) {
    echo 'Exception when calling OrderReportApi->orderReportDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\OrderReportDeleteRequest**](../Model/OrderReportDeleteRequest.md)|  |

### Return type

void (empty response body)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **orderReportGet**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2001 orderReportGet($orderUuid)

Get order report

Returns the full compliance report and report link for a completed order. Authenticate with a vendor API key (`x-api-key`).

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\OrderReportApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$orderUuid = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 

try {
    $result = $apiInstance->orderReportGet($orderUuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderReportApi->orderReportGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **orderUuid** | [****](../Model/.md)|  |

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

