# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto
The body of a contact creation.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TenantId** | **Guid** | Must match the tenant in the route. | [optional] 
**ContactId** | **string** | The contact&#39;s identifier in the source system. Distinct from the record id, which the service  assigns and returns in the response. | [optional] 
**FirstName** | **string** | Required. Never overridable - only email and phone are. | [optional] 
**LastName** | **string** | Required. Never overridable - only email and phone are. | [optional] 
**Email** | **string** | The SIS-sourced email. Correcting it later is an override and goes through the  &#x60;email-override&#x60; route instead - see EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.UpdateContactRequestDto. | [optional] 
**Phone** | **string** | The SIS-sourced phone, on the same terms as Email. | [optional] 
**Students** | [**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminContactStudentRequestDto.md) | The students to link the contact to. Optional; omit or send an empty list for a contact with no  links yet. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

