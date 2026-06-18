# EdGraph.Platform.Client.Api.TenantsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetTenantByIdAsync**](TenantsApi.md#gettenantbyidasync) | **GET** /tenants/{tenantId} | Retrieves the profile of a specific tenant |
| [**UpdateTenantAsync**](TenantsApi.md#updatetenantasync) | **PUT** /tenants/{tenantId} | Updates a tenant&#39;s profile |

<a id="gettenantbyidasync"></a>
# **GetTenantByIdAsync**
> TenantApiTenantV1TenantProfileResponse GetTenantByIdAsync (string tenantId)

Retrieves the profile of a specific tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**TenantApiTenantV1TenantProfileResponse**](TenantApiTenantV1TenantProfileResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatetenantasync"></a>
# **UpdateTenantAsync**
> TenantApiTenantV1TenantUpdatedResponse UpdateTenantAsync (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest = null)

Updates a tenant's profile

Note: Only the tenant's Identity Providers can be updated at this time


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsTenantsUpdateTenantRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1TenantUpdatedResponse**](TenantApiTenantV1TenantUpdatedResponse.md)

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

