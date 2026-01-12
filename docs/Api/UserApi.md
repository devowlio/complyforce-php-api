# DevOwl\ComplyforceApiClient\UserApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**userPost**](UserApi.md#userpost) | **POST** /user | User Create
[**userPut**](UserApi.md#userput) | **PUT** /user | User Update

# **userPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2011 userPost($body)

User Create

Creates a new user, which must be assigned to at least one vendor

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: superAdmin
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-authentication-super-admin', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-authentication-super-admin', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\UserCreate(); // \DevOwl\ComplyforceApiClient\Model\UserCreate | 

try {
    $result = $apiInstance->userPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\UserCreate**](../Model/UserCreate.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2011**](../Model/InlineResponse2011.md)

### Authorization

[superAdmin](../../README.md#superAdmin)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userPut**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2001 userPut($body)

User Update

Updates user details or vendor assignments

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: superAdmin
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('x-authentication-super-admin', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('x-authentication-super-admin', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\UserUpdate(); // \DevOwl\ComplyforceApiClient\Model\UserUpdate | 

try {
    $result = $apiInstance->userPut($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\UserUpdate**](../Model/UserUpdate.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2001**](../Model/InlineResponse2001.md)

### Authorization

[superAdmin](../../README.md#superAdmin)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

