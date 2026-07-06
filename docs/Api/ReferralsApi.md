# Mydex\ApiPdxSdk\ReferralsApi

Operations related to referrals

All URIs are relative to https://api.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getAllReferrals()**](ReferralsApi.md#getAllReferrals) | **GET** /referrals/read-all | Retrieve rall referrals for a given member. |
| [**getSingleReferral()**](ReferralsApi.md#getSingleReferral) | **GET** /referrals/read-single | Retrieve a single referral by id for a given member. |
| [**postSelfReferral()**](ReferralsApi.md#postSelfReferral) | **POST** /referrals/self-refer | Supports self-referral. |
| [**updateReferralStatus()**](ReferralsApi.md#updateReferralStatus) | **PUT** /referrals/update-status | Supports updating the status of a referral. |


## `getAllReferrals()`

```php
getAllReferrals($connection_token, $uid, $con_id): \Mydex\ApiPdxSdk\Model\ReferralListResponse
```

Retrieve rall referrals for a given member.

Returns a list of referrals.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\ReferralsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.

try {
    $result = $apiInstance->getAllReferrals($connection_token, $uid, $con_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferralsApi->getAllReferrals: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |

### Return type

[**\Mydex\ApiPdxSdk\Model\ReferralListResponse**](../Model/ReferralListResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getSingleReferral()`

```php
getSingleReferral($connection_token, $uid, $con_id, $id): \Mydex\ApiPdxSdk\Model\ReferralSingleResponse
```

Retrieve a single referral by id for a given member.

Returns the requested referral.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\ReferralsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$id = 1234; // string | The record id requested.

try {
    $result = $apiInstance->getSingleReferral($connection_token, $uid, $con_id, $id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferralsApi->getSingleReferral: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **id** | **string**| The record id requested. | |

### Return type

[**\Mydex\ApiPdxSdk\Model\ReferralSingleResponse**](../Model/ReferralSingleResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postSelfReferral()`

```php
postSelfReferral($connection_token, $uid, $con_id, $self_referral_request_body): \Mydex\ApiPdxSdk\Model\CreateResponse
```

Supports self-referral.

Creates a new referral of type 'Self Referred' in the member's PDS.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\ReferralsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$self_referral_request_body = new \Mydex\ApiPdxSdk\Model\SelfReferralRequestBody(); // \Mydex\ApiPdxSdk\Model\SelfReferralRequestBody

try {
    $result = $apiInstance->postSelfReferral($connection_token, $uid, $con_id, $self_referral_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferralsApi->postSelfReferral: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **self_referral_request_body** | [**\Mydex\ApiPdxSdk\Model\SelfReferralRequestBody**](../Model/SelfReferralRequestBody.md)|  | [optional] |

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

## `updateReferralStatus()`

```php
updateReferralStatus($connection_token, $uid, $con_id, $referral_status_update_request_body): \Mydex\ApiPdxSdk\Model\UpdateResponse
```

Supports updating the status of a referral.

Updates the status of a member's referral specified by id. For example, having been referred to a service, the status is set by default to 'Referred' and this route enables it to be updated to 'Accepted' or 'Rejected'

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\ReferralsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$referral_status_update_request_body = new \Mydex\ApiPdxSdk\Model\ReferralStatusUpdateRequestBody(); // \Mydex\ApiPdxSdk\Model\ReferralStatusUpdateRequestBody

try {
    $result = $apiInstance->updateReferralStatus($connection_token, $uid, $con_id, $referral_status_update_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ReferralsApi->updateReferralStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **referral_status_update_request_body** | [**\Mydex\ApiPdxSdk\Model\ReferralStatusUpdateRequestBody**](../Model/ReferralStatusUpdateRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiPdxSdk\Model\UpdateResponse**](../Model/UpdateResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
