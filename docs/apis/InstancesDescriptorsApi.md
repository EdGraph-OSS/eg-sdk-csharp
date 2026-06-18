# EdGraph.Platform.Client.Api.InstancesDescriptorsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDescriptorAsync**](InstancesDescriptorsApi.md#createdescriptorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Creates a Descriptor. |
| [**DeleteDescriptorAsync**](InstancesDescriptorsApi.md#deletedescriptorasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Deletes a Descriptor. |
| [**GetDescriptorByIdAsync**](InstancesDescriptorsApi.md#getdescriptorbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Retrieves a Descriptor by ID. |
| [**GetDescriptorNamespacesAsync**](InstancesDescriptorsApi.md#getdescriptornamespacesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/namespaces | Retrieves a list of Descriptor Namespaces. |
| [**GetDescriptorsAsync**](InstancesDescriptorsApi.md#getdescriptorsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Retrieves a list of Descriptors. |
| [**UpdateDescriptorAsync**](InstancesDescriptorsApi.md#updatedescriptorasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Updates a Descriptor. |

<a id="createdescriptorasync"></a>
# **CreateDescriptorAsync**
> EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse CreateDescriptorAsync (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1DescriptorType edfiAdminApiEdfiAdminV1DescriptorType = null)

Creates a Descriptor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1DescriptorType** | [**EdfiAdminApiEdfiAdminV1DescriptorType**](EdfiAdminApiEdfiAdminV1DescriptorType.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse.md)

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

<a id="deletedescriptorasync"></a>
# **DeleteDescriptorAsync**
> void DeleteDescriptorAsync (string tenantId, string instanceId, int year, int descriptorId)

Deletes a Descriptor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorId** | **int** |  |  |

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

<a id="getdescriptorbyidasync"></a>
# **GetDescriptorByIdAsync**
> EdfiAdminApiEdfiAdminV1DescriptorType GetDescriptorByIdAsync (string tenantId, string instanceId, int year, int descriptorId)

Retrieves a Descriptor by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorType**](EdfiAdminApiEdfiAdminV1DescriptorType.md)

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

<a id="getdescriptornamespacesasync"></a>
# **GetDescriptorNamespacesAsync**
> EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse GetDescriptorNamespacesAsync (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null)

Retrieves a list of Descriptor Namespaces.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse.md)

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

<a id="getdescriptorsasync"></a>
# **GetDescriptorsAsync**
> EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse GetDescriptorsAsync (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null, string filter = null, string orderBy = null)

Retrieves a list of Descriptors.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse.md)

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

<a id="updatedescriptorasync"></a>
# **UpdateDescriptorAsync**
> EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse UpdateDescriptorAsync (string tenantId, string instanceId, int year, int descriptorId, EdfiAdminApiEdfiAdminV1DescriptorType edfiAdminApiEdfiAdminV1DescriptorType = null)

Updates a Descriptor.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1DescriptorType** | [**EdfiAdminApiEdfiAdminV1DescriptorType**](EdfiAdminApiEdfiAdminV1DescriptorType.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse.md)

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

