# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDto
One entry in a contact's override history.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventId** | **string** |  | [optional] 
**Detail** | **string** | Which detail this entry is about: &#x60;email&#x60; or &#x60;phone&#x60;. | [optional] 
**Action** | **string** | &#x60;set&#x60; or &#x60;removed&#x60;. A removal returns the detail to its SIS value. | [optional] 
**PreviousValue** | **string** | The value this entry superseded, if any. Superseded values are kept, never deleted. | [optional] 
**NewValue** | **string** |  | [optional] 
**SisValue** | **string** |  | [optional] 
**OverriddenBy** | **string** |  | [optional] 
**OverriddenAt** | **DateTime** |  | [optional] 
**ActingStudentId** | **string** | The student whose screen the change was made from, when one was recorded. | [optional] 
**StudentIds** | **List&lt;string&gt;** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

