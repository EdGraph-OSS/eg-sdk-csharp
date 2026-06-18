# EdGraph.Platform.Client.Api.InstancesEducationOrganizationsLocalEducationAgenciesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#createlocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Creates a LocalEducationAgency. |
| [**DeleteLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#deletelocaleducationagencyasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Deletes a LocalEducationAgency. |
| [**GetLocalEducationAgencyByIdAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getlocaleducationagencybyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Retrieves a LocalEducationAgency by ID. |
| [**GetlLocalEducationAgenciesAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getllocaleducationagenciesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Retrieves a list of LocalEducationAgencies. |
| [**SyncLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#synclocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId}/sync | Copies a LocalEducationAgency from one instance to another/other instance(s). |
| [**UpdateLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#updatelocaleducationagencyasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Updates a LocalEducationAgency. |

<a id="createlocaleducationagencyasync"></a>
# **CreateLocalEducationAgencyAsync**
> EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse CreateLocalEducationAgencyAsync (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest = null)

Creates a LocalEducationAgency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse**](EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse.md)

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

<a id="deletelocaleducationagencyasync"></a>
# **DeleteLocalEducationAgencyAsync**
> void DeleteLocalEducationAgencyAsync (string tenantId, string instanceId, int year, string localEducationAgencyId)

Deletes a LocalEducationAgency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **localEducationAgencyId** | **string** |  |  |

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

<a id="getlocaleducationagencybyidasync"></a>
# **GetLocalEducationAgencyByIdAsync**
> EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse GetLocalEducationAgencyByIdAsync (string tenantId, string instanceId, int year, string localEducationAgencyId)

Retrieves a LocalEducationAgency by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **localEducationAgencyId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse**](EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse.md)

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

<a id="getllocaleducationagenciesasync"></a>
# **GetlLocalEducationAgenciesAsync**
> EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel GetlLocalEducationAgenciesAsync (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of LocalEducationAgencies.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel.md)

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

<a id="synclocaleducationagencyasync"></a>
# **SyncLocalEducationAgencyAsync**
> EdfiAdminApiEdfiAdminV1SyncResponse SyncLocalEducationAgencyAsync (string tenantId, string instanceId, int year, int localEducationAgencyId, EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest = null)

Copies a LocalEducationAgency from one instance to another/other instance(s).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **localEducationAgencyId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SyncResponse**](EdfiAdminApiEdfiAdminV1SyncResponse.md)

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

<a id="updatelocaleducationagencyasync"></a>
# **UpdateLocalEducationAgencyAsync**
> void UpdateLocalEducationAgencyAsync (string tenantId, string instanceId, int year, string localEducationAgencyId, EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest = null)

Updates a LocalEducationAgency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **localEducationAgencyId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest.md) |  | [optional]  |

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

