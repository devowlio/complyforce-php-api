# DevOwl\ComplyforceApiClient\VendorAPIKeyApi

All URIs are relative to *https://api.complyforce.com/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vendorApiKeyValidateGet**](VendorAPIKeyApi.md#vendorapikeyvalidateget) | **GET** /vendor/api-key/validate | Validate API key authorization

# **vendorApiKeyValidateGet**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2002 vendorApiKeyValidateGet()

Validate API key authorization

Checks whether the provided API key is valid and, if successful, returns the vendor name linked to that key.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: apiKey
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-api-key', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-api-key', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorAPIKeyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->vendorApiKeyValidateGet();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorAPIKeyApi->vendorApiKeyValidateGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

