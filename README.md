# Chabok API for PHP
Integrate your app with Chabok messaging & push api seamlessly

## Upgrade Notes to v1.1.0 (MUST READ)
* Change all `Swagger` prefix to `Chabok`
* You should set 'App_ID' on Chabok Configuration to connect in the right way


## Requirements

PHP 5.4.0 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/chabokpush/chabok-php-demo/.git"
    }
  ],
  "require": {
    "/": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/chabok-php-demo/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

$api_instance = new Chabok\Client\Api\InstallationApi();
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

## Documentation for API Endpoints

All URIs are relative to *https://sandbox.push.adpdigital.com/api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*InstallationApi* | [**installationAddTag**](docs/Api/InstallationApi.md#installationaddtag) | **GET** /installations/addTag/{userId}/{tagName} | Add tag to all devices of a user
*InstallationApi* | [**installationFetchById**](docs/Api/InstallationApi.md#installationfetchbyid) | **GET** /installations/fetchById/{installationId} | Find device installation data by installationId
*InstallationApi* | [**installationFetchByUserId**](docs/Api/InstallationApi.md#installationfetchbyuserid) | **GET** /installations/fetchByUserId/{userId} | Find devices of a specific user
*InstallationApi* | [**installationGroupBySubscription**](docs/Api/InstallationApi.md#installationgroupbysubscription) | **GET** /installations/channels | List of unique channel names
*InstallationApi* | [**installationRemoveTag**](docs/Api/InstallationApi.md#installationremovetag) | **GET** /installations/removeTag/{userId}/{tagName} | Remove a tag from devices of a UserId
*InstallationApi* | [**installationTags**](docs/Api/InstallationApi.md#installationtags) | **GET** /installations/tags | List of unique tag names
*MessageApi* | [**messageFetchById**](docs/Api/MessageApi.md#messagefetchbyid) | **GET** /messages/fetchById/{messageId} | Fetch a pushed message by id
*PushApi* | [**pushByQuery**](docs/Api/PushApi.md#pushbyquery) | **POST** /push/byQuery | Push a text message to a segment of devices
*PushApi* | [**pushToUsers**](docs/Api/PushApi.md#pushtousers) | **POST** /push/toUsers | Push multiple text messages to users
*VerificationApi* | [**verificationRequestCodeGet**](docs/Api/VerificationApi.md#verificationrequestcodeget) | **GET** /verification/requestCode/{userId} | Request a verification code to be sent to a user
*VerificationApi* | [**verificationVerifyGetVerificationVerifyCodeuserIdcode**](docs/Api/VerificationApi.md#verificationverifygetverificationverifycodeuseridcode) | **GET** /verification/verifyCode/{userId}/{code} | Verify user&#39;s verification code


## Documentation For Models

 - [Installation](docs/Model/Installation.md)
 - [Message](docs/Model/Message.md)
 - [ObjectID](docs/Model/ObjectID.md)
 - [Push](docs/Model/Push.md)
 - [PushResponse](docs/Model/PushResponse.md)
 - [SegmentPush](docs/Model/SegmentPush.md)
 - [Verification](docs/Model/Verification.md)
 - [VerificationStatus](docs/Model/VerificationStatus.md)
 - [XAny](docs/Model/XAny.md)


## Documentation For Authorization


## ApiSecurity

- **Type**: API key
- **API key parameter name**: access_token
- **Location**: URL query string

