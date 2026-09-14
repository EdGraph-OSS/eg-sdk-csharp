# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto
EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateSchoolProgramRequestDto.Code/EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateSchoolProgramRequestDto.Name/EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateSchoolProgramRequestDto.ProgramType/EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateSchoolProgramRequestDto.EligibilityCriteria/              EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateSchoolProgramRequestDto.RequiredDocuments only apply when the row being updated is school-specific; on a              row linked to a catalog entry they are inherited and a request that sets them is rejected -              server-side, since the aggregator does not know which case an id names until it reads the row.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | [optional] 
**TenantId** | **Guid** |  | [optional] 
**Code** | **string** |  | [optional] 
**Name** | **string** |  | [optional] 
**ProgramType** | **string** |  | [optional] 
**EligibilityCriteria** | **string** |  | [optional] 
**RequiredDocuments** | **List&lt;string&gt;** |  | [optional] 
**Grades** | **List&lt;string&gt;** |  | [optional] 
**CapacityByGrade** | [**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto.md) |  | [optional] 
**Zone** | **string** |  | [optional] 
**Latitude** | **double** |  | [optional] 
**Longitude** | **double** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

