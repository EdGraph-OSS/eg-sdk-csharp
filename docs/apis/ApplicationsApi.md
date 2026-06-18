# EdGraph.Platform.Client.Api.ApplicationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetTenantApplicationProfileByIdAsync**](ApplicationsApi.md#gettenantapplicationprofilebyidasync) | **GET** /tenants/{tenantId}/applications/{applicationId} | Retrieves an application |
| [**GetTenantApplicationsAsync**](ApplicationsApi.md#gettenantapplicationsasync) | **GET** /tenants/{tenantId}/applications | Retrieves a list of applications associated to this tenant |

<a id="gettenantapplicationprofilebyidasync"></a>
# **GetTenantApplicationProfileByIdAsync**
> ApplicationApiApplicationV1ApplicationProfileResponse GetTenantApplicationProfileByIdAsync (string tenantId, string applicationId)

Retrieves an application


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **applicationId** | **string** |  |  |

### Return type

[**ApplicationApiApplicationV1ApplicationProfileResponse**](ApplicationApiApplicationV1ApplicationProfileResponse.md)

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

<a id="gettenantapplicationsasync"></a>
# **GetTenantApplicationsAsync**
> ApplicationApiApplicationV1ApplicationListResponse GetTenantApplicationsAsync (string tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of applications associated to this tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional]  |
| **filter** | **string** |  | [optional]  |

### Return type

[**ApplicationApiApplicationV1ApplicationListResponse**](ApplicationApiApplicationV1ApplicationListResponse.md)

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

