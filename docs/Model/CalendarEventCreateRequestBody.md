# CalendarEventCreateRequestBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Title of the event |
**description** | **string** | Detailed description of the event | [optional]
**start_timestamp** | **int** | Start date and time as Unix timestamp |
**end_timestamp** | **int** | End date and time as Unix timestamp |
**status** | **string** | Status of the event | [default to 'TENTATIVE']
**organiser** | **string** | Creator of the event | [optional]
**attendee** | **string** | Person attending the event | [optional]
**location** | **string** | Event location | [optional]
**type** | **string** | Type of event | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
