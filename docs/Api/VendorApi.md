# DevOwl\ComplyforceApiClient\VendorApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vendorContractPost**](VendorApi.md#vendorcontractpost) | **POST** /vendor/contract | Update vendor contract
[**vendorInvoiceAddressPost**](VendorApi.md#vendorinvoiceaddresspost) | **POST** /vendor/invoice-address | Update invoice address
[**vendorPost**](VendorApi.md#vendorpost) | **POST** /vendor | Create a new vendor
[**vendorPut**](VendorApi.md#vendorput) | **PUT** /vendor | Update a vendor
[**vendorsGet**](VendorApi.md#vendorsget) | **GET** /vendors | Get all vendors

# **vendorContractPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2016 vendorContractPost($body)

Update vendor contract

Contract is immutable and every time its updated, a new contract is created.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: superAdmin
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-authentication-super-admin', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-authentication-super-admin', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorContractBody(); // \DevOwl\ComplyforceApiClient\Model\VendorContractBody | 

try {
    $result = $apiInstance->vendorContractPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorApi->vendorContractPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorContractBody**](../Model/VendorContractBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2016**](../Model/InlineResponse2016.md)

### Authorization

[superAdmin](../../README.md#superAdmin)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorInvoiceAddressPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2017 vendorInvoiceAddressPost($body)

Update invoice address

Invoice address is immutable and every time its updated, a new invoice address is created.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorInvoiceaddressBody(); // \DevOwl\ComplyforceApiClient\Model\VendorInvoiceaddressBody | 

try {
    $result = $apiInstance->vendorInvoiceAddressPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorApi->vendorInvoiceAddressPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorInvoiceaddressBody**](../Model/VendorInvoiceaddressBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2017**](../Model/InlineResponse2017.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2018 vendorPost($body)

Create a new vendor

Creates a new vendor with an invoice address and contract with contract pricing components.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: superAdmin
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-authentication-super-admin', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-authentication-super-admin', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorBody1(); // \DevOwl\ComplyforceApiClient\Model\VendorBody1 | 

try {
    $result = $apiInstance->vendorPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorApi->vendorPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorBody1**](../Model/VendorBody1.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2018**](../Model/InlineResponse2018.md)

### Authorization

[superAdmin](../../README.md#superAdmin)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorPut**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2005 vendorPut($body)

Update a vendor

Updates editable properties of vendor only. Editable properties are alias, status and statusBlockingReason.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: superAdmin
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-authentication-super-admin', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-authentication-super-admin', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\VendorBody(); // \DevOwl\ComplyforceApiClient\Model\VendorBody | 

try {
    $result = $apiInstance->vendorPut($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorApi->vendorPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\VendorBody**](../Model/VendorBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2005**](../Model/InlineResponse2005.md)

### Authorization

[superAdmin](../../README.md#superAdmin)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorsGet**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2006 vendorsGet($body)

Get all vendors

Returns a list of all vendors assigned to the current logged in user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\null(); //  | 

try {
    $result = $apiInstance->vendorsGet($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorApi->vendorsGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [****](../Model/.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2006**](../Model/InlineResponse2006.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

