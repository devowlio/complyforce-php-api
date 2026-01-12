# DevOwl\ComplyforceApiClient\VendorBrandChannelPropertyApi

All URIs are relative to *https://api.complyforce.com/1.0.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**vendorBrandChannelPropertiesDelete**](VendorBrandChannelPropertyApi.md#vendorbrandchannelpropertiesdelete) | **DELETE** /vendor/brand/channel/properties | Delete vendor brand channel properties (single or batch)
[**vendorBrandChannelPropertiesPost**](VendorBrandChannelPropertyApi.md#vendorbrandchannelpropertiespost) | **POST** /vendor/brand/channel/properties | Add vendor brand channel properties (single or batch)
[**vendorBrandChannelPropertyPut**](VendorBrandChannelPropertyApi.md#vendorbrandchannelpropertyput) | **PUT** /vendor/brand/channel/property | Update vendor brand channel property

# **vendorBrandChannelPropertiesDelete**
> vendorBrandChannelPropertiesDelete($body)

Delete vendor brand channel properties (single or batch)

If a property does not exist, it will be ignored. Possible properties are:<br /><br />- ScanPriority = <code>priority</code><br />- WebhookUrl = <code>webhookUrl</code><br />- WebhookOrderStatusCreated = <code>webhookOrderStatusCreated</code><br />- WebhookOrderStatusAllUpdates = <code>webhookOrderStatusAllUpdates</code><br />- WebhookOrderStatusProgressInPercent = <code>webhookOrderStatusProgressInPercent</code><br />- WebhookOrderStatusCompleted = <code>webhookOrderStatusCompleted</code><br />- WebhookOrderStatusError = <code>webhookFeatureOrderStatusError</code><br />- ScanFeatureBrowseAgentVisionAi = <code>scanFeatureBrowseAgentVisionAi</code><br />- ScanFeatureInformationObligationAgentLlmAi = <code>scanFeatureInformationObligationAgentLlmAi</code><br />- ScanFeatureConsentComplianceAgent = <code>scanFeatureConsentComplianceAgent</code><br />- ScanFeatureArchivingAgent = <code>scanFeatureArchivingAgent</code>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandChannelPropertyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\ChannelPropertiesBody1(); // \DevOwl\ComplyforceApiClient\Model\ChannelPropertiesBody1 | 

try {
    $apiInstance->vendorBrandChannelPropertiesDelete($body);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandChannelPropertyApi->vendorBrandChannelPropertiesDelete: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\ChannelPropertiesBody1**](../Model/ChannelPropertiesBody1.md)|  | [optional]

### Return type

void (empty response body)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandChannelPropertiesPost**
> \DevOwl\ComplyforceApiClient\Model\InlineResponse2012 vendorBrandChannelPropertiesPost($body)

Add vendor brand channel properties (single or batch)

If a property already exists, it will be ignored.<br /><br />Possible properties are:<br />- ScanPriority = <code>priority</code><br />- WebhookUrl = <code>webhookUrl</code><br />- WebhookOrderStatusCreated = <code>webhookOrderStatusCreated</code><br />- WebhookOrderStatusAllUpdates = <code>webhookOrderStatusAllUpdates</code><br />- WebhookOrderStatusProgressInPercent = <code>webhookOrderStatusProgressInPercent</code><br />- WebhookOrderStatusCompleted = <code>webhookOrderStatusCompleted</code><br />- WebhookOrderStatusError = <code>webhookFeatureOrderStatusError</code><br />- ScanFeatureBrowseAgentVisionAi = <code>scanFeatureBrowseAgentVisionAi</code><br />- ScanFeatureInformationObligationAgentLlmAi = <code>scanFeatureInformationObligationAgentLlmAi</code><br />- ScanFeatureConsentComplianceAgent = <code>scanFeatureConsentComplianceAgent</code><br />- ScanFeatureArchivingAgent = <code>scanFeatureArchivingAgent</code>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandChannelPropertyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\ChannelPropertiesBody(); // \DevOwl\ComplyforceApiClient\Model\ChannelPropertiesBody | 

try {
    $result = $apiInstance->vendorBrandChannelPropertiesPost($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandChannelPropertyApi->vendorBrandChannelPropertiesPost: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\ChannelPropertiesBody**](../Model/ChannelPropertiesBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\InlineResponse2012**](../Model/InlineResponse2012.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **vendorBrandChannelPropertyPut**
> \DevOwl\ComplyforceApiClient\Model\VendorBrandChannelPropertyUpdated vendorBrandChannelPropertyPut($body)

Update vendor brand channel property

Possible properties are:  - ScanPriority = <code>priority</code> - WebhookUrl = <code>webhookUrl</code> - WebhookOrderStatusCreated = <code>webhookOrderStatusCreated</code> - WebhookOrderStatusAllUpdates = <code>webhookOrderStatusAllUpdates</code> - WebhookOrderStatusProgressInPercent = <code>webhookOrderStatusProgressInPercent</code> - WebhookOrderStatusCompleted = <code>webhookOrderStatusCompleted</code> - WebhookOrderStatusError = <code>webhookFeatureOrderStatusError</code> - ScanFeatureBrowseAgentVisionAi = <code>scanFeatureBrowseAgentVisionAi</code> - ScanFeatureInformationObligationAgentLlmAi = <code>scanFeatureInformationObligationAgentLlmAi</code> - ScanFeatureConsentComplianceAgent = <code>scanFeatureConsentComplianceAgent</code> - ScanFeatureArchivingAgent = <code>scanFeatureArchivingAgent</code>

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');
// Configure API key authorization: jwt
$config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKey('authorization', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = DevOwl\ComplyforceApiClient\Configuration::getDefaultConfiguration()->setApiKeyPrefix('authorization', 'Bearer');

$apiInstance = new DevOwl\ComplyforceApiClient\Api\VendorBrandChannelPropertyApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \DevOwl\ComplyforceApiClient\Model\ChannelPropertyBody(); // \DevOwl\ComplyforceApiClient\Model\ChannelPropertyBody | 

try {
    $result = $apiInstance->vendorBrandChannelPropertyPut($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VendorBrandChannelPropertyApi->vendorBrandChannelPropertyPut: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\DevOwl\ComplyforceApiClient\Model\ChannelPropertyBody**](../Model/ChannelPropertyBody.md)|  | [optional]

### Return type

[**\DevOwl\ComplyforceApiClient\Model\VendorBrandChannelPropertyUpdated**](../Model/VendorBrandChannelPropertyUpdated.md)

### Authorization

[jwt](../../README.md#jwt)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

