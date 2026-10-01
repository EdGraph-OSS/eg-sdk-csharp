# EdGraph.Platform.Client.Model.EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationMessage
One Program-seat choice on a Registration - zero-to-many, independently approvable. See  ApproveRegistrationApplication / GetRegistrationApplications.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ApplicationId** | **string** |  | [optional] 
**ApplicationStatus** | **string** |  | [optional] 
**ProgramId** | **string** | enrollment-svc-programs._id - one school&#39;s offering of a program. | [optional] 
**Rank** | **int** | The family&#39;s preference order within the round. 1-based and contiguous across the  registration - the matcher&#39;s contract. Assigned server-side, never supplied by a caller. | [optional] 
**Priority** | **int** | The priority tier - sibling, staff, feeder, PreK. Unset until the priority engine stamps it. | [optional] 
**ApplicationRoundId** | **string** | Foreign key into the application round this entry was submitted to. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

