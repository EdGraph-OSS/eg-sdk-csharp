# EdGraph.Platform.Client.Api.EnrollmentAdminFeederPatternsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateFeederPattern**](EnrollmentAdminFeederPatternsApi.md#createfeederpattern) | **POST** /tenants/{tenantId}/enrollmentadmin/feederpatterns | Creates a feeder pattern. |
| [**DeleteFeederPattern**](EnrollmentAdminFeederPatternsApi.md#deletefeederpattern) | **DELETE** /tenants/{tenantId}/enrollmentadmin/feederpatterns/{id} | Soft-deletes a feeder pattern. |
| [**GetFeederPatternById**](EnrollmentAdminFeederPatternsApi.md#getfeederpatternbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/feederpatterns/{id} | Gets a feeder pattern by id. |
| [**GetFeederPatterns**](EnrollmentAdminFeederPatternsApi.md#getfeederpatterns) | **GET** /tenants/{tenantId}/enrollmentadmin/feederpatterns | Searches feeder patterns: which High/Middle/Elementary school code a point falls into. |
| [**UpdateFeederPattern**](EnrollmentAdminFeederPatternsApi.md#updatefeederpattern) | **PUT** /tenants/{tenantId}/enrollmentadmin/feederpatterns/{id} | Updates a feeder pattern&#39;s geometry and properties. |

<a id="createfeederpattern"></a>
# **CreateFeederPattern**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto CreateFeederPattern (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto = null)

Creates a feeder pattern.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateFeederPatternRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto.md)

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
| **201** | The feeder pattern was created. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletefeederpattern"></a>
# **DeleteFeederPattern**
> void DeleteFeederPattern (string tenantId, Guid id)

Soft-deletes a feeder pattern.


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
| **204** | The feeder pattern was removed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getfeederpatternbyid"></a>
# **GetFeederPatternById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDto GetFeederPatternById (string tenantId, Guid id)

Gets a feeder pattern by id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDto.md)

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

<a id="getfeederpatterns"></a>
# **GetFeederPatterns**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDtoPaginatedItemsViewModel GetFeederPatterns (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, string search = null)

Searches feeder patterns: which High/Middle/Elementary school code a point falls into.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 50] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **search** | **string** | Free-text match on feederPattern/highSchool/middleSchool/elementary. | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternDtoPaginatedItemsViewModel.md)

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

<a id="updatefeederpattern"></a>
# **UpdateFeederPattern**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto UpdateFeederPattern (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto = null)

Updates a feeder pattern's geometry and properties.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateFeederPatternRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminFeederPatternMutationResultDto.md)

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
| **200** | The feeder pattern was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

