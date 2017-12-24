# Chabok\Client\PushApi

All URIs are relative to *https://sandbox.push.adpdigital.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pushByQuery**](PushApi.md#pushByQuery) | **POST** /push/byQuery | Push a text message to a segment of devices
[**pushToUsers**](PushApi.md#pushToUsers) | **POST** /push/toUsers | Push multiple text messages to users


# **pushByQuery**
> \Chabok\Client\Model\PushResponse pushByQuery($payload)

Push a text message to a segment of devices

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity,  Get your 'YOUR_API_KEY' from http://sandbox.push.adpdigital.com/front/account/edit 
Chabok\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Get your 'App_ID' from http://sandbox.push.adpdigital.com/front/account/edit 
Chabok\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
// Make Dev mode enable If you want to test your App on Development environment or don't have Chabok premium account
Chabok\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Chabok\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Chabok\Client\Api\PushApi();
$payload = new \Chabok\Client\Model\SegmentPush(); // \Chabok\Client\Model\SegmentPush | 

try {
    $result = $api_instance->pushByQuery($payload);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PushApi->pushByQuery: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **payload** | [**\Chabok\Client\Model\SegmentPush**](../Model/SegmentPush.md)|  |

### Return type

[**\Chabok\Client\Model\PushResponse**](../Model/PushResponse.md)

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pushToUsers**
> \Chabok\Client\Model\PushResponse[] pushToUsers($messages)

Push multiple text messages to users

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity,  Get your 'YOUR_API_KEY' from http://sandbox.push.adpdigital.com/front/account/edit 
Chabok\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Get your 'App_ID' from http://sandbox.push.adpdigital.com/front/account/edit 
Chabok\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
// Make Dev mode enable If you want to test your App on Development environment or don't have Chabok premium account
Chabok\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Chabok\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Chabok\Client\Api\PushApi();
$messages = new \Chabok\Client\Model\Push(); // \Chabok\Client\Model\Push | 

try {
    $result = $api_instance->pushToUsers($messages);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling PushApi->pushToUsers: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **messages** | [**\Chabok\Client\Model\Push**](../Model/Push.md)|  |

### Return type

[**\Chabok\Client\Model\PushResponse[]**](../Model/PushResponse.md)

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

