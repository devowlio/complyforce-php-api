# DevOwl\ComplyforceApiClient\UserSessionApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**userMagicLinkPost**](UserSessionApi.md#usermagiclinkpost) | **POST** /user/magic-link | User Session MagicLink request
[**userSessionDelete**](UserSessionApi.md#usersessiondelete) | **DELETE** /user/session | User Session delete
[**userSessionPatch**](UserSessionApi.md#usersessionpatch) | **PATCH** /user/session | User Session renew
[**userSessionPost**](UserSessionApi.md#usersessionpost) | **POST** /user/session | User Session create

# **userMagicLinkPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse201 userMagicLinkPost($body)

User Session MagicLink request

Users can request a magic link (passwordless authentication) to create a user session. If a user wants to sign in without a password, a magic link is sent to his/her email address.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\UserSessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \DevOwl\ComplyforceApiClient\Model\UserMagiclinkBody(); // \DevOwl\ComplyforceApiClient\Model\UserMagiclinkBody | 

try {
    $result = $apiInstance->userMagicLinkPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserSessionApi->userMagicLinkPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\UserMagiclinkBody**](../Model/UserMagiclinkBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse201**](../Model/InlineResponse201.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userSessionDelete**
> userSessionDelete()

User Session delete

Session will be marked as revoked on server side and JWT becomes invalid.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\UserSessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $apiInstance->userSessionDelete();
} catch (Exception $e) {
    echo 'Exception when calling UserSessionApi->userSessionDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userSessionPatch**
> \DevOwl\ComplyforceApiClient\Model\UserSessionRenewed userSessionPatch()

User Session renew

Expects authentication with a still valid JWT to renew the session. As result, a new JWT will be issued.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\UserSessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->userSessionPatch();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserSessionApi->userSessionPatch: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**\DevOwl\ComplyforceApiClient\Model\UserSessionRenewed**](../Model/UserSessionRenewed.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **userSessionPost**
> \DevOwl\ComplyforceApiClient\Model\UserSessionCreated userSessionPost($body)

User Session create

After [requesting a magic link](##tag/user/post/user/magic-link), user can redeem token to create a session. Session management with JWTs for users. Sessions are time limited and need to be renewed to keep user signed in.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\UserSessionApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$body = new \DevOwl\ComplyforceApiClient\Model\UserSessionBody(); // \DevOwl\ComplyforceApiClient\Model\UserSessionBody | 

try {
    $result = $apiInstance->userSessionPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserSessionApi->userSessionPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\UserSessionBody**](../Model/UserSessionBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\UserSessionCreated**](../Model/UserSessionCreated.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

