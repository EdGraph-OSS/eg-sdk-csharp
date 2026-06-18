# EdGraph.Platform.Client.Api.APIClientsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTenantApiClientAsync**](APIClientsApi.md#createtenantapiclientasync) | **POST** /tenants/{tenantId}/apiclients | Creates a new OpenId API Client |
| [**DeleteTenantApiClientAsync**](APIClientsApi.md#deletetenantapiclientasync) | **DELETE** /tenants/{tenantId}/apiclients/{clientId} | Deletes an OpenId API Client |
| [**GetAllTenantApiClientsAsync**](APIClientsApi.md#getalltenantapiclientsasync) | **GET** /tenants/{tenantId}/apiclients | Retrieves a list of OpenId API Clients associated to this tenant |
| [**GetTenantApiClientByIdAsync**](APIClientsApi.md#gettenantapiclientbyidasync) | **GET** /tenants/{tenantId}/apiclients/{clientId} | Retrieves an OpenId API Client |
| [**RegenerateTenantApiClientSecretAsync**](APIClientsApi.md#regeneratetenantapiclientsecretasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId}/regeneratesecret | Regenerates an OpenId API Client&#39;s secret |
| [**UpdateTenantApiClientAsync**](APIClientsApi.md#updatetenantapiclientasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId} | Updates an OpenId API Client |

<a id="createtenantapiclientasync"></a>
# **CreateTenantApiClientAsync**
> IdentityApiApiClientV1ApiClientCreatedResponse CreateTenantApiClientAsync (string tenantId, IdentityApiApiClientV1CreateApiClientRequest identityApiApiClientV1CreateApiClientRequest = null)

Creates a new OpenId API Client


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **identityApiApiClientV1CreateApiClientRequest** | [**IdentityApiApiClientV1CreateApiClientRequest**](IdentityApiApiClientV1CreateApiClientRequest.md) |  | [optional]  |

### Return type

[**IdentityApiApiClientV1ApiClientCreatedResponse**](IdentityApiApiClientV1ApiClientCreatedResponse.md)

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletetenantapiclientasync"></a>
# **DeleteTenantApiClientAsync**
> void DeleteTenantApiClientAsync (string tenantId, string clientId)

Deletes an OpenId API Client


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |

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
| **204** | The resource was successfully deleted. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getalltenantapiclientsasync"></a>
# **GetAllTenantApiClientsAsync**
> IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel GetAllTenantApiClientsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of OpenId API Clients associated to this tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel**](IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel.md)

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

<a id="gettenantapiclientbyidasync"></a>
# **GetTenantApiClientByIdAsync**
> IdentityApiApiClientV1ApiClientProfileResponse GetTenantApiClientByIdAsync (string tenantId, string clientId)

Retrieves an OpenId API Client


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |

### Return type

[**IdentityApiApiClientV1ApiClientProfileResponse**](IdentityApiApiClientV1ApiClientProfileResponse.md)

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

<a id="regeneratetenantapiclientsecretasync"></a>
# **RegenerateTenantApiClientSecretAsync**
> IdentityApiApiClientV1ApiClientSecretRegeneratedResponse RegenerateTenantApiClientSecretAsync (string tenantId, string clientId, IdentityApiApiClientV1RegenerateApiClientSecretRequest identityApiApiClientV1RegenerateApiClientSecretRequest = null)

Regenerates an OpenId API Client's secret


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **identityApiApiClientV1RegenerateApiClientSecretRequest** | [**IdentityApiApiClientV1RegenerateApiClientSecretRequest**](IdentityApiApiClientV1RegenerateApiClientSecretRequest.md) |  | [optional]  |

### Return type

[**IdentityApiApiClientV1ApiClientSecretRegeneratedResponse**](IdentityApiApiClientV1ApiClientSecretRegeneratedResponse.md)

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

<a id="updatetenantapiclientasync"></a>
# **UpdateTenantApiClientAsync**
> IdentityApiApiClientV1ApiClientUpdatedResponse UpdateTenantApiClientAsync (string tenantId, string clientId, IdentityApiApiClientV1UpdateApiClientRequest identityApiApiClientV1UpdateApiClientRequest = null)

Updates an OpenId API Client


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **identityApiApiClientV1UpdateApiClientRequest** | [**IdentityApiApiClientV1UpdateApiClientRequest**](IdentityApiApiClientV1UpdateApiClientRequest.md) |  | [optional]  |

### Return type

[**IdentityApiApiClientV1ApiClientUpdatedResponse**](IdentityApiApiClientV1ApiClientUpdatedResponse.md)

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

