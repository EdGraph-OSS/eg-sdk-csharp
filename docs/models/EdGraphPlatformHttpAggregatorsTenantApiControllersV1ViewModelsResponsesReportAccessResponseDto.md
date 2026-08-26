# EdGraph.Platform.Client.Model.EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesReportAccessResponseDto
A report's audience targeting, returned with EdGraph.Platform.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.ReportAccessResponseDto.TargetAudience as a stable  string (\"AnyoneInTenant\" | \"UsersWithRoleInTenant\" | \"SpecificUsersInTenant\") so the client  does not depend on proto enum serialization.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TenantId** | **string** |  | [optional] 
**ReportId** | **string** |  | [optional] 
**TargetAudience** | **string** |  | [optional] 
**StaffClassifications** | **List&lt;string&gt;** |  | [optional] 
**Users** | **List&lt;string&gt;** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

