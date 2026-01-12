# DevOwl\ComplyforceApiClient\VendorBrandPropertyApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vendorBrandPropertiesDelete**](VendorBrandPropertyApi.md#vendorbrandpropertiesdelete) | **DELETE** /vendor/brand/properties | Delete vendor brand properties (single or batch)
[**vendorBrandPropertiesPost**](VendorBrandPropertyApi.md#vendorbrandpropertiespost) | **POST** /vendor/brand/properties | Add vendor brand properties (single or batch)
[**vendorBrandPropertyPut**](VendorBrandPropertyApi.md#vendorbrandpropertyput) | **PUT** /vendor/brand/property | Update vendor brand property

# **vendorBrandPropertiesDelete**
> vendorBrandPropertiesDelete($body)

Delete vendor brand properties (single or batch)

If the property does not exist, it will be ignored.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandPropertyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\BrandPropertiesBody1(); // \DevOwl\ComplyforceApiClient\Model\BrandPropertiesBody1 | 

try {
    $apiInstance->vendorBrandPropertiesDelete($body);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandPropertyApi->vendorBrandPropertiesDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\BrandPropertiesBody1**](../Model/BrandPropertiesBody1.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandPropertiesPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2015 vendorBrandPropertiesPost($body)

Add vendor brand properties (single or batch)

If the property already exists, it will be ignored.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandPropertyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\BrandPropertiesBody(); // \DevOwl\ComplyforceApiClient\Model\BrandPropertiesBody | 

try {
    $result = $apiInstance->vendorBrandPropertiesPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandPropertyApi->vendorBrandPropertiesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\BrandPropertiesBody**](../Model/BrandPropertiesBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2015**](../Model/InlineResponse2015.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandPropertyPut**
> \DevOwl\ComplyforceApiClient\Model\BrandPropertyBody vendorBrandPropertyPut($body)

Update vendor brand property

Possible properties are:<br /><br />- BrandName = <code>brandName</code><br />- ColorPrimary = <code>colorPrimary</code><br />- Whitelabel = <code>whitelabel</code><br />- RealCookieBannerAds = <code>realCookieBannerAds</code>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandPropertyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\BrandPropertyBody(); // \DevOwl\ComplyforceApiClient\Model\BrandPropertyBody | 

try {
    $result = $apiInstance->vendorBrandPropertyPut($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandPropertyApi->vendorBrandPropertyPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\BrandPropertyBody**](../Model/BrandPropertyBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\BrandPropertyBody**](../Model/BrandPropertyBody.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

