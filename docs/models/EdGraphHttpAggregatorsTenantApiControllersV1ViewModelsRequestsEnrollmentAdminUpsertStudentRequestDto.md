# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertStudentRequestDto
The body of a student upsert, keyed by EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpsertStudentRequestDto.StudentLocalCode (the district's SIS code). Contact association is managed  exclusively through the `/students/{id}/contacts` sub-resource, not through this call.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TenantId** | **Guid** |  | [optional] 
**StudentLocalCode** | **string** |  | [optional] 
**StudentStateCode** | **string** |  | [optional] 
**ExternalDataSourceStudentId** | **string** |  | [optional] 
**FirstName** | **string** |  | [optional] 
**MiddleName** | **string** |  | [optional] 
**LastName** | **string** |  | [optional] 
**Birthdate** | **string** |  | [optional] 
**Last4SSN** | **string** |  | [optional] 
**NextAddress** | **string** |  | [optional] 
**NextGradeLevel** | **string** |  | [optional] 
**NextSchoolStateShortCode** | **string** |  | [optional] 
**NextSchoolStateCode** | **string** |  | [optional] 
**NextSchoolName** | **string** |  | [optional] 
**NextSchoolAddress** | **string** |  | [optional] 
**EligibilityCode** | **string** |  | [optional] 
**EligibilityDescription** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

