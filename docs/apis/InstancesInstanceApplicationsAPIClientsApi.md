# EdGraph.Platform.Client.Api.InstancesInstanceApplicationsAPIClientsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateInstanceApiClient**](InstancesInstanceApplicationsAPIClientsApi.md#createinstanceapiclient) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Creates an Instance ApiClient |
| [**DeleteInstanceApiClient**](InstancesInstanceApplicationsAPIClientsApi.md#deleteinstanceapiclient) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Deletes an Instance ApiClient |
| [**GetInstanceApiClientById**](InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclientbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Retrieves an Instance ApiClient by ID. |
| [**GetInstanceApiClients**](InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclients) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Retrieves a paginated list of Instance ApiClients |
| [**UpdateInstanceApiClient**](InstancesInstanceApplicationsAPIClientsApi.md#updateinstanceapiclient) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Updates an Instance Application ApiClient |

<a id="createinstanceapiclient"></a>
# **CreateInstanceApiClient**
> EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse CreateInstanceApiClient (string tenantId, string instanceId, string applicationId, EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest = null)

Creates an Instance ApiClient


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest** | [**EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest**](EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse**](EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse.md)

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

<a id="deleteinstanceapiclient"></a>
# **DeleteInstanceApiClient**
> void DeleteInstanceApiClient (string tenantId, string instanceId, string applicationId, string apiClientId)

Deletes an Instance ApiClient


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |

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

<a id="getinstanceapiclientbyid"></a>
# **GetInstanceApiClientById**
> EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse GetInstanceApiClientById (string tenantId, string instanceId, string applicationId, string apiClientId)

Retrieves an Instance ApiClient by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse**](EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse.md)

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

<a id="getinstanceapiclients"></a>
# **GetInstanceApiClients**
> EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel GetInstanceApiClients (string tenantId, string instanceId, string applicationId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a paginated list of Instance ApiClients


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel.md)

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

<a id="updateinstanceapiclient"></a>
# **UpdateInstanceApiClient**
> EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse UpdateInstanceApiClient (string tenantId, string instanceId, string applicationId, string apiClientId, EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest = null)

Updates an Instance Application ApiClient


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest** | [**EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest**](EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse**](EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse.md)

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

