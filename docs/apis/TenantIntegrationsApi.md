# EdGraph.Platform.Client.Api.TenantIntegrationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddTenantIntegration**](TenantIntegrationsApi.md#addtenantintegration) | **POST** /tenants/{tenantId}/integrations | Creates an Integration for a tenant. |
| [**DeleteTenantIntegration**](TenantIntegrationsApi.md#deletetenantintegration) | **DELETE** /tenants/{tenantId}/integrations/{id} | Removes a tenant Integration. |
| [**GetTenantIntegration**](TenantIntegrationsApi.md#gettenantintegration) | **GET** /tenants/{tenantId}/integrations/{id} | Gets a tenant Integration. |
| [**SearchIntegrations**](TenantIntegrationsApi.md#searchintegrations) | **GET** /tenants/{tenantId}/integrations | Search a Tenant&#39;s Integrations |
| [**UpdateTenantIntegration**](TenantIntegrationsApi.md#updatetenantintegration) | **PUT** /tenants/{tenantId}/integrations/{id} | Updates a tenant Integration. |

<a id="addtenantintegration"></a>
# **AddTenantIntegration**
> TenantApiIntegrationsV1CreateIntegrationResponse AddTenantIntegration (Guid tenantId, TenantApiIntegrationsV1CreateIntegrationRequest tenantApiIntegrationsV1CreateIntegrationRequest = null)

Creates an Integration for a tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **tenantApiIntegrationsV1CreateIntegrationRequest** | [**TenantApiIntegrationsV1CreateIntegrationRequest**](TenantApiIntegrationsV1CreateIntegrationRequest.md) |  | [optional]  |

### Return type

[**TenantApiIntegrationsV1CreateIntegrationResponse**](TenantApiIntegrationsV1CreateIntegrationResponse.md)

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
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletetenantintegration"></a>
# **DeleteTenantIntegration**
> TenantApiIntegrationsV1DeleteIntegrationResponse DeleteTenantIntegration (Guid tenantId, Guid id)

Removes a tenant Integration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1DeleteIntegrationResponse**](TenantApiIntegrationsV1DeleteIntegrationResponse.md)

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
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettenantintegration"></a>
# **GetTenantIntegration**
> TenantApiIntegrationsV1GetIntegrationResponse GetTenantIntegration (Guid tenantId, Guid id)

Gets a tenant Integration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1GetIntegrationResponse**](TenantApiIntegrationsV1GetIntegrationResponse.md)

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
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchintegrations"></a>
# **SearchIntegrations**
> TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel SearchIntegrations (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search a Tenant's Integrations


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel**](TenantApiIntegrationsV1IntegrationPaginatedItemsViewModel.md)

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

<a id="updatetenantintegration"></a>
# **UpdateTenantIntegration**
> Object UpdateTenantIntegration (Guid tenantId, Guid id, TenantApiIntegrationsV1UpdateIntegrationRequest tenantApiIntegrationsV1UpdateIntegrationRequest = null)

Updates a tenant Integration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **id** | **Guid** |  |  |
| **tenantApiIntegrationsV1UpdateIntegrationRequest** | [**TenantApiIntegrationsV1UpdateIntegrationRequest**](TenantApiIntegrationsV1UpdateIntegrationRequest.md) |  | [optional]  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

