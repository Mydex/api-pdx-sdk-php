# CalendarEventUpdateRequestBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **string** | Title of the event | [optional]
**description** | **string** | Detailed description of the event | [optional]
**start_timestamp** | **int** | Start date and time as Unix timestamp | [optional]
**end_timestamp** | **int** | End date and time as Unix timestamp | [optional]
**status** | **string** | Status of the event | [optional] [default to 'TENTATIVE']
**organiser** | **string** | Creator of the event | [optional]
**attendee** | **string** | Person attending the event | [optional]
**location** | **string** | Event location | [optional]
**id** | **int** | ID of the calendar-event to be updated |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
