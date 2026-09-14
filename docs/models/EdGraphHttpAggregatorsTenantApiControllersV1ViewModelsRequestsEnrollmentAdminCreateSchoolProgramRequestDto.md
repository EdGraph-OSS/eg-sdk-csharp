# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto
Covers two cases, distinguished by EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateSchoolProgramRequestDto.ProgramCatalogEntryId: adding an existing  district catalog entry to a school (a \"school association\" - EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateSchoolProgramRequestDto.Code/  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateSchoolProgramRequestDto.Name/EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateSchoolProgramRequestDto.ProgramType/EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateSchoolProgramRequestDto.EligibilityCriteria/  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateSchoolProgramRequestDto.RequiredDocuments are inherited and must be left unset), or creating a brand new  school-specific program (those same fields are required).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TenantId** | **Guid** |  | [optional] 
**SchoolCode** | **string** |  | [optional] 
**SchoolName** | **string** |  | [optional] 
**ProgramCatalogEntryId** | **Guid** |  | [optional] 
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

