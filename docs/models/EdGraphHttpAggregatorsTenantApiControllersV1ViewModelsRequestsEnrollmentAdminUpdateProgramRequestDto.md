# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto
The body of a Program update. The school never changes; the program type and the requirement  set are replaced from the ids given here (an empty list clears the requirements).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | [optional] 
**TenantId** | **Guid** |  | [optional] 
**ProgramCode** | **string** |  | [optional] 
**ProgramName** | **string** |  | [optional] 
**ProgramTypeId** | **Guid** |  | [optional] 
**EligibilityCriteria** | **string** |  | [optional] 
**RequirementIds** | **List&lt;Guid&gt;** |  | [optional] 
**Grades** | **List&lt;string&gt;** |  | [optional] 
**CapacityByGrade** | [**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto.md) |  | [optional] 
**Zone** | **string** |  | [optional] 
**Latitude** | **double** |  | [optional] 
**Longitude** | **double** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

