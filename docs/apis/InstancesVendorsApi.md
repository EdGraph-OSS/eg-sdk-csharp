# EdGraph.Platform.Client.Api.InstancesVendorsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateVendorAsync**](InstancesVendorsApi.md#createvendorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Creates a new Vendor. |
| [**DeleteVendorAsync**](InstancesVendorsApi.md#deletevendorasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Deletes a Vendor. |
| [**GetVendorByIdAsync**](InstancesVendorsApi.md#getvendorbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Retrieves a Vendor by ID. |
| [**GetVendorsAsync**](InstancesVendorsApi.md#getvendorsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors | Retrieves a list of Vendors. |
| [**SyncVendorAsync**](InstancesVendorsApi.md#syncvendorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId}/sync | Copies a Vendor from one instance to another/other instance(s). |
| [**UpdateVendorAsync**](InstancesVendorsApi.md#updatevendorasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/vendors/{vendorId} | Updates a Vendor. |

<a id="createvendorasync"></a>
# **CreateVendorAsync**
> EdfiAdminApiEdfiAdminV1VendorCreatedResponse CreateVendorAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1CreateVendorRequest edfiAdminApiEdfiAdminV1CreateVendorRequest = null)

Creates a new Vendor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateVendorRequest** | [**EdfiAdminApiEdfiAdminV1CreateVendorRequest**](EdfiAdminApiEdfiAdminV1CreateVendorRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1VendorCreatedResponse**](EdfiAdminApiEdfiAdminV1VendorCreatedResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletevendorasync"></a>
# **DeleteVendorAsync**
> void DeleteVendorAsync (string tenantId, string instanceId, int vendorId)

Deletes a Vendor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **vendorId** | **int** |  |  |

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getvendorbyidasync"></a>
# **GetVendorByIdAsync**
> EdfiAdminApiEdfiAdminV1VendorProfileResponse GetVendorByIdAsync (string tenantId, string instanceId, string vendorId)

Retrieves a Vendor by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **vendorId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1VendorProfileResponse**](EdfiAdminApiEdfiAdminV1VendorProfileResponse.md)

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

<a id="getvendorsasync"></a>
# **GetVendorsAsync**
> EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel GetVendorsAsync (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Vendors.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1VendorListResponsePaginatedItemsViewModel.md)

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

<a id="syncvendorasync"></a>
# **SyncVendorAsync**
> void SyncVendorAsync (string tenantId, string instanceId, int vendorId, EdfiAdminApiEdfiAdminV1SyncVendorRequest edfiAdminApiEdfiAdminV1SyncVendorRequest = null)

Copies a Vendor from one instance to another/other instance(s).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **vendorId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SyncVendorRequest** | [**EdfiAdminApiEdfiAdminV1SyncVendorRequest**](EdfiAdminApiEdfiAdminV1SyncVendorRequest.md) |  | [optional]  |

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
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatevendorasync"></a>
# **UpdateVendorAsync**
> EdfiAdminApiEdfiAdminV1VendorUpdatedResponse UpdateVendorAsync (string tenantId, string instanceId, string vendorId, EdfiAdminApiEdfiAdminV1UpdateVendorRequest edfiAdminApiEdfiAdminV1UpdateVendorRequest = null)

Updates a Vendor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **vendorId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateVendorRequest** | [**EdfiAdminApiEdfiAdminV1UpdateVendorRequest**](EdfiAdminApiEdfiAdminV1UpdateVendorRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1VendorUpdatedResponse**](EdfiAdminApiEdfiAdminV1VendorUpdatedResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

