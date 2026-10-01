# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto
The body of a contact-student link. Enrollment resolves or creates the linked EnrollmentStudent  document server-side - no other student fields are accepted here.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**StudentLocalCode** | **string** | The student&#39;s SIS code. Required unless EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.AddContactStudentRequestDto.Id is given. If no student has this SIS  code yet, a new one is created under it. | [optional] 
**Id** | **Guid** | An existing student&#39;s own internal id (as returned by, e.g., GET .../contacts/{id}/students).  When given, this always wins over EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.AddContactStudentRequestDto.StudentLocalCode: that student is linked directly and  never auto-created - a 404 if it does not exist, rather than a blank duplicate. | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

