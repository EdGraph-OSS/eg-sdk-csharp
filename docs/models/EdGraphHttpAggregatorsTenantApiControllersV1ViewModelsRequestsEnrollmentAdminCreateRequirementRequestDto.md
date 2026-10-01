# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto
The body of a requirement creation. The route names the tenant, so the body carries only the  requirement's own fields. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.RequirementType is one of `document`, `url`,  `information` or `event`, lowercase as stored. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.IsRequired left out  creates a required requirement. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.IsUploadEnabled left out is false, and the service  forces it false for a `url` or `information` requirement. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.CreateRequirementRequestDto.Url is required  for a `url` requirement (an absolute http or https link) and not used for other types. A code  already used in the tenant (deleted rows included) is refused with 409.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RequirementType** | **string** |  | [optional] 
**RequirementCode** | **string** |  | [optional] 
**RequirementTitle** | **string** |  | [optional] 
**RequirementDescription** | **string** |  | [optional] 
**IsUploadEnabled** | **bool** |  | [optional] 
**IsRequired** | **bool** |  | [optional] 
**Url** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

