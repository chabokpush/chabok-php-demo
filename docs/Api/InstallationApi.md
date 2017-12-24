# Swagger\Client\InstallationApi

All URIs are relative to *https://sandbox.push.adpdigital.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**installationAddTag**](InstallationApi.md#installationAddTag) | **GET** /installations/addTag/{userId}/{tagName} | Add tag to all devices of a user
[**installationFetchById**](InstallationApi.md#installationFetchById) | **GET** /installations/fetchById/{installationId} | Find device installation data by installationId
[**installationFetchByUserId**](InstallationApi.md#installationFetchByUserId) | **GET** /installations/fetchByUserId/{userId} | Find devices of a specific user
[**installationGroupBySubscription**](InstallationApi.md#installationGroupBySubscription) | **GET** /installations/channels | List of unique channel names
[**installationRemoveTag**](InstallationApi.md#installationRemoveTag) | **GET** /installations/removeTag/{userId}/{tagName} | Remove a tag from devices of a UserId
[**installationTags**](InstallationApi.md#installationTags) | **GET** /installations/tags | List of unique tag names


# **installationAddTag**
> object installationAddTag($user_id, $tag_name)

Add tag to all devices of a user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
Swagger\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
Swagger\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\InstallationApi();
$user_id = "user_id_example"; // string | 
$tag_name = "tag_name_example"; // string | 

try {
    $result = $api_instance->installationAddTag($user_id, $tag_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstallationApi->installationAddTag: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**|  |
 **tag_name** | **string**|  |

### Return type

**object**

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **installationFetchById**
> \Swagger\Client\Model\Installation installationFetchById($installation_id)

Find device installation data by installationId

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
Swagger\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
Swagger\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\InstallationApi();
$installation_id = "installation_id_example"; // string | installationId

try {
    $result = $api_instance->installationFetchById($installation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstallationApi->installationFetchById: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **installation_id** | **string**| installationId |

### Return type

[**\Swagger\Client\Model\Installation**](../Model/Installation.md)

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **installationFetchByUserId**
> \Swagger\Client\Model\Installation[] installationFetchByUserId($user_id)

Find devices of a specific user

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
Swagger\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
Swagger\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\InstallationApi();
$user_id = "user_id_example"; // string | The userId

try {
    $result = $api_instance->installationFetchByUserId($user_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstallationApi->installationFetchByUserId: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**| The userId |

### Return type

[**\Swagger\Client\Model\Installation[]**](../Model/Installation.md)

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **installationGroupBySubscription**
> object[] installationGroupBySubscription()

List of unique channel names

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
Swagger\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
Swagger\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\InstallationApi();

try {
    $result = $api_instance->installationGroupBySubscription();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstallationApi->installationGroupBySubscription: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**object[]**

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **installationRemoveTag**
> object installationRemoveTag($user_id, $tag_name)

Remove a tag from devices of a UserId

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
Swagger\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
Swagger\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\InstallationApi();
$user_id = "user_id_example"; // string | 
$tag_name = "tag_name_example"; // string | 

try {
    $result = $api_instance->installationRemoveTag($user_id, $tag_name);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstallationApi->installationRemoveTag: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **string**|  |
 **tag_name** | **string**|  |

### Return type

**object**

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **installationTags**
> string[] installationTags()

List of unique tag names

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: ApiSecurity
Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('access_token', 'YOUR_API_KEY');
Swagger\Client\Configuration::getDefaultConfiguration()->setAppId('App_ID');
Swagger\Client\Configuration::getDefaultConfiguration()->setDevMode(true);
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('access_token', 'Bearer');

$api_instance = new Swagger\Client\Api\InstallationApi();

try {
    $result = $api_instance->installationTags();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling InstallationApi->installationTags: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters
This endpoint does not need any parameter.

### Return type

**string[]**

### Authorization

[ApiSecurity](../../README.md#ApiSecurity)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

