# EdGraph.Platform.Client.Api.EnrollmentAdminSchoolsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteEnrollmentSchool**](EnrollmentAdminSchoolsApi.md#deleteenrollmentschool) | **DELETE** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Deletes an Enrollment School. |
| [**DisableEnrollmentSchool**](EnrollmentAdminSchoolsApi.md#disableenrollmentschool) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/{id}/disable | Disables an Enrollment School. |
| [**EnableEnrollmentSchool**](EnrollmentAdminSchoolsApi.md#enableenrollmentschool) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/{id}/enable | Enables an Enrollment School. |
| [**GetEnrollmentSchoolById**](EnrollmentAdminSchoolsApi.md#getenrollmentschoolbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Gets an Enrollment School by its record id, with the programs it runs. |
| [**GetEnrollmentSchools**](EnrollmentAdminSchoolsApi.md#getenrollmentschools) | **GET** /tenants/{tenantId}/enrollmentadmin/schools | Searches Enrollment Schools. |
| [**UpdateEnrollmentSchool**](EnrollmentAdminSchoolsApi.md#updateenrollmentschool) | **PUT** /tenants/{tenantId}/enrollmentadmin/schools/{id} | Replaces an Enrollment School by its record id. |
| [**UpsertEnrollmentSchool**](EnrollmentAdminSchoolsApi.md#upsertenrollmentschool) | **POST** /tenants/{tenantId}/enrollmentadmin/schools | Creates or updates an Enrollment School, keyed on &#x60;externalDataSourceSchoolId&#x60;. |

<a id="deleteenrollmentschool"></a>
# **DeleteEnrollmentSchool**
> void DeleteEnrollmentSchool (string tenantId, Guid id)

Deletes an Enrollment School.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **204** | The resource was successfully deleted. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="disableenrollmentschool"></a>
# **DisableEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto DisableEnrollmentSchool (string tenantId, Guid id)

Disables an Enrollment School.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The resource was successfully updated. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="enableenrollmentschool"></a>
# **EnableEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto EnableEnrollmentSchool (string tenantId, Guid id)

Enables an Enrollment School.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolEnabledResponseDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The resource was successfully updated. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getenrollmentschoolbyid"></a>
# **GetEnrollmentSchoolById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto GetEnrollmentSchoolById (string tenantId, Guid id)

Gets an Enrollment School by its record id, with the programs it runs.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolResponseDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getenrollmentschools"></a>
# **GetEnrollmentSchools**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel GetEnrollmentSchools (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, string search = null)

Searches Enrollment Schools.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 50] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **search** | **string** | Free-text match on school name or school code. | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolListItemResponseDtoPaginatedItemsViewModel.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateenrollmentschool"></a>
# **UpdateEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto UpdateEnrollmentSchool (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto = null)

Replaces an Enrollment School by its record id.

Full replace, not keyed on `externalDataSourceSchoolId` - use the id in the route.  `isEnabled` is never moved by this call - use `PUT .../schools/{id}/enable` or  `.../disable` instead.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The school was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="upsertenrollmentschool"></a>
# **UpsertEnrollmentSchool**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto UpsertEnrollmentSchool (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto = null)

Creates or updates an Enrollment School, keyed on `externalDataSourceSchoolId`.

Upsert semantics: when `externalDataSourceSchoolId` is present and matches a live school  in the tenant, that school is updated - every field, including `schoolStateShortCode`, is  overwritten. A soft-deleted match is refused (recover it first). Otherwise a new school is  always inserted, keeping the external id if one was given; a `schoolStateShortCode`  collision on insert is rejected as AlreadyExists (409) rather than overwriting the existing  school - a POST with no external id no longer overwrites by code. `isEnabled` is never  moved by this call - use `PUT .../schools/{id}/enable` or `.../disable` instead.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertSchoolRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminSchoolMutationResultDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **201** | A new school was created. |  -  |
| **200** | An existing school (matched by external id) was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **409** | A school with this &#x60;schoolStateShortCode&#x60; already exists. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

