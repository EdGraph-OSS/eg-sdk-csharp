# EdGraph.Platform.Client.Api.IntegrationVendorsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateIntegrationVendor**](IntegrationVendorsApi.md#createintegrationvendor) | **POST** /integrations/vendors | Creates an Integration Vendor. |
| [**DeleteIntegrationVendor**](IntegrationVendorsApi.md#deleteintegrationvendor) | **DELETE** /integrations/vendors/{vendorId} | Removes an Integration Vendor. |
| [**GetIntegrationVendor**](IntegrationVendorsApi.md#getintegrationvendor) | **GET** /integrations/vendors/{vendorId} | Gets an Integration Vendor. |
| [**SearchIntegrationVendors**](IntegrationVendorsApi.md#searchintegrationvendors) | **GET** /integrations/vendors | Search Integration Vendors. |
| [**UpdateIntegrationVendor**](IntegrationVendorsApi.md#updateintegrationvendor) | **PUT** /integrations/vendors/{vendorId} | Updates an Integration Vendor. |

<a id="createintegrationvendor"></a>
# **CreateIntegrationVendor**
> TenantApiIntegrationsV1CreateIntegrationVendorResponse CreateIntegrationVendor (TenantApiIntegrationsV1CreateIntegrationVendorRequest tenantApiIntegrationsV1CreateIntegrationVendorRequest = null)

Creates an Integration Vendor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantApiIntegrationsV1CreateIntegrationVendorRequest** | [**TenantApiIntegrationsV1CreateIntegrationVendorRequest**](TenantApiIntegrationsV1CreateIntegrationVendorRequest.md) |  | [optional]  |

### Return type

[**TenantApiIntegrationsV1CreateIntegrationVendorResponse**](TenantApiIntegrationsV1CreateIntegrationVendorResponse.md)

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

<a id="deleteintegrationvendor"></a>
# **DeleteIntegrationVendor**
> TenantApiIntegrationsV1DeleteIntegrationVendorResponse DeleteIntegrationVendor (Guid vendorId)

Removes an Integration Vendor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **vendorId** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1DeleteIntegrationVendorResponse**](TenantApiIntegrationsV1DeleteIntegrationVendorResponse.md)

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

<a id="getintegrationvendor"></a>
# **GetIntegrationVendor**
> TenantApiIntegrationsV1GetIntegrationVendorResponse GetIntegrationVendor (Guid vendorId)

Gets an Integration Vendor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **vendorId** | **Guid** |  |  |

### Return type

[**TenantApiIntegrationsV1GetIntegrationVendorResponse**](TenantApiIntegrationsV1GetIntegrationVendorResponse.md)

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

<a id="searchintegrationvendors"></a>
# **SearchIntegrationVendors**
> TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel SearchIntegrationVendors (int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search Integration Vendors.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel**](TenantApiIntegrationsV1IntegrationVendorPaginatedItemsViewModel.md)

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

<a id="updateintegrationvendor"></a>
# **UpdateIntegrationVendor**
> Object UpdateIntegrationVendor (Guid vendorId, TenantApiIntegrationsV1UpdateIntegrationVendorRequest tenantApiIntegrationsV1UpdateIntegrationVendorRequest = null)

Updates an Integration Vendor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **vendorId** | **Guid** |  |  |
| **tenantApiIntegrationsV1UpdateIntegrationVendorRequest** | [**TenantApiIntegrationsV1UpdateIntegrationVendorRequest**](TenantApiIntegrationsV1UpdateIntegrationVendorRequest.md) |  | [optional]  |

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

