# Mydex\ApiPdxSdk\SecureMessagesApi



All URIs are relative to https://api.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getSecureMessageConversation()**](SecureMessagesApi.md#getSecureMessageConversation) | **GET** /secure-messages/conversation | Retrieve all secure messages for a given conversation. |
| [**postSecureMessageReceive()**](SecureMessagesApi.md#postSecureMessageReceive) | **POST** /secure-messages/receive | Supports sending a message to the member&#39;s PDS. |
| [**postSecureMessageSend()**](SecureMessagesApi.md#postSecureMessageSend) | **POST** /secure-messages/send | Supports sending a message from the member&#39;s PDS. |


## `getSecureMessageConversation()`

```php
getSecureMessageConversation($connection_token, $uid, $con_id, $conversation_id): \Mydex\ApiPdxSdk\Model\SecureMessageConversationResponse
```

Retrieve all secure messages for a given conversation.

Returns a list of secure messages that form part of a conversation.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\SecureMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$conversation_id = referral-123; // string | The specific ID of the conversation that groups messages together

try {
    $result = $apiInstance->getSecureMessageConversation($connection_token, $uid, $con_id, $conversation_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SecureMessagesApi->getSecureMessageConversation: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **conversation_id** | **string**| The specific ID of the conversation that groups messages together | |

### Return type

[**\Mydex\ApiPdxSdk\Model\SecureMessageConversationResponse**](../Model/SecureMessageConversationResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSecureMessageReceive()`

```php
postSecureMessageReceive($connection_token, $uid, $con_id, $secure_message_receive_request): \Mydex\ApiPdxSdk\Model\CreateResponse
```

Supports sending a message to the member's PDS.

Creates a new received message in the member's PDS.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\SecureMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$secure_message_receive_request = new \Mydex\ApiPdxSdk\Model\SecureMessageReceiveRequest(); // \Mydex\ApiPdxSdk\Model\SecureMessageReceiveRequest

try {
    $result = $apiInstance->postSecureMessageReceive($connection_token, $uid, $con_id, $secure_message_receive_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SecureMessagesApi->postSecureMessageReceive: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **secure_message_receive_request** | [**\Mydex\ApiPdxSdk\Model\SecureMessageReceiveRequest**](../Model/SecureMessageReceiveRequest.md)|  | [optional] |

### Return type

[**\Mydex\ApiPdxSdk\Model\CreateResponse**](../Model/CreateResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSecureMessageSend()`

```php
postSecureMessageSend($connection_token, $uid, $con_id, $secure_message_send_request): \Mydex\ApiPdxSdk\Model\CreateResponse
```

Supports sending a message from the member's PDS.

Creates a new sent message in the member's PDS.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\SecureMessagesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$secure_message_send_request = new \Mydex\ApiPdxSdk\Model\SecureMessageSendRequest(); // \Mydex\ApiPdxSdk\Model\SecureMessageSendRequest

try {
    $result = $apiInstance->postSecureMessageSend($connection_token, $uid, $con_id, $secure_message_send_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling SecureMessagesApi->postSecureMessageSend: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **secure_message_send_request** | [**\Mydex\ApiPdxSdk\Model\SecureMessageSendRequest**](../Model/SecureMessageSendRequest.md)|  | [optional] |

### Return type

[**\Mydex\ApiPdxSdk\Model\CreateResponse**](../Model/CreateResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
