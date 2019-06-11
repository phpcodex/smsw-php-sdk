# SwaggerClient-php
The SMS Works provides a low-cost, reliable SMS API for developers. Pay only for delivered texts, all failed messages are refunded.

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Build package: io.swagger.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), add the following to `composer.json`:

```
{
  "repositories": [
    {
      "type": "git",
      "url": "https://github.com/phpcodex/smsw-php-sdk.git"
    }
  ],
  "require": {
      "phpcodex/smsw-php-sdk": "^1.0.0"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/SwaggerClient-php/vendor/autoload.php');
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

$apiInstance = new Swagger\Client\Api\AuthApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$customerid = "customerid_example"; // string | The Customer ID

try {
    $result = $apiInstance->keySecret($customerid);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AuthApi->keySecret: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Test calls in Postman

[![Run in Postman](https://run.pstmn.io/button.svg)](https://app.getpostman.com/run-collection/5348de8f62f83cddcee3)


## Documentation for API Endpoints

All URIs are relative to *https://api.thesmsworks.co.uk/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AuthApi* | [**keySecret**](docs/Api/AuthApi.md#keysecret) | **GET** /auth/getApiKey | 
*AuthApi* | [**login**](docs/Api/AuthApi.md#login) | **POST** /auth/token | 
*BatchMessagesApi* | [**cancelScheduledBatchJob**](docs/Api/BatchMessagesApi.md#cancelscheduledbatchjob) | **DELETE** /batches/schedule/{batchid} | 
*BatchMessagesApi* | [**getBatchById**](docs/Api/BatchMessagesApi.md#getbatchbyid) | **GET** /batch/{batchid} | 
*BatchMessagesApi* | [**scheduleBatch**](docs/Api/BatchMessagesApi.md#schedulebatch) | **POST** /batch/schedule | 
*BatchMessagesApi* | [**sendBatch**](docs/Api/BatchMessagesApi.md#sendbatch) | **POST** /batch/send | 
*MessagesApi* | [**cancelScheduledJob**](docs/Api/MessagesApi.md#cancelscheduledjob) | **DELETE** /messages/schedule/{messageid} | 
*MessagesApi* | [**getInboxMessages**](docs/Api/MessagesApi.md#getinboxmessages) | **POST** /messages/inbox | 
*MessagesApi* | [**getMessageById**](docs/Api/MessagesApi.md#getmessagebyid) | **GET** /messages/{messageid} | 
*MessagesApi* | [**getMessages**](docs/Api/MessagesApi.md#getmessages) | **POST** /messages | 
*MessagesApi* | [**scheduleMessage**](docs/Api/MessagesApi.md#schedulemessage) | **POST** /message/schedule | 
*MessagesApi* | [**sendMessage**](docs/Api/MessagesApi.md#sendmessage) | **POST** /message/send | 
*UtilsApi* | [**test**](docs/Api/UtilsApi.md#test) | **GET** /utils/test | 


## Documentation For Models

 - [ApiKeyResponse](docs/Model/ApiKeyResponse.md)
 - [BatchMessage](docs/Model/BatchMessage.md)
 - [BatchMessageResponse](docs/Model/BatchMessageResponse.md)
 - [CancelledMessageResponse](docs/Model/CancelledMessageResponse.md)
 - [ErrorModel](docs/Model/ErrorModel.md)
 - [Login](docs/Model/Login.md)
 - [Message](docs/Model/Message.md)
 - [MessageMetadata](docs/Model/MessageMetadata.md)
 - [MessageResponse](docs/Model/MessageResponse.md)
 - [MessageResponseFailurereason](docs/Model/MessageResponseFailurereason.md)
 - [MessagesResponse](docs/Model/MessagesResponse.md)
 - [MessagesResponseMessages](docs/Model/MessagesResponseMessages.md)
 - [MetaData](docs/Model/MetaData.md)
 - [Query](docs/Model/Query.md)
 - [QueryMetadata](docs/Model/QueryMetadata.md)
 - [ScheduledBatchResponse](docs/Model/ScheduledBatchResponse.md)
 - [ScheduledMessageResponse](docs/Model/ScheduledMessageResponse.md)
 - [SendMessageResponse](docs/Model/SendMessageResponse.md)
 - [TestResponse](docs/Model/TestResponse.md)
 - [TokenResponse](docs/Model/TokenResponse.md)
 - [ExtendedErrorModel](docs/Model/ExtendedErrorModel.md)


## Documentation For Authorization


## JWT

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author




