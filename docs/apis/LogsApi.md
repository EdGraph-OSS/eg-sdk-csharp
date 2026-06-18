# EdGraph.Platform.Client.Api.LogsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetLogs**](LogsApi.md#getlogs) | **GET** /tenants/{tenantId}/validations/logs | Retrieves a list of Logs. |

<a id="getlogs"></a>
# **GetLogs**
> ValidationsApiValidationResultsV1FindResponse GetLogs (string tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string environmentId = null, string collectionId = null, string containerId = null, string ruleId = null, string jobId = null, string jobExecutionId = null)

Retrieves a list of Logs.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional]  |
| **environmentId** | **string** |  | [optional]  |
| **collectionId** | **string** |  | [optional]  |
| **containerId** | **string** |  | [optional]  |
| **ruleId** | **string** |  | [optional]  |
| **jobId** | **string** |  | [optional]  |
| **jobExecutionId** | **string** |  | [optional]  |

### Return type

[**ValidationsApiValidationResultsV1FindResponse**](ValidationsApiValidationResultsV1FindResponse.md)

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

