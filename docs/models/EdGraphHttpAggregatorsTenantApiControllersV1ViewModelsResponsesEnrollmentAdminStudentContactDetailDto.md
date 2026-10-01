# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactDetailDto
A contact linked to a student, joined with that contact's own live name/email/phone, plus the  association attributes read from this student's own EnrollmentStudentContact entry for the  contact. The reverse-direction sibling of EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.ContactStudentDetailDto. `id` is the  contact record id; `externalDataSourceContactId` is its SIS id, when it has one.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | [optional] 
**ExternalDataSourceContactId** | **string** |  | [optional] 
**FirstName** | **string** |  | [optional] 
**LastName** | **string** |  | [optional] 
**Email** | **string** |  | [optional] 
**Phone** | **string** |  | [optional] 
**Priority** | **int** |  | [optional] 
**Relationship** | **string** |  | [optional] 
**LivesWithStudent** | **bool** |  | [optional] 
**HasLegalCustody** | **bool** |  | [optional] 
**CanPickUp** | **bool** |  | [optional] 
**IsEmergency** | **bool** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

