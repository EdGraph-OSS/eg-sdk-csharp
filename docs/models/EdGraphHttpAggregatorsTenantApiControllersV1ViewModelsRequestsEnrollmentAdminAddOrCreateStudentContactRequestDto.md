# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto
The body of a student-contact link where the contact is created if its  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.AddOrCreateStudentContactRequestDto.ExternalDataSourceContactId (the SIS id) does not already exist. When it does, the submitted name/email/phone are ignored - an existing  contact is only linked, never overwritten, by this route.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ExternalDataSourceContactId** | **string** |  | [optional] 
**FirstName** | **string** |  | [optional] 
**LastName** | **string** |  | [optional] 
**Email** | **string** |  | [optional] 
**Phone** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

