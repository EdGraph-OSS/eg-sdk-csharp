# EdGraph.Platform.Client.Api.InstancesDescriptorMappingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDescriptorMapping**](InstancesDescriptorMappingsApi.md#createdescriptormapping) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Creates a Descriptor Mapping. |
| [**DeleteDescriptorMapping**](InstancesDescriptorMappingsApi.md#deletedescriptormapping) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Deletes a Descriptor Mapping. |
| [**ExportDescriptorMappings**](InstancesDescriptorMappingsApi.md#exportdescriptormappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/export | Exports all Descriptor Mappings as a JSON file. |
| [**GetDescriptorMappingById**](InstancesDescriptorMappingsApi.md#getdescriptormappingbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Retrieves a Descriptor Mapping by ID. |
| [**GetDescriptorMappings**](InstancesDescriptorMappingsApi.md#getdescriptormappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Retrieves a list of Descriptors Mappings. |
| [**ImportDescriptorMappings**](InstancesDescriptorMappingsApi.md#importdescriptormappings) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/import | Imports Descriptor Mappings from a JSON file. |
| [**UpdateDescriptorMapping**](InstancesDescriptorMappingsApi.md#updatedescriptormapping) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Updates a Descriptor Mapping. |

<a id="createdescriptormapping"></a>
# **CreateDescriptorMapping**
> EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse CreateDescriptorMapping (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest = null)

Creates a Descriptor Mapping.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest** | [**EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest**](EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse.md)

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

<a id="deletedescriptormapping"></a>
# **DeleteDescriptorMapping**
> void DeleteDescriptorMapping (string tenantId, string instanceId, int year, string descriptorMappingId)

Deletes a Descriptor Mapping.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorMappingId** | **string** |  |  |

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

<a id="exportdescriptormappings"></a>
# **ExportDescriptorMappings**
> void ExportDescriptorMappings (string tenantId, string instanceId, int year, string varNamespace = null)

Exports all Descriptor Mappings as a JSON file.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **varNamespace** | **string** |  | [optional]  |

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
| **200** | The descriptor mappings were successfully exported. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getdescriptormappingbyid"></a>
# **GetDescriptorMappingById**
> EdfiAdminApiEdfiAdminV1DescriptorMapping GetDescriptorMappingById (string tenantId, string instanceId, int year, string descriptorMappingId)

Retrieves a Descriptor Mapping by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorMappingId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMapping**](EdfiAdminApiEdfiAdminV1DescriptorMapping.md)

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

<a id="getdescriptormappings"></a>
# **GetDescriptorMappings**
> EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse GetDescriptorMappings (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null, string varNamespace = null)

Retrieves a list of Descriptors Mappings.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **varNamespace** | **string** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse.md)

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

<a id="importdescriptormappings"></a>
# **ImportDescriptorMappings**
> void ImportDescriptorMappings (string tenantId, string instanceId, int year, System.IO.Stream file = null)

Imports Descriptor Mappings from a JSON file.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **file** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |

### Return type

void (empty response body)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **200** | The descriptor mappings were successfully imported. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatedescriptormapping"></a>
# **UpdateDescriptorMapping**
> EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse UpdateDescriptorMapping (string tenantId, string instanceId, int year, string descriptorMappingId, EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest = null)

Updates a Descriptor Mapping.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorMappingId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest** | [**EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest**](EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse.md)

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

