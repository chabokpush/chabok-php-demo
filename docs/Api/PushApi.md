# Swagger\Client\PushApi

All URIs are relative to *https://sandbox.push.adpdigital.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**pushByQuery**](PushApi.md#pushByQuery) | **POST** /push/byQuery | Push a text message to a segment of devices
[**pushToUsers**](PushApi.md#pushToUsers) | **POST** /push/toUsers | Push multiple text messages to users


# **pushByQuery**
> string[] pushByQuery($payload)

Push a text message to a segment of devices

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\PushApi();
$payload = new \Swagger\Client\Model\Push(); // \Swagger\Client\Model\Push | 

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
 **payload** | [**\Swagger\Client\Model\Push**](../Model/Push.md)|  |

### Return type

**string[]**

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **pushToUsers**
> \Swagger\Client\Model\InlineResponse200 pushToUsers($messages)

Push multiple text messages to users

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\PushApi();
$messages = new \Swagger\Client\Model\Push(); // \Swagger\Client\Model\Push | 

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
 **messages** | [**\Swagger\Client\Model\Push**](../Model/Push.md)|  |

### Return type

[**\Swagger\Client\Model\InlineResponse200**](../Model/InlineResponse200.md)

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

