# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto
The body of a Program creation. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateProgramRequestDto.SchoolId, EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateProgramRequestDto.ProgramTypeId and  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateProgramRequestDto.RequirementIds are record ids of existing rows; the service copies their display  fields onto the program and rejects an id it cannot find.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TenantId** | **Guid** |  | [optional] 
**SchoolId** | **Guid** |  | [optional] 
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

