# EdGraph.Platform.Client.Api.EdFiSyncApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEdFiSync**](EdFiSyncApi.md#createedfisync) | **POST** /tenants/{tenantId}/jobs/edfisync | Creates an Ed-Fi Sync Job for a given tenant |
| [**ExecuteEdFiSyncJob**](EdFiSyncApi.md#executeedfisyncjob) | **PUT** /tenants/{tenantId}/jobs/edfisync/execute | Executes an Ed-Fi Sync Job |
| [**GetEdFiSyncData**](EdFiSyncApi.md#getedfisyncdata) | **GET** /tenants/{tenantId}/jobs/edfisync | Retrieves Ed-Fi Sync Connection Data for a given tenant |
| [**UpdateEdFiSync**](EdFiSyncApi.md#updateedfisync) | **PUT** /tenants/{tenantId}/jobs/edfisync | Updates an Ed-Fi Sync for a given tenant |

<a id="createedfisync"></a>
# **CreateEdFiSync**
> EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult CreateEdFiSync (string tenantId, EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto = null)

Creates an Ed-Fi Sync Job for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto** | [**EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto**](EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult**](EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult.md)

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

<a id="executeedfisyncjob"></a>
# **ExecuteEdFiSyncJob**
> DataSyncApiJobV1JobExecutionRequestedResponse ExecuteEdFiSyncJob (Guid tenantId)

Executes an Ed-Fi Sync Job


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**DataSyncApiJobV1JobExecutionRequestedResponse**](DataSyncApiJobV1JobExecutionRequestedResponse.md)

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

<a id="getedfisyncdata"></a>
# **GetEdFiSyncData**
> DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile GetEdFiSyncData (Guid tenantId)

Retrieves Ed-Fi Sync Connection Data for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile**](DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile.md)

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

<a id="updateedfisync"></a>
# **UpdateEdFiSync**
> MicrosoftAspNetCoreMvcNoContentResult UpdateEdFiSync (Guid tenantId, Object body = null)

Updates an Ed-Fi Sync for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**MicrosoftAspNetCoreMvcNoContentResult**](MicrosoftAspNetCoreMvcNoContentResult.md)

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

