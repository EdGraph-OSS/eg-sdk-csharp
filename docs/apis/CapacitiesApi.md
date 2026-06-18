# EdGraph.Platform.Client.Api.CapacitiesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AssignMyGroupToCapacity**](CapacitiesApi.md#assignmygrouptocapacity) | **POST** /tenants/{tenantId}/analytics/capacities | Assigns the specified group to the specified capacity. |
| [**GetAllAnalyticsPowerBiCapacities**](CapacitiesApi.md#getallanalyticspowerbicapacities) | **GET** /tenants/{tenantId}/analytics/capacities | Retrieves a list of capacities in Power Bi that the user has access to. |
| [**ResumeCapacityAsync**](CapacitiesApi.md#resumecapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/resume | Resumes currently suspended capacity |
| [**SuspendCapacityAsync**](CapacitiesApi.md#suspendcapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/suspend | Suspends currently active capacity |

<a id="assignmygrouptocapacity"></a>
# **AssignMyGroupToCapacity**
> void AssignMyGroupToCapacity (string tenantId, AnalyticsApiCapacitiesV1AssignCapacityRequest analyticsApiCapacitiesV1AssignCapacityRequest = null)

Assigns the specified group to the specified capacity.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiCapacitiesV1AssignCapacityRequest** | [**AnalyticsApiCapacitiesV1AssignCapacityRequest**](AnalyticsApiCapacitiesV1AssignCapacityRequest.md) |  | [optional]  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getallanalyticspowerbicapacities"></a>
# **GetAllAnalyticsPowerBiCapacities**
> AnalyticsApiCapacitiesV1CapacityResponse GetAllAnalyticsPowerBiCapacities (string tenantId)

Retrieves a list of capacities in Power Bi that the user has access to.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**AnalyticsApiCapacitiesV1CapacityResponse**](AnalyticsApiCapacitiesV1CapacityResponse.md)

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

<a id="resumecapacityasync"></a>
# **ResumeCapacityAsync**
> void ResumeCapacityAsync (string tenantId, AnalyticsApiCapacitiesV1ResumeCapacityRequest analyticsApiCapacitiesV1ResumeCapacityRequest = null)

Resumes currently suspended capacity


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiCapacitiesV1ResumeCapacityRequest** | [**AnalyticsApiCapacitiesV1ResumeCapacityRequest**](AnalyticsApiCapacitiesV1ResumeCapacityRequest.md) |  | [optional]  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="suspendcapacityasync"></a>
# **SuspendCapacityAsync**
> void SuspendCapacityAsync (string tenantId, AnalyticsApiCapacitiesV1SuspendCapacityRequest analyticsApiCapacitiesV1SuspendCapacityRequest = null)

Suspends currently active capacity


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiCapacitiesV1SuspendCapacityRequest** | [**AnalyticsApiCapacitiesV1SuspendCapacityRequest**](AnalyticsApiCapacitiesV1SuspendCapacityRequest.md) |  | [optional]  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

