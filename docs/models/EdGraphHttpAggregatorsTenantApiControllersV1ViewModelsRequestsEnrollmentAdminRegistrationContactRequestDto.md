# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationContactRequestDto
A contact carried on a Registration create call. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.RegistrationContactRequestDto.Id is the entry's own id (minted when  omitted); EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.RegistrationContactRequestDto.ContactId is the EnrollmentContact record id, resolved server-side from the  email/phone when omitted; EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.RegistrationContactRequestDto.ExternalDataSourceContactId is the SIS id, when known.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**ContactId** | **string** |  | [optional] 
**ContactName** | **string** |  | [optional] 
**ContactPhone** | **string** |  | [optional] 
**ContactEmail** | **string** |  | [optional] 
**ExternalDataSourceContactId** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

