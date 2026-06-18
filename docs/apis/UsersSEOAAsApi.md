# EdGraph.Platform.Client.Api.UsersSEOAAsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUserSEOAA**](UsersSEOAAsApi.md#adduserseoaa) | **POST** /v2/tenants/{tenantId}/users/{userId}/seoaas | Add User SEOAAs |
| [**DeleteUserSEOAA**](UsersSEOAAsApi.md#deleteuserseoaa) | **DELETE** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Delete User SEOAAs |
| [**SearchUserSEOAA**](UsersSEOAAsApi.md#searchuserseoaa) | **GET** /v2/tenants/{tenantId}/users/{userId}/seoaas | Search User SEOAAs |
| [**UpdateUserSEOAA**](UsersSEOAAsApi.md#updateuserseoaa) | **PUT** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Update User SEOAAs |

<a id="adduserseoaa"></a>
# **AddUserSEOAA**
> IdentityApiUserV1SEOAAAddedResponse AddUserSEOAA (Guid tenantId, Guid userId, EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest = null)

Add User SEOAAs


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest**](EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SEOAAAddedResponse**](IdentityApiUserV1SEOAAAddedResponse.md)

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

<a id="deleteuserseoaa"></a>
# **DeleteUserSEOAA**
> IdentityApiUserV1SEOAAUpdatedResponse DeleteUserSEOAA (Guid tenantId, Guid userId, string seoaaId)

Delete User SEOAAs


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **seoaaId** | **string** |  |  |

### Return type

[**IdentityApiUserV1SEOAAUpdatedResponse**](IdentityApiUserV1SEOAAUpdatedResponse.md)

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

<a id="searchuserseoaa"></a>
# **SearchUserSEOAA**
> IdentityApiUserV1GetSEOAAsResponse SearchUserSEOAA (Guid tenantId, Guid userId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search User SEOAAs


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV1GetSEOAAsResponse**](IdentityApiUserV1GetSEOAAsResponse.md)

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

<a id="updateuserseoaa"></a>
# **UpdateUserSEOAA**
> IdentityApiUserV1SEOAAUpdatedResponse UpdateUserSEOAA (Guid tenantId, Guid userId, string seoaaId, EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest = null)

Update User SEOAAs


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **seoaaId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest**](EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SEOAAUpdatedResponse**](IdentityApiUserV1SEOAAUpdatedResponse.md)

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

