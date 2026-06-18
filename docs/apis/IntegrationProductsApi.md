# EdGraph.Platform.Client.Api.IntegrationProductsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateIntegrationProduct**](IntegrationProductsApi.md#createintegrationproduct) | **POST** /integrations/products | Creates an Integration Product. |
| [**DeleteIntegrationProduct**](IntegrationProductsApi.md#deleteintegrationproduct) | **DELETE** /integrations/products/{productId} | Removes an Integration Product. |
| [**GetIntegrationProduct**](IntegrationProductsApi.md#getintegrationproduct) | **GET** /integrations/products/{productId} | Gets an Integration Product. |
| [**SearchIntegrationProducts**](IntegrationProductsApi.md#searchintegrationproducts) | **GET** /integrations/products | Search Integration Products. |
| [**UpdateIntegrationProduct**](IntegrationProductsApi.md#updateintegrationproduct) | **PUT** /integrations/products/{productId} | Updates an Integration Product. |

<a id="createintegrationproduct"></a>
# **CreateIntegrationProduct**
> TenantApiIntegrationsV1CreateIntegrationProductResponse CreateIntegrationProduct (TenantApiIntegrationsV1CreateIntegrationProductRequest tenantApiIntegrationsV1CreateIntegrationProductRequest = null)

Creates an Integration Product.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantApiIntegrationsV1CreateIntegrationProductRequest** | [**TenantApiIntegrationsV1CreateIntegrationProductRequest**](TenantApiIntegrationsV1CreateIntegrationProductRequest.md) |  | [optional]  |

### Return type

[**TenantApiIntegrationsV1CreateIntegrationProductResponse**](TenantApiIntegrationsV1CreateIntegrationProductResponse.md)

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

<a id="deleteintegrationproduct"></a>
# **DeleteIntegrationProduct**
> TenantApiIntegrationsV1DeleteIntegrationProductResponse DeleteIntegrationProduct (Guid productId)

Removes an Integration Product.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1DeleteIntegrationProductResponse**](TenantApiIntegrationsV1DeleteIntegrationProductResponse.md)

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

<a id="getintegrationproduct"></a>
# **GetIntegrationProduct**
> TenantApiIntegrationsV1GetIntegrationProductResponse GetIntegrationProduct (Guid productId)

Gets an Integration Product.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1GetIntegrationProductResponse**](TenantApiIntegrationsV1GetIntegrationProductResponse.md)

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

<a id="searchintegrationproducts"></a>
# **SearchIntegrationProducts**
> TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel SearchIntegrationProducts (int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search Integration Products.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel**](TenantApiIntegrationsV1IntegrationProductPaginatedItemsViewModel.md)

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

<a id="updateintegrationproduct"></a>
# **UpdateIntegrationProduct**
> Object UpdateIntegrationProduct (Guid productId, TenantApiIntegrationsV1UpdateIntegrationProductRequest tenantApiIntegrationsV1UpdateIntegrationProductRequest = null)

Updates an Integration Product.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **productId** | **Guid** |  |  |
| **tenantApiIntegrationsV1UpdateIntegrationProductRequest** | [**TenantApiIntegrationsV1UpdateIntegrationProductRequest**](TenantApiIntegrationsV1UpdateIntegrationProductRequest.md) |  | [optional]  |

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

