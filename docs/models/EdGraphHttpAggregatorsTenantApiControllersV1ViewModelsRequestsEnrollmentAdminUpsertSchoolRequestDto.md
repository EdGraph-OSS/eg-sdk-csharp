# EdGraph.Platform.Client.Model.EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto
The body of a school creation or update.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TenantId** | **Guid** | Must match the tenant in the route. | [optional] 
**ExternalDataSourceSchoolId** | **string** | When present, the upsert is keyed on this id rather than SchoolStateShortCode:  a live school with a matching external id is updated; a soft-deleted one is refused (recover it  first). When absent, a new school is always inserted, and a SchoolStateShortCode  collision on insert is rejected as AlreadyExists. | [optional] 
**SchoolStateShortCode** | **string** | Required. Unique per tenant. | [optional] 
**SchoolName** | **string** | Required. | [optional] 
**DistrictStateShortCode** | **string** |  | [optional] 
**SchoolStateLongCode** | **string** |  | [optional] 
**SchoolLocalCode** | **string** |  | [optional] 
**DistrictLocalCode** | **string** |  | [optional] 
**DistrictStateCode** | **string** |  | [optional] 
**DistrictName** | **string** |  | [optional] 
**GradesServed** | **List&lt;string&gt;** |  | [optional] 
**Address** | **string** |  | [optional] 
**Lat** | **double** |  | [optional] 
**Lon** | **double** |  | [optional] 
**Phone** | **string** |  | [optional] 

[[Back to Model list]](../../README.md#documentation-for-models) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to README]](../../README.md)

