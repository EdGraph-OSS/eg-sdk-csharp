# EdGraph.Platform.Client.Api.EnrollmentAdminProgramTypesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetProgramTypeById**](EnrollmentAdminProgramTypesApi.md#getprogramtypebyid) | **GET** /tenants/{tenantId}/enrollmentadmin/programtypes/{id} | Gets a program type by its record id. |
| [**GetProgramTypes**](EnrollmentAdminProgramTypesApi.md#getprogramtypes) | **GET** /tenants/{tenantId}/enrollmentadmin/programtypes | Lists the tenant&#39;s program types, sorted by name. Unpaged: a district has a handful. A  program&#39;s &#x60;programType.programTypeId&#x60; is one of these ids, and the programs search  filters on it (&#x60;programTypeId&#x60;). |

<a id="getprogramtypebyid"></a>
# **GetProgramTypeById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto GetProgramTypeById (string tenantId, Guid id)

Gets a program type by its record id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto.md)

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

<a id="getprogramtypes"></a>
# **GetProgramTypes**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto&gt; GetProgramTypes (string tenantId)

Lists the tenant's program types, sorted by name. Unpaged: a district has a handful. A  program's `programType.programTypeId` is one of these ids, and the programs search  filters on it (`programTypeId`).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramTypeResponseDto.md)

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

