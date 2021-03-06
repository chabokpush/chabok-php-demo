# Chabok\Client\VerificationApi

All URIs are relative to *https://sandbox.push.adpdigital.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**verificationRequestCodeGet**](VerificationApi.md#verificationRequestCodeGet) | **GET** /verification/requestCode/{userId} | Request a verification code to be sent to a user
[**verificationVerifyGetVerificationVerifyCodeuserIdcode**](VerificationApi.md#verificationVerifyGetVerificationVerifyCodeuserIdcode) | **GET** /verification/verifyCode/{userId}/{code} | Verify user&#39;s verification code


# **verificationRequestCodeGet**
> \Chabok\Client\Model\VerificationStatus verificationRequestCodeGet($user_id)

Request a verification code to be sent to a user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Chabok\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
Chabok\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
Chabok\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Chabok\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Chabok\Client\Api\VerificationApi();
$user_id = "user_id_example"; // string | Should be a 98 starting mobile number in case of SMS

try {
    $result = $api_instance->verificationRequestCodeGet($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VerificationApi->verificationRequestCodeGet: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**| Should be a 98 starting mobile number in case of SMS |

### Return type

[**\Chabok\Client\Model\VerificationStatus**](../Model/VerificationStatus.md)

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **verificationVerifyGetVerificationVerifyCodeuserIdcode**
> \Chabok\Client\Model\VerificationStatus verificationVerifyGetVerificationVerifyCodeuserIdcode($user_id, $code)

Verify user's verification code

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

$api_instance = new Chabok\Client\Api\VerificationApi();
$user_id = "user_id_example"; // string | The same userId passed to requestCode before
$code = "code_example"; // string | User's provided verification code

try {
    $result = $api_instance->verificationVerifyGetVerificationVerifyCodeuserIdcode($user_id, $code);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VerificationApi->verificationVerifyGetVerificationVerifyCodeuserIdcode: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**| The same userId passed to requestCode before |
 **code** | **string**| User&#39;s provided verification code |

### Return type

[**\Chabok\Client\Model\VerificationStatus**](../Model/VerificationStatus.md)

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

