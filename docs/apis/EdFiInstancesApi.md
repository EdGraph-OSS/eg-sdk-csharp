# EdGraph.Platform.Client.Api.EdFiInstancesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAllEdFiAdminConnectionsFromAnalyticsAsync**](EdFiInstancesApi.md#getalledfiadminconnectionsfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/connections | Retrieves a list of EdFi Admin connections |
| [**GetAllEdFiAdminInstancesFromAnalyticsAsync**](EdFiInstancesApi.md#getalledfiadmininstancesfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances | Retrieves a list of EdFi Admin instances |
| [**GetEdFiAdminInstanceByIdFromAnalyticsAsync**](EdFiInstancesApi.md#getedfiadmininstancebyidfromanalyticsasync) | **GET** /tenants/{tenantId}/analytics/edfiadmin/instances/{instanceId} | Retrieves an Ed-Fi Admin instance by ID. |

<a id="getalledfiadminconnectionsfromanalyticsasync"></a>
# **GetAllEdFiAdminConnectionsFromAnalyticsAsync**
> AnalyticsApiReportsV1ReportPaginatedItemsResponse GetAllEdFiAdminConnectionsFromAnalyticsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of EdFi Admin connections


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiReportsV1ReportPaginatedItemsResponse**](AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Missing the required permissions to access to this tenant/resource |  -  |
| **500** | Oops! Can&#39;t retrieve the list of EdFi Admin connections right now |  -  |
| **200** | List of EdFi Admin connections |  -  |
| **400** | Tenant has missing/invalid values |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getalledfiadmininstancesfromanalyticsasync"></a>
# **GetAllEdFiAdminInstancesFromAnalyticsAsync**
> AnalyticsApiReportsV1ReportPaginatedItemsResponse GetAllEdFiAdminInstancesFromAnalyticsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of EdFi Admin instances


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiReportsV1ReportPaginatedItemsResponse**](AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Missing the required permissions to access to this tenant/resource |  -  |
| **500** | Oops! Can&#39;t retrieve the list of EdFi Admin instances right now |  -  |
| **200** | List of EdFi Admin instances |  -  |
| **400** | Tenant has missing/invalid values |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getedfiadmininstancebyidfromanalyticsasync"></a>
# **GetEdFiAdminInstanceByIdFromAnalyticsAsync**
> EdfiAdminApiEdfiAdminV1Instance GetEdFiAdminInstanceByIdFromAnalyticsAsync (string tenantId, string instanceId)

Retrieves an Ed-Fi Admin instance by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1Instance**](EdfiAdminApiEdfiAdminV1Instance.md)

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

