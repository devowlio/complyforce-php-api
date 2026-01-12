# DevOwl\ComplyforceApiClient\VendorAPIKeyApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vendorApiKeyDelete**](VendorAPIKeyApi.md#vendorapikeydelete) | **DELETE** /vendor/api-key | Delete API key
[**vendorApiKeyPost**](VendorAPIKeyApi.md#vendorapikeypost) | **POST** /vendor/api-key | Create API key
[**vendorApiKeysGet**](VendorAPIKeyApi.md#vendorapikeysget) | **GET** /vendor/api-keys | Get API keys for a vendor

# **vendorApiKeyDelete**
> vendorApiKeyDelete($body)

Delete API key

Delete API key by revoking it

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorAPIKeyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorApikeyBody1(); // \DevOwl\ComplyforceApiClient\Model\VendorApikeyBody1 | 

try {
    $apiInstance->vendorApiKeyDelete($body);
} catch (Exception $e) {
    echo 'Exception when calling VendorAPIKeyApi->vendorApiKeyDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorApikeyBody1**](../Model/VendorApikeyBody1.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorApiKeyPost**
> \DevOwl\ComplyforceApiClient\Model\VendorApiKey vendorApiKeyPost($body)

Create API key

Creates a random API key for logged in user to given vendor.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorAPIKeyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorApikeyBody(); // \DevOwl\ComplyforceApiClient\Model\VendorApikeyBody | 

try {
    $result = $apiInstance->vendorApiKeyPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorAPIKeyApi->vendorApiKeyPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorApikeyBody**](../Model/VendorApikeyBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\VendorApiKey**](../Model/VendorApiKey.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorApiKeysGet**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2002 vendorApiKeysGet($vendorUuid, $showAll)

Get API keys for a vendor

Gets all API keys for specific vendor by using vendor uuid and optionally showAll as true to show all keys. If showAll is true, the response will include all keys, including revoked ones.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorAPIKeyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$vendorUuid = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 
$showAll = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 

try {
    $result = $apiInstance->vendorApiKeysGet($vendorUuid, $showAll);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorAPIKeyApi->vendorApiKeysGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **vendorUuid** | [****](../Model/.md)|  |
 **showAll** | [****](../Model/.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2002**](../Model/InlineResponse2002.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

