# EdGraph.Platform.Client.Api.InstancesInstanceApplicationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateInstanceApplication**](InstancesInstanceApplicationsApi.md#createinstanceapplication) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Creates an Instance Application |
| [**DeleteInstanceApplication**](InstancesInstanceApplicationsApi.md#deleteinstanceapplication) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Deletes an Instance Application |
| [**GetInstanceApplicationById**](InstancesInstanceApplicationsApi.md#getinstanceapplicationbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Retrieves an Instance Application by ID. |
| [**GetInstanceApplications**](InstancesInstanceApplicationsApi.md#getinstanceapplications) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications | Retrieves a paginated list of Instance applications |
| [**UpdateInstanceApplication**](InstancesInstanceApplicationsApi.md#updateinstanceapplication) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId} | Updates an Instance Application |

<a id="createinstanceapplication"></a>
# **CreateInstanceApplication**
> EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse CreateInstanceApplication (string tenantId, string instanceId, EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest edGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest = null)

Creates an Instance Application


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest** | [**EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest**](EdGraphHttpAggregatorsTenantApiServicesInstanceApplicationsUseCasesCreateTenantInstanceApplicationRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse**](EdfiAdminApiEdfiAdminV1InstanceApplicationCreatedResponse.md)

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

<a id="deleteinstanceapplication"></a>
# **DeleteInstanceApplication**
> void DeleteInstanceApplication (string tenantId, string instanceId, string applicationId)

Deletes an Instance Application


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |

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

<a id="getinstanceapplicationbyid"></a>
# **GetInstanceApplicationById**
> EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse GetInstanceApplicationById (string tenantId, string instanceId, string applicationId)

Retrieves an Instance Application by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse**](EdfiAdminApiEdfiAdminV1InstanceApplicationProfileResponse.md)

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

<a id="getinstanceapplications"></a>
# **GetInstanceApplications**
> EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel GetInstanceApplications (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a paginated list of Instance applications


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

[**EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1InstanceApplicationsListResponsePaginatedItemsViewModel.md)

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

<a id="updateinstanceapplication"></a>
# **UpdateInstanceApplication**
> EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse UpdateInstanceApplication (string tenantId, string instanceId, string applicationId, EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest edfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest = null)

Updates an Instance Application


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest** | [**EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest**](EdfiAdminApiEdfiAdminV1UpdateInstanceApplicationRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse**](EdfiAdminApiEdfiAdminV1InstanceApplicationUpdatedResponse.md)

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

