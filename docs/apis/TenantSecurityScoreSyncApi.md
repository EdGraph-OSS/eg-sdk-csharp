# EdGraph.Platform.Client.Api.TenantSecurityScoreSyncApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#createsecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore | Creates an Security Score Sync Job for a given tenant |
| [**ExecuteSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#executesecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore/execute | Executes an Security Score Sync Job |
| [**GetSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#getsecurityscoresyncjob) | **GET** /tenants/{tenantId}/jobs/securityscore | Retrieves a Security Score Sync Job for a given tenant |
| [**GetSecurityScoreSyncJobExecution**](TenantSecurityScoreSyncApi.md#getsecurityscoresyncjobexecution) | **GET** /tenants/{tenantId}/jobs/securityscore/{jobId}/executions/{jobExecutionId} | Retrieves a Security Score Sync Job Execution for a given tenant |
| [**UpdateSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#updatesecurityscoresyncjob) | **PUT** /tenants/{tenantId}/jobs/securityscore | Updates a Security Score Sync for a given tenant |

<a id="createsecurityscoresyncjob"></a>
# **CreateSecurityScoreSyncJob**
> EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult CreateSecurityScoreSyncJob (string tenantId, EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest = null)

Creates an Security Score Sync Job for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest** | [**EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest**](EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult**](EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult.md)

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

<a id="executesecurityscoresyncjob"></a>
# **ExecuteSecurityScoreSyncJob**
> void ExecuteSecurityScoreSyncJob (Guid tenantId)

Executes an Security Score Sync Job


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

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
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **202** | Accepted |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getsecurityscoresyncjob"></a>
# **GetSecurityScoreSyncJob**
> DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile GetSecurityScoreSyncJob (Guid tenantId)

Retrieves a Security Score Sync Job for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile**](DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile.md)

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

<a id="getsecurityscoresyncjobexecution"></a>
# **GetSecurityScoreSyncJobExecution**
> DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile GetSecurityScoreSyncJobExecution (Guid tenantId, Guid jobId, Guid jobExecutionId)

Retrieves a Security Score Sync Job Execution for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |
| **jobExecutionId** | **Guid** |  |  |

### Return type

[**DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile**](DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile.md)

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

<a id="updatesecurityscoresyncjob"></a>
# **UpdateSecurityScoreSyncJob**
> void UpdateSecurityScoreSyncJob (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest = null)

Updates a Security Score Sync for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest** | [**EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest**](EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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
| **204** | No Content |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

