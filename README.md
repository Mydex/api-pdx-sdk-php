# OpenAPIClient-php

API for processing subscribers requests to the PDX API to retrieve one or more combinations of data, deliver and update records in a Members PDS and ensure record integrity is maintained.


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/GIT_USER_ID/GIT_REPO_ID.git"
    }
  ],
  "require": {
    "GIT_USER_ID/GIT_REPO_ID": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/OpenAPIClient-php/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *https://api.mydex.org*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*CalendarApi* | [**deleteCalendarEvent**](docs/Api/CalendarApi.md#deletecalendarevent) | **DELETE** /calendar/delete-event | Supports deleting a calendar-event.
*CalendarApi* | [**getCalendarAppointments**](docs/Api/CalendarApi.md#getcalendarappointments) | **GET** /calendar/get-appointments | Retrieve appointments for a given context
*CalendarApi* | [**getCalendarEvents**](docs/Api/CalendarApi.md#getcalendarevents) | **GET** /calendar/get-events | Retrieve calendar events
*CalendarApi* | [**postCalendarAppointment**](docs/Api/CalendarApi.md#postcalendarappointment) | **POST** /calendar/add-appointment | Supports adding a calendar-appointment.
*CalendarApi* | [**postCalendarEvent**](docs/Api/CalendarApi.md#postcalendarevent) | **POST** /calendar/add-event | Supports adding a calendar-event.
*CalendarApi* | [**putCalendarEvent**](docs/Api/CalendarApi.md#putcalendarevent) | **PUT** /calendar/update-event | Supports updating a calendar-event.
*ReferralsApi* | [**getAllReferrals**](docs/Api/ReferralsApi.md#getallreferrals) | **GET** /referrals/read-all | Retrieve rall referrals for a given member.
*ReferralsApi* | [**getSingleReferral**](docs/Api/ReferralsApi.md#getsinglereferral) | **GET** /referrals/read-single | Retrieve a single referral by id for a given member.
*ReferralsApi* | [**postSelfReferral**](docs/Api/ReferralsApi.md#postselfreferral) | **POST** /referrals/self-refer | Supports self-referral.
*ReferralsApi* | [**updateReferralStatus**](docs/Api/ReferralsApi.md#updatereferralstatus) | **PUT** /referrals/update-status | Supports updating the status of a referral.
*SecureMessagesApi* | [**getSecureMessageConversation**](docs/Api/SecureMessagesApi.md#getsecuremessageconversation) | **GET** /secure-messages/conversation | Retrieve all secure messages for a given conversation.
*SecureMessagesApi* | [**postSecureMessageReceive**](docs/Api/SecureMessagesApi.md#postsecuremessagereceive) | **POST** /secure-messages/receive | Supports sending a message to the member&#39;s PDS.
*SecureMessagesApi* | [**postSecureMessageSend**](docs/Api/SecureMessagesApi.md#postsecuremessagesend) | **POST** /secure-messages/send | Supports sending a message from the member&#39;s PDS.
*TimelineApi* | [**getTimeline**](docs/Api/TimelineApi.md#gettimeline) | **GET** /timeline | Retrieve list of timeline items.
*TimelineApi* | [**getTimelineItem**](docs/Api/TimelineApi.md#gettimelineitem) | **GET** /timeline/single-item | Retrieve a single timeline item.

## Models

- [AuthErrorResponse](docs/Model/AuthErrorResponse.md)
- [AuthErrorResponseError](docs/Model/AuthErrorResponseError.md)
- [CalendarAppointmentCreateRequestBody](docs/Model/CalendarAppointmentCreateRequestBody.md)
- [CalendarEvent](docs/Model/CalendarEvent.md)
- [CalendarEventCommonRequestBodyFields](docs/Model/CalendarEventCommonRequestBodyFields.md)
- [CalendarEventCreateRequestBody](docs/Model/CalendarEventCreateRequestBody.md)
- [CalendarEventDeleteRequestBody](docs/Model/CalendarEventDeleteRequestBody.md)
- [CalendarEventUpdateRequestBody](docs/Model/CalendarEventUpdateRequestBody.md)
- [CreateResponse](docs/Model/CreateResponse.md)
- [DeleteResponse](docs/Model/DeleteResponse.md)
- [ErrorResponse](docs/Model/ErrorResponse.md)
- [GetAppointmentsResponse](docs/Model/GetAppointmentsResponse.md)
- [GetEventsResponse](docs/Model/GetEventsResponse.md)
- [ReferralCommonRequestBodyFields](docs/Model/ReferralCommonRequestBodyFields.md)
- [ReferralCommonRequestBodyFieldsReferreeAvailability](docs/Model/ReferralCommonRequestBodyFieldsReferreeAvailability.md)
- [ReferralListResponse](docs/Model/ReferralListResponse.md)
- [ReferralListResponseReferralsInner](docs/Model/ReferralListResponseReferralsInner.md)
- [ReferralSingleResponse](docs/Model/ReferralSingleResponse.md)
- [ReferralSingleResponseReferral](docs/Model/ReferralSingleResponseReferral.md)
- [ReferralStatusUpdateRequestBody](docs/Model/ReferralStatusUpdateRequestBody.md)
- [SecureMessage](docs/Model/SecureMessage.md)
- [SecureMessageCommonFields](docs/Model/SecureMessageCommonFields.md)
- [SecureMessageConversationResponse](docs/Model/SecureMessageConversationResponse.md)
- [SecureMessageReceiveRequest](docs/Model/SecureMessageReceiveRequest.md)
- [SecureMessageSendRequest](docs/Model/SecureMessageSendRequest.md)
- [SelfReferralRequestBody](docs/Model/SelfReferralRequestBody.md)
- [TimelineItemCalendarEvent](docs/Model/TimelineItemCalendarEvent.md)
- [TimelineItemReferral](docs/Model/TimelineItemReferral.md)
- [TimelineItemSecureMessage](docs/Model/TimelineItemSecureMessage.md)
- [TimelineResponse](docs/Model/TimelineResponse.md)
- [TimelineResponseTimelineInner](docs/Model/TimelineResponseTimelineInner.md)
- [TimelineResponseTimelineInnerOneOf](docs/Model/TimelineResponseTimelineInnerOneOf.md)
- [TimelineResponseTimelineInnerOneOf1](docs/Model/TimelineResponseTimelineInnerOneOf1.md)
- [TimelineResponseTimelineInnerOneOf2](docs/Model/TimelineResponseTimelineInnerOneOf2.md)
- [TimelineSingleItemResponse](docs/Model/TimelineSingleItemResponse.md)
- [TimelineSingleItemResponseTimelineItem](docs/Model/TimelineSingleItemResponseTimelineItem.md)
- [UpdateResponse](docs/Model/UpdateResponse.md)

## Authorization

Authentication schemes defined for the API:
### oauth2

- **Type**: `OAuth`
- **Flow**: `application`
- **Authorization URL**: ``
- **Scopes**: 
    - **mydex:pdx**: Global access scope
    - **post:/calendar/add-event**: Create a calendar event
    - **post:/calendar/add-appointment**: Create a calendar appointment
    - **put:/calendar/update-event**: Update a calendar event
    - **delete:/calendar/delete-event**: Delete a calendar event
    - **get:/calendar/get-events**: Read calendar events
    - **get:/calendar/get-appointments**: Read calendar appointments
    - **post:/referrals/self-refer**: Make a self-referral to a service
    - **get:/referrals/read-all**: Read all referrals
    - **get:/referrals/read-single**: Read a single referral
    - **put:/referrals/update-status**: Update the status of a referral
    - **post:/secure-messages/send**: Send a message FROM the member's PDS
    - **post:/secure-messages/receive**: Send a message TO the member's PDS
    - **get:/secure-messages/conversation**: Read messages grouped by the specified conversation
    - **get:/timeline**: Read a list of timeline items
    - **get:/timeline/single-item**: Read a single item from the timeline

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `1.0.0`
    - Package version: `1.0.0`
    - Generator version: `7.23.0`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
