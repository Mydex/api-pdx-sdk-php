# Mydex\ApiPdxSdk\TimelineApi

Operations related to timeline

All URIs are relative to https://api.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getTimeline()**](TimelineApi.md#getTimeline) | **GET** /timeline | Retrieve list of timeline items. |
| [**getTimelineItem()**](TimelineApi.md#getTimelineItem) | **GET** /timeline/single-item | Retrieve a single timeline item. |


## `getTimeline()`

```php
getTimeline($connection_token, $uid, $con_id): \Mydex\ApiPdxSdk\Model\TimelineResponse
```

Retrieve list of timeline items.

Returns a list of timeline items which includes: referrals, calendar events and secure messages.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\TimelineApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.

try {
    $result = $apiInstance->getTimeline($connection_token, $uid, $con_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimelineApi->getTimeline: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |

### Return type

[**\Mydex\ApiPdxSdk\Model\TimelineResponse**](../Model/TimelineResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getTimelineItem()`

```php
getTimelineItem($connection_token, $uid, $con_id, $feature_block, $feature_block_id): \Mydex\ApiPdxSdk\Model\TimelineSingleItemResponse
```

Retrieve a single timeline item.

Returns a single timeline item based on feature block and feature block id requested e.g. a 'referral' with id 123.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\TimelineApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$feature_block = referrals; // string | The feature block the teimline item belongs to
$feature_block_id = 123; // int | The specific ID of the record within the specified feature block e.g. if 'referrals' is the feature block, then this should be a specific referral id

try {
    $result = $apiInstance->getTimelineItem($connection_token, $uid, $con_id, $feature_block, $feature_block_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TimelineApi->getTimelineItem: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **feature_block** | **string**| The feature block the teimline item belongs to | |
| **feature_block_id** | **int**| The specific ID of the record within the specified feature block e.g. if &#39;referrals&#39; is the feature block, then this should be a specific referral id | |

### Return type

[**\Mydex\ApiPdxSdk\Model\TimelineSingleItemResponse**](../Model/TimelineSingleItemResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
