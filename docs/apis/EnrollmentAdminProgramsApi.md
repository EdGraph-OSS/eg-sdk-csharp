# EdGraph.Platform.Client.Api.EnrollmentAdminProgramsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateProgram**](EnrollmentAdminProgramsApi.md#createprogram) | **POST** /tenants/{tenantId}/enrollmentadmin/programs | Creates a Program at a school. The body names the school, the program type and the  requirements by id; the service copies their display fields onto the row. |
| [**DeleteProgram**](EnrollmentAdminProgramsApi.md#deleteprogram) | **DELETE** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Removes a Program (soft delete). |
| [**GetProgramApplications**](EnrollmentAdminProgramsApi.md#getprogramapplications) | **GET** /tenants/{tenantId}/enrollmentadmin/programs/{id}/applications | Gets the Registration Applications referencing a Program. |
| [**GetProgramById**](EnrollmentAdminProgramsApi.md#getprogrambyid) | **GET** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Gets a Program by its record id. |
| [**GetPrograms**](EnrollmentAdminProgramsApi.md#getprograms) | **GET** /tenants/{tenantId}/enrollmentadmin/programs | Searches Programs. Every row is one school&#39;s offering of a program: the school, the program  type and the requirements are embedded on it, each with its own &#x60;_id&#x60; beside the id of  the row it was copied from. |
| [**UpdateProgram**](EnrollmentAdminProgramsApi.md#updateprogram) | **PUT** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Updates a Program. The school a program runs at never changes; everything else, including  the program type and the requirement set, is replaced from the body. |

<a id="createprogram"></a>
# **CreateProgram**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto CreateProgram (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto = null)

Creates a Program at a school. The body names the school, the program type and the  requirements by id; the service copies their display fields onto the row.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto.md)

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
| **201** | The program was created. |  -  |
| **400** | Bad Request. The request was invalid, or named a school, program type or requirement that does not exist. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteprogram"></a>
# **DeleteProgram**
> void DeleteProgram (string tenantId, Guid id)

Removes a Program (soft delete).


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
| **204** | The program was removed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprogramapplications"></a>
# **GetProgramApplications**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramApplicationDto&gt; GetProgramApplications (string tenantId, Guid id)

Gets the Registration Applications referencing a Program.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramApplicationDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramApplicationDto.md)

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

<a id="getprogrambyid"></a>
# **GetProgramById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto GetProgramById (string tenantId, Guid id)

Gets a Program by its record id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto.md)

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

<a id="getprograms"></a>
# **GetPrograms**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel GetPrograms (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, string search = null, string schoolLocalCode = null, string programTypeId = null)

Searches Programs. Every row is one school's offering of a program: the school, the program  type and the requirements are embedded on it, each with its own `_id` beside the id of  the row it was copied from.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 50] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **search** | **string** | Free-text match on program name/code. | [optional] [default to &quot;&quot;] |
| **schoolLocalCode** | **string** | Narrows to programs offered at this school. Not a security boundary. | [optional] [default to &quot;&quot;] |
| **programTypeId** | **string** | Narrows to programs of this program type (its record id). | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel.md)

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

<a id="updateprogram"></a>
# **UpdateProgram**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto UpdateProgram (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto = null)

Updates a Program. The school a program runs at never changes; everything else, including  the program type and the requirement set, is replaced from the body.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto.md)

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
| **200** | The program was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

