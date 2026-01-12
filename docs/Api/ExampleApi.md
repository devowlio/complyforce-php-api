# DevOwl\ComplyforceApiClient\ExampleApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**examplePost**](ExampleApi.md#examplepost) | **POST** /example | Create an example entity

# **examplePost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse200 examplePost($body, $xDate, $shouldFail)

Create an example entity

Create an example entity

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: webhook-secret
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('secret', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('secret', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\ExampleApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\ExampleBody(); // \DevOwl\ComplyforceApiClient\Model\ExampleBody | 
$xDate = new \DevOwl\ComplyforceApiClient\Model\null(); //  | An example header
$shouldFail = new \DevOwl\ComplyforceApiClient\Model\null(); //  | Whether to fail the request

try {
    $result = $apiInstance->examplePost($body, $xDate, $shouldFail);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ExampleApi->examplePost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\ExampleBody**](../Model/ExampleBody.md)|  | [optional]
 **xDate** | [****](../Model/.md)| An example header | [optional]
 **shouldFail** | [****](../Model/.md)| Whether to fail the request | [optional] [default to false]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[webhook-secret](../../README.md#webhook-secret)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

