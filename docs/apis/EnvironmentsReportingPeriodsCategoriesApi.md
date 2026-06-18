# EdGraph.Platform.Client.Api.EnvironmentsReportingPeriodsCategoriesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SearchStateReportingPeriodCategories**](EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories | Retrieves the Categories of a Reporting Period. |
| [**SearchStateReportingPeriodSubCategories**](EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodsubcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories/{categoryId}/subcategories | Retrieves the Sub-Categories of a Reporting Period. |

<a id="searchstatereportingperiodcategories"></a>
# **SearchStateReportingPeriodCategories**
> EdGraphServicesStateReportingV1PaginatedCategories SearchStateReportingPeriodCategories (Guid tenantId, Guid environmentId, Guid reportingPeriodId, int pageIndex = null, int pageSize = null, string orderBy = null)

Retrieves the Categories of a Reporting Period.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedCategories**](EdGraphServicesStateReportingV1PaginatedCategories.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchstatereportingperiodsubcategories"></a>
# **SearchStateReportingPeriodSubCategories**
> EdGraphServicesStateReportingV1PaginatedSubCategories SearchStateReportingPeriodSubCategories (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid categoryId, int pageIndex = null, int pageSize = null, string orderBy = null)

Retrieves the Sub-Categories of a Reporting Period.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedSubCategories**](EdGraphServicesStateReportingV1PaginatedSubCategories.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

