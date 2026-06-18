# EdGraph.Platform.Client.Api.TenantJobsDSLApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDslJob**](TenantJobsDSLApi.md#createdsljob) | **POST** /tenants/{tenantId}/jobs/dsl | Creates a DSL Sync Job for a given tenant |
| [**ExecuteDslJob**](TenantJobsDSLApi.md#executedsljob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId}/execute | Executes a DSL Sync Job for a given tenant |
| [**GetDslJob**](TenantJobsDSLApi.md#getdsljob) | **GET** /tenants/{tenantId}/jobs/dsl/{jobId} | Retrieves a DSL jobs profile for a given tenant |
| [**UpdateDslJob**](TenantJobsDSLApi.md#updatedsljob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId} | Updates a DSL Sync Job for a given tenant |

<a id="createdsljob"></a>
# **CreateDslJob**
> DataSyncApiDslV1JobCreatedResponse CreateDslJob (Guid tenantId, DataSyncApiDslV1CreateJobRequest dataSyncApiDslV1CreateJobRequest = null)

Creates a DSL Sync Job for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **dataSyncApiDslV1CreateJobRequest** | [**DataSyncApiDslV1CreateJobRequest**](DataSyncApiDslV1CreateJobRequest.md) |  | [optional]  |

### Return type

[**DataSyncApiDslV1JobCreatedResponse**](DataSyncApiDslV1JobCreatedResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
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

<a id="executedsljob"></a>
# **ExecuteDslJob**
> DataSyncApiDslV1DslJobExecutedResponse ExecuteDslJob (Guid tenantId, Guid jobId)

Executes a DSL Sync Job for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |

### Return type

[**DataSyncApiDslV1DslJobExecutedResponse**](DataSyncApiDslV1DslJobExecutedResponse.md)

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
| **202** | The job execution was successfully requested. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getdsljob"></a>
# **GetDslJob**
> DataSyncApiDslV1DslProfile GetDslJob (Guid tenantId, Guid jobId)

Retrieves a DSL jobs profile for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |

### Return type

[**DataSyncApiDslV1DslProfile**](DataSyncApiDslV1DslProfile.md)

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

<a id="updatedsljob"></a>
# **UpdateDslJob**
> Object UpdateDslJob (Guid tenantId, Guid jobId, DataSyncApiDslV1UpdateJobRequest dataSyncApiDslV1UpdateJobRequest = null)

Updates a DSL Sync Job for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |
| **dataSyncApiDslV1UpdateJobRequest** | [**DataSyncApiDslV1UpdateJobRequest**](DataSyncApiDslV1UpdateJobRequest.md) |  | [optional]  |

### Return type

**Object**

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **204** | The resource was successfully updated. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

