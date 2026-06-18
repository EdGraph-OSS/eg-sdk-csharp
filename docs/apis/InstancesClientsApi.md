# EdGraph.Platform.Client.Api.InstancesClientsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateClient**](InstancesClientsApi.md#createclient) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Creates a new client |
| [**DeleteClient**](InstancesClientsApi.md#deleteclient) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Deletes a client by Id |
| [**GetClientById**](InstancesClientsApi.md#getclientbyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Retrieves a client by Id |
| [**GetPagedClients**](InstancesClientsApi.md#getpagedclients) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Retrieves a list of clients for a given instance |
| [**UpdateClient**](InstancesClientsApi.md#updateclient) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Updates a client by Id |

<a id="createclient"></a>
# **CreateClient**
> IMSAdminApiV1ClientsClientCreatedResponse CreateClient (string tenantId, string instanceId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto = null)

Creates a new client


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientCreatedResponse**](IMSAdminApiV1ClientsClientCreatedResponse.md)

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

<a id="deleteclient"></a>
# **DeleteClient**
> IMSAdminApiV1ClientsClientDeletedResponse DeleteClient (string tenantId, string instanceId, string clientId)

Deletes a client by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |

### Return type

[**IMSAdminApiV1ClientsClientDeletedResponse**](IMSAdminApiV1ClientsClientDeletedResponse.md)

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

<a id="getclientbyid"></a>
# **GetClientById**
> IMSAdminApiV1ClientsClientProfileResponse GetClientById (string tenantId, string instanceId, string clientId)

Retrieves a client by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |

### Return type

[**IMSAdminApiV1ClientsClientProfileResponse**](IMSAdminApiV1ClientsClientProfileResponse.md)

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

<a id="getpagedclients"></a>
# **GetPagedClients**
> IMSAdminApiV1ClientsPaginatedItemsResponse GetPagedClients (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of clients for a given instance


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

[**IMSAdminApiV1ClientsPaginatedItemsResponse**](IMSAdminApiV1ClientsPaginatedItemsResponse.md)

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

<a id="updateclient"></a>
# **UpdateClient**
> IMSAdminApiV1ClientsClientUpdatedResponse UpdateClient (string tenantId, string instanceId, string clientId, IMSAdminApiV1ClientsUpdateClientRequest iMSAdminApiV1ClientsUpdateClientRequest = null)

Updates a client by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **iMSAdminApiV1ClientsUpdateClientRequest** | [**IMSAdminApiV1ClientsUpdateClientRequest**](IMSAdminApiV1ClientsUpdateClientRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientUpdatedResponse**](IMSAdminApiV1ClientsClientUpdatedResponse.md)

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

