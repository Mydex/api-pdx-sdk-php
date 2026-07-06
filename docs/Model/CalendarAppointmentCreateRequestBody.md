# CalendarAppointmentCreateRequestBody

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
**context** | **string** | The context the appointment belongs to e.g. a referral |
**context_id** | **int** | The id of the specific context record that this appointment relates to e.g. the referral id |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
