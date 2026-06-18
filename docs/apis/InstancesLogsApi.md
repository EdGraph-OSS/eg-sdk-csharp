# EdGraph.Platform.Client.Api.InstancesLogsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetInstanceHttpLogs**](InstancesLogsApi.md#getinstancehttplogs) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/logs/http | Retrieves HTTP logs for a given instance |

<a id="getinstancehttplogs"></a>
# **GetInstanceHttpLogs**
> EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel GetInstanceHttpLogs (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null, long from = null, long to = null, string field = null, bool order = null)

Retrieves HTTP logs for a given instance


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **from** | **long** |  | [optional] [default to 0] |
| **to** | **long** |  | [optional] [default to 0] |
| **field** | **string** |  | [optional] [default to &quot;&quot;] |
| **order** | **bool** |  | [optional] [default to false] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiServicesEdFiAdminUseCasesInstanceLogPaginatedItemsViewModel.md)

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

