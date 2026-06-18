# EdGraph.Platform.Client.Api.ConnectionsEdFiApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetTenantDataSyncConnectionEdFiDistricts**](ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfidistricts) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/districts | Retrieves a list of districts from an Ed-Fi API using the DataSync connection metadata |
| [**GetTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors**](ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfieducationorganizationiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/educationorganizationidentificationsystemdescriptors | Retrieves a list of education organization identification system descriptors from an Ed-Fi API using the DataSync connection metadata |
| [**GetTenantDataSyncConnectionEdFiSchoolYears**](ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfischoolyears) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/schoolyears | Retrieves a list of school years from an Ed-Fi API using the DataSync connection metadata |
| [**GetTenantDataSyncConnectionEdFiStaffIdDescriptors**](ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfistaffiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/staffidentificationsystemdescriptors | Retrieves a list of staff identification system descriptors from an Ed-Fi API using the DataSync connection metadata |
| [**GetTenantDataSyncConnectionEdFiStudentIdDescriptors**](ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfistudentiddescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/studentidentificationsystemdescriptors | Retrieves a list of student identification system descriptors from an Ed-Fi API using the DataSync connection metadata |
| [**GetTenantDataSyncConnectionEdFiTermDescriptors**](ConnectionsEdFiApi.md#gettenantdatasyncconnectionedfitermdescriptors) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId}/edfi/termdescriptors | Retrieves a list of term descriptors from an Ed-Fi API using the DataSync connection metadata |

<a id="gettenantdatasyncconnectionedfidistricts"></a>
# **GetTenantDataSyncConnectionEdFiDistricts**
> List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt; GetTenantDataSyncConnectionEdFiDistricts (string tenantId, string connectionId)

Retrieves a list of districts from an Ed-Fi API using the DataSync connection metadata


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt;**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

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

<a id="gettenantdatasyncconnectionedfieducationorganizationiddescriptors"></a>
# **GetTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors**
> List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt; GetTenantDataSyncConnectionEdFiEducationOrganizationIdDescriptors (string tenantId, string connectionId)

Retrieves a list of education organization identification system descriptors from an Ed-Fi API using the DataSync connection metadata


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt;**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

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

<a id="gettenantdatasyncconnectionedfischoolyears"></a>
# **GetTenantDataSyncConnectionEdFiSchoolYears**
> List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt; GetTenantDataSyncConnectionEdFiSchoolYears (string tenantId, string connectionId)

Retrieves a list of school years from an Ed-Fi API using the DataSync connection metadata


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt;**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

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

<a id="gettenantdatasyncconnectionedfistaffiddescriptors"></a>
# **GetTenantDataSyncConnectionEdFiStaffIdDescriptors**
> List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt; GetTenantDataSyncConnectionEdFiStaffIdDescriptors (string tenantId, string connectionId)

Retrieves a list of staff identification system descriptors from an Ed-Fi API using the DataSync connection metadata


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt;**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

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

<a id="gettenantdatasyncconnectionedfistudentiddescriptors"></a>
# **GetTenantDataSyncConnectionEdFiStudentIdDescriptors**
> List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt; GetTenantDataSyncConnectionEdFiStudentIdDescriptors (string tenantId, string connectionId)

Retrieves a list of student identification system descriptors from an Ed-Fi API using the DataSync connection metadata


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt;**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

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

<a id="gettenantdatasyncconnectionedfitermdescriptors"></a>
# **GetTenantDataSyncConnectionEdFiTermDescriptors**
> List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt; GetTenantDataSyncConnectionEdFiTermDescriptors (string tenantId, string connectionId)

Retrieves a list of term descriptors from an Ed-Fi API using the DataSync connection metadata


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**List&lt;EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse&gt;**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesConnectionEdFiResponse.md)

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

