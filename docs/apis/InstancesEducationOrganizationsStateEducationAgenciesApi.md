# EdGraph.Platform.Client.Api.InstancesEducationOrganizationsStateEducationAgenciesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateStateEducationAgencyAsync**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#createstateeducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies | Creates a StateEducationAgency. |
| [**DeleteStateEducationAgencyAsync**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#deletestateeducationagencyasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Deletes a StateEducationAgency. |
| [**GetStateEducationAgencyByIdAsync**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#getstateeducationagencybyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Retrieves a StateEducationAgency by ID. |
| [**UpdateStateEducationAgencyAsync**](InstancesEducationOrganizationsStateEducationAgenciesApi.md#updatestateeducationagencyasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/stateeducationagencies/{stateEducationAgencyId} | Updates a StateEducationAgency. |

<a id="createstateeducationagencyasync"></a>
# **CreateStateEducationAgencyAsync**
> EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse CreateStateEducationAgencyAsync (Guid tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest edfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest = null)

Creates a StateEducationAgency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1CreateStateEducationAgencyRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse**](EdfiAdminApiEdfiAdminV1StateEducationAgencyCreatedResponse.md)

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

<a id="deletestateeducationagencyasync"></a>
# **DeleteStateEducationAgencyAsync**
> void DeleteStateEducationAgencyAsync (Guid tenantId, string instanceId, int year, Guid stateEducationAgencyId)

Deletes a StateEducationAgency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **stateEducationAgencyId** | **Guid** |  |  |

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

<a id="getstateeducationagencybyidasync"></a>
# **GetStateEducationAgencyByIdAsync**
> EdfiAdminApiEdfiAdminV1StateEducationAgency GetStateEducationAgencyByIdAsync (Guid tenantId, string instanceId, int year, Guid stateEducationAgencyId)

Retrieves a StateEducationAgency by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **stateEducationAgencyId** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1StateEducationAgency**](EdfiAdminApiEdfiAdminV1StateEducationAgency.md)

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

<a id="updatestateeducationagencyasync"></a>
# **UpdateStateEducationAgencyAsync**
> void UpdateStateEducationAgencyAsync (Guid tenantId, string instanceId, int year, Guid stateEducationAgencyId, EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest edfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest = null)

Updates a StateEducationAgency.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **stateEducationAgencyId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1UpdateStateEducationAgencyRequest.md) |  | [optional]  |

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

