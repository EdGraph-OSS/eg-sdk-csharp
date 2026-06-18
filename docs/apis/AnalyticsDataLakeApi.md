# EdGraph.Platform.Client.Api.AnalyticsDataLakeApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetPaginatedLakehouseRecords**](AnalyticsDataLakeApi.md#getpaginatedlakehouserecords) | **GET** /tenants/{tenantId}/analytics/datalake/query | Retrieves gold-tier data from the lakehouse |

<a id="getpaginatedlakehouserecords"></a>
# **GetPaginatedLakehouseRecords**
> AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse GetPaginatedLakehouseRecords (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves gold-tier data from the lakehouse


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse**](AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse.md)

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

