# EdGraph.Platform.Client.Api.InstancesEducationOrganizationsEducationServiceCentersApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEducationServiceCenterAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#createeducationservicecenterasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters | Creates an EducationServiceCenter. |
| [**DeleteEducationServiceCenterAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#deleteeducationservicecenterasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Deletes an EducationServiceCenter. |
| [**GetEducationServiceCenterByIdAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#geteducationservicecenterbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Retrieves an EducationServiceCenter by ID. |
| [**UpdateEducationServiceCenterAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#updateeducationservicecenterasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Updates an EducationServiceCenter. |

<a id="createeducationservicecenterasync"></a>
# **CreateEducationServiceCenterAsync**
> EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse CreateEducationServiceCenterAsync (Guid tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest = null)

Creates an EducationServiceCenter.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest** | [**EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest**](EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse**](EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse.md)

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

<a id="deleteeducationservicecenterasync"></a>
# **DeleteEducationServiceCenterAsync**
> void DeleteEducationServiceCenterAsync (Guid tenantId, string instanceId, int year, Guid educationServiceCenterId)

Deletes an EducationServiceCenter.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **educationServiceCenterId** | **Guid** |  |  |

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

<a id="geteducationservicecenterbyidasync"></a>
# **GetEducationServiceCenterByIdAsync**
> EdfiAdminApiEdfiAdminV1EducationServiceCenter GetEducationServiceCenterByIdAsync (Guid tenantId, string instanceId, int year, Guid educationServiceCenterId)

Retrieves an EducationServiceCenter by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **educationServiceCenterId** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EducationServiceCenter**](EdfiAdminApiEdfiAdminV1EducationServiceCenter.md)

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

<a id="updateeducationservicecenterasync"></a>
# **UpdateEducationServiceCenterAsync**
> void UpdateEducationServiceCenterAsync (Guid tenantId, string instanceId, int year, Guid educationServiceCenterId, EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest = null)

Updates an EducationServiceCenter.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **educationServiceCenterId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest** | [**EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest**](EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest.md) |  | [optional]  |

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

