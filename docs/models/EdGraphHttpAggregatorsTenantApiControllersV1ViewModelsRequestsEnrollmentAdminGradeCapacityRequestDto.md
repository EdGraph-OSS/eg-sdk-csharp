# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminGradeCapacityRequestDto
One grade's seats. EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.GradeCapacityRequestDto.SeatsAvailable, EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.GradeCapacityRequestDto.LotteryEligible and  EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Requests.EnrollmentAdmin.GradeCapacityRequestDto.SchoolYear are what the lottery reads; the Salesforce sync normally supplies  them, and an admin edit may leave them null to keep whatever the row already has unset.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Grade** | **string** |  | [optional] 
**Capacity** | **int** |  | [optional] 
**Enrolled** | **int** |  | [optional] 
**SeatsAvailable** | **int** |  | [optional] 
**LotteryEligible** | **bool** |  | [optional] 
**SchoolYear** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

