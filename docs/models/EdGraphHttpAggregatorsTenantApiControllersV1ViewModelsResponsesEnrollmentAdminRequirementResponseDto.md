# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto
Something a family must satisfy for a program. Programs embed a copy of it  (EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementRefDto), where `requirementId` is this row's EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.Id.  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.RequirementType is one of `document`, `url`, `information` or  `event`. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.IsUploadEnabled can only be true for a `document` or an `event`.  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.IsRequired false means the requirement is optional. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.RequirementResponseDto.Url is the online  form of a `url` requirement, absent for other types.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** |  | [optional] 
**TenantId** | **Guid** |  | [optional] 
**RequirementType** | **string** |  | [optional] 
**RequirementCode** | **string** |  | [optional] 
**RequirementTitle** | **string** |  | [optional] 
**RequirementDescription** | **string** |  | [optional] 
**IsUploadEnabled** | **bool** |  | [optional] 
**IsRequired** | **bool** |  | [optional] 
**Url** | **string** |  | [optional] 
**CreatedBy** | **string** |  | [optional] 
**CreatedDateTime** | **DateTime** |  | [optional] 
**LastModifiedBy** | **string** |  | [optional] 
**LastModifiedDateTime** | **DateTime** |  | [optional] 
**IsDeleted** | **bool** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

