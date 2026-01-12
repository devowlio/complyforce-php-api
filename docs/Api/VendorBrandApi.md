# DevOwl\ComplyforceApiClient\VendorBrandApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vendorBrandDelete**](VendorBrandApi.md#vendorbranddelete) | **DELETE** /vendor/brand | Delete vendor brand
[**vendorBrandPost**](VendorBrandApi.md#vendorbrandpost) | **POST** /vendor/brand | Create vendor brand
[**vendorBrandPut**](VendorBrandApi.md#vendorbrandput) | **PUT** /vendor/brand | Edit vendor brand
[**vendorBrandsGet**](VendorBrandApi.md#vendorbrandsget) | **GET** /vendor/brands | Get all vendor brands

# **vendorBrandDelete**
> vendorBrandDelete($body)

Delete vendor brand

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorBrandBody2(); // \DevOwl\ComplyforceApiClient\Model\VendorBrandBody2 | 

try {
    $apiInstance->vendorBrandDelete($body);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandApi->vendorBrandDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorBrandBody2**](../Model/VendorBrandBody2.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2014 vendorBrandPost($body)

Create vendor brand

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorBrandBody1(); // \DevOwl\ComplyforceApiClient\Model\VendorBrandBody1 | 

try {
    $result = $apiInstance->vendorBrandPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandApi->vendorBrandPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorBrandBody1**](../Model/VendorBrandBody1.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2014**](../Model/InlineResponse2014.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandPut**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2003 vendorBrandPut($body)

Edit vendor brand

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorBrandBody(); // \DevOwl\ComplyforceApiClient\Model\VendorBrandBody | 

try {
    $result = $apiInstance->vendorBrandPut($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandApi->vendorBrandPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorBrandBody**](../Model/VendorBrandBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2003**](../Model/InlineResponse2003.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandsGet**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2004 vendorBrandsGet($vendorUuid)

Get all vendor brands

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$vendorUuid = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 

try {
    $result = $apiInstance->vendorBrandsGet($vendorUuid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandApi->vendorBrandsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **vendorUuid** | [****](../Model/.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2004**](../Model/InlineResponse2004.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

