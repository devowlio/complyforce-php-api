# DevOwl\ComplyforceApiClient\VendorBrandChannelApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vendorBrandChannelPut**](VendorBrandChannelApi.md#vendorbrandchannelput) | **PUT** /vendor/brand/channel | Update vendor brand channel
[**vendorBrandChannelsDelete**](VendorBrandChannelApi.md#vendorbrandchannelsdelete) | **DELETE** /vendor/brand/channels | Delete vendor brand channels (single or batch)
[**vendorBrandChannelsPost**](VendorBrandChannelApi.md#vendorbrandchannelspost) | **POST** /vendor/brand/channels | Add vendor brand channels (single or batch)

# **vendorBrandChannelPut**
> \DevOwl\ComplyforceApiClient\Model\VendorBrandChannelUpdated vendorBrandChannelPut($body)

Update vendor brand channel

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\BrandChannelBody(); // \DevOwl\ComplyforceApiClient\Model\BrandChannelBody | 

try {
    $result = $apiInstance->vendorBrandChannelPut($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandChannelApi->vendorBrandChannelPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\BrandChannelBody**](../Model/BrandChannelBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\VendorBrandChannelUpdated**](../Model/VendorBrandChannelUpdated.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandChannelsDelete**
> vendorBrandChannelsDelete($body)

Delete vendor brand channels (single or batch)

If the channel does not exist, it will be ignored.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\BrandChannelsBody1(); // \DevOwl\ComplyforceApiClient\Model\BrandChannelsBody1 | 

try {
    $apiInstance->vendorBrandChannelsDelete($body);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandChannelApi->vendorBrandChannelsDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\BrandChannelsBody1**](../Model/BrandChannelsBody1.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandChannelsPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2013 vendorBrandChannelsPost($body)

Add vendor brand channels (single or batch)

If the channel already exists, it will be ignored.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandChannelApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\BrandChannelsBody(); // \DevOwl\ComplyforceApiClient\Model\BrandChannelsBody | 

try {
    $result = $apiInstance->vendorBrandChannelsPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandChannelApi->vendorBrandChannelsPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\BrandChannelsBody**](../Model/BrandChannelsBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2013**](../Model/InlineResponse2013.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

