# EdGraph.Platform.Client.Api.IntegrationTypesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateIntegrationType**](IntegrationTypesApi.md#createintegrationtype) | **POST** /integrations/types | Creates an Integration Type. |
| [**DeleteIntegrationType**](IntegrationTypesApi.md#deleteintegrationtype) | **DELETE** /integrations/types/{typeId} | Removes an Integration Type. |
| [**GetIntegrationType**](IntegrationTypesApi.md#getintegrationtype) | **GET** /integrations/types/{typeId} | Gets an Integration Type. |
| [**SearchIntegrationTypes**](IntegrationTypesApi.md#searchintegrationtypes) | **GET** /integrations/types | Search Integration Types. |
| [**UpdateIntegrationType**](IntegrationTypesApi.md#updateintegrationtype) | **PUT** /integrations/types/{typeId} | Updates an Integration Type. |

<a id="createintegrationtype"></a>
# **CreateIntegrationType**
> TenantApiIntegrationsV1CreateIntegrationTypeResponse CreateIntegrationType (TenantApiIntegrationsV1CreateIntegrationTypeRequest tenantApiIntegrationsV1CreateIntegrationTypeRequest = null)

Creates an Integration Type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantApiIntegrationsV1CreateIntegrationTypeRequest** | [**TenantApiIntegrationsV1CreateIntegrationTypeRequest**](TenantApiIntegrationsV1CreateIntegrationTypeRequest.md) |  | [optional]  |

### Return type

[**TenantApiIntegrationsV1CreateIntegrationTypeResponse**](TenantApiIntegrationsV1CreateIntegrationTypeResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteintegrationtype"></a>
# **DeleteIntegrationType**
> TenantApiIntegrationsV1DeleteIntegrationTypeResponse DeleteIntegrationType (Guid typeId)

Removes an Integration Type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **typeId** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1DeleteIntegrationTypeResponse**](TenantApiIntegrationsV1DeleteIntegrationTypeResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getintegrationtype"></a>
# **GetIntegrationType**
> TenantApiIntegrationsV1GetIntegrationTypeResponse GetIntegrationType (Guid typeId)

Gets an Integration Type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **typeId** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1GetIntegrationTypeResponse**](TenantApiIntegrationsV1GetIntegrationTypeResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchintegrationtypes"></a>
# **SearchIntegrationTypes**
> TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel SearchIntegrationTypes (int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search Integration Types.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel**](TenantApiIntegrationsV1IntegrationTypePaginatedItemsViewModel.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateintegrationtype"></a>
# **UpdateIntegrationType**
> Object UpdateIntegrationType (Guid typeId, TenantApiIntegrationsV1UpdateIntegrationTypeRequest tenantApiIntegrationsV1UpdateIntegrationTypeRequest = null)

Updates an Integration Type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **typeId** | **Guid** |  |  |
| **tenantApiIntegrationsV1UpdateIntegrationTypeRequest** | [**TenantApiIntegrationsV1UpdateIntegrationTypeRequest**](TenantApiIntegrationsV1UpdateIntegrationTypeRequest.md) |  | [optional]  |

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
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

