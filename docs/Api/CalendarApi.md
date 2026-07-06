# Mydex\ApiPdxSdk\CalendarApi

Operations related to calendar events

All URIs are relative to https://api.mydex.org, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteCalendarEvent()**](CalendarApi.md#deleteCalendarEvent) | **DELETE** /calendar/delete-event | Supports deleting a calendar-event. |
| [**getCalendarAppointments()**](CalendarApi.md#getCalendarAppointments) | **GET** /calendar/get-appointments | Retrieve appointments for a given context |
| [**getCalendarEvents()**](CalendarApi.md#getCalendarEvents) | **GET** /calendar/get-events | Retrieve calendar events |
| [**postCalendarAppointment()**](CalendarApi.md#postCalendarAppointment) | **POST** /calendar/add-appointment | Supports adding a calendar-appointment. |
| [**postCalendarEvent()**](CalendarApi.md#postCalendarEvent) | **POST** /calendar/add-event | Supports adding a calendar-event. |
| [**putCalendarEvent()**](CalendarApi.md#putCalendarEvent) | **PUT** /calendar/update-event | Supports updating a calendar-event. |


## `deleteCalendarEvent()`

```php
deleteCalendarEvent($connection_token, $uid, $con_id, $calendar_event_delete_request_body): \Mydex\ApiPdxSdk\Model\DeleteResponse
```

Supports deleting a calendar-event.

Deletes an event in the user's calendar.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\CalendarApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$calendar_event_delete_request_body = new \Mydex\ApiPdxSdk\Model\CalendarEventDeleteRequestBody(); // \Mydex\ApiPdxSdk\Model\CalendarEventDeleteRequestBody

try {
    $result = $apiInstance->deleteCalendarEvent($connection_token, $uid, $con_id, $calendar_event_delete_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarApi->deleteCalendarEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **calendar_event_delete_request_body** | [**\Mydex\ApiPdxSdk\Model\CalendarEventDeleteRequestBody**](../Model/CalendarEventDeleteRequestBody.md)|  | [optional] |

### Return type

[**\Mydex\ApiPdxSdk\Model\DeleteResponse**](../Model/DeleteResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCalendarAppointments()`

```php
getCalendarAppointments($connection_token, $uid, $con_id, $context, $context_id): \Mydex\ApiPdxSdk\Model\GetAppointmentsResponse
```

Retrieve appointments for a given context

Returns a list of appointments filtered by context and context_id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\CalendarApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$context = referral; // string | The context this belongs to
$context_id = 123; // int | The specific ID of the context record

try {
    $result = $apiInstance->getCalendarAppointments($connection_token, $uid, $con_id, $context, $context_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarApi->getCalendarAppointments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **context** | **string**| The context this belongs to | |
| **context_id** | **int**| The specific ID of the context record | |

### Return type

[**\Mydex\ApiPdxSdk\Model\GetAppointmentsResponse**](../Model/GetAppointmentsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCalendarEvents()`

```php
getCalendarEvents($connection_token, $uid, $con_id): \Mydex\ApiPdxSdk\Model\GetEventsResponse
```

Retrieve calendar events

Returns a list of calendar events.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\CalendarApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.

try {
    $result = $apiInstance->getCalendarEvents($connection_token, $uid, $con_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarApi->getCalendarEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |

### Return type

[**\Mydex\ApiPdxSdk\Model\GetEventsResponse**](../Model/GetEventsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `postCalendarAppointment()`

```php
postCalendarAppointment($connection_token, $uid, $con_id, $calendar_appointment_create_request_body): \Mydex\ApiPdxSdk\Model\CreateResponse
```

Supports adding a calendar-appointment.

Creates a new appointment in the user's calendar. An appointment must be made within a specified context e.g. a 'Referral'

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\CalendarApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$calendar_appointment_create_request_body = new \Mydex\ApiPdxSdk\Model\CalendarAppointmentCreateRequestBody(); // \Mydex\ApiPdxSdk\Model\CalendarAppointmentCreateRequestBody

try {
    $result = $apiInstance->postCalendarAppointment($connection_token, $uid, $con_id, $calendar_appointment_create_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarApi->postCalendarAppointment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **calendar_appointment_create_request_body** | [**\Mydex\ApiPdxSdk\Model\CalendarAppointmentCreateRequestBody**](../Model/CalendarAppointmentCreateRequestBody.md)|  | [optional] |

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

## `postCalendarEvent()`

```php
postCalendarEvent($connection_token, $uid, $con_id, $calendar_event_create_request_body): \Mydex\ApiPdxSdk\Model\CreateResponse
```

Supports adding a calendar-event.

Creates a new event in the user's calendar.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\CalendarApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$calendar_event_create_request_body = new \Mydex\ApiPdxSdk\Model\CalendarEventCreateRequestBody(); // \Mydex\ApiPdxSdk\Model\CalendarEventCreateRequestBody

try {
    $result = $apiInstance->postCalendarEvent($connection_token, $uid, $con_id, $calendar_event_create_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarApi->postCalendarEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **calendar_event_create_request_body** | [**\Mydex\ApiPdxSdk\Model\CalendarEventCreateRequestBody**](../Model/CalendarEventCreateRequestBody.md)|  | [optional] |

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

## `putCalendarEvent()`

```php
putCalendarEvent($connection_token, $uid, $con_id, $calendar_event_update_request_body): \Mydex\ApiPdxSdk\Model\UpdateResponse
```

Supports updating a calendar-event.

Updates an event in the user's calendar. For example, updating the 'status' from 'INVITED' to 'CONFIRMED' when a user accepts the invitation to an appointment.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = Mydex\ApiPdxSdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Mydex\ApiPdxSdk\Api\CalendarApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$connection_token = abc123xyz456; // string | Member's Connection Key
$uid = 1234; // string | The unique ID of a mydex member
$con_id = 1234-67890; // string | The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID.
$calendar_event_update_request_body = new \Mydex\ApiPdxSdk\Model\CalendarEventUpdateRequestBody(); // \Mydex\ApiPdxSdk\Model\CalendarEventUpdateRequestBody

try {
    $result = $apiInstance->putCalendarEvent($connection_token, $uid, $con_id, $calendar_event_update_request_body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CalendarApi->putCalendarEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **connection_token** | **string**| Member&#39;s Connection Key | |
| **uid** | **string**| The unique ID of a mydex member | |
| **con_id** | **string**| The connection_id is a shared id between a connection and a member. It is a hyphenated combination of the member UID and the Dedicated Connection NID. | |
| **calendar_event_update_request_body** | [**\Mydex\ApiPdxSdk\Model\CalendarEventUpdateRequestBody**](../Model/CalendarEventUpdateRequestBody.md)|  | [optional] |

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
