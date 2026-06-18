# EdGraph.Platform.Client.Api.EnvironmentsConnectionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateStateReportingConnection**](EnvironmentsConnectionsApi.md#createstatereportingconnection) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Creates a new Connection. |
| [**DeleteStateReportingConnection**](EnvironmentsConnectionsApi.md#deletestatereportingconnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Deletes a Connection. |
| [**FindStateReportingConnections**](EnvironmentsConnectionsApi.md#findstatereportingconnections) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections | Retrieves a list of Connections. |
| [**GetStateReportingConnection**](EnvironmentsConnectionsApi.md#getstatereportingconnection) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Retrieves a Connection by ID. |
| [**TestStateReportingConnectionById**](EnvironmentsConnectionsApi.md#teststatereportingconnectionbyid) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId}/testconnection | Tests a Connection by ID. |
| [**TestStateReportingConnectionByType**](EnvironmentsConnectionsApi.md#teststatereportingconnectionbytype) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/testconnection | Tests a Connection by Type. |
| [**UpdateStateReportingConnection**](EnvironmentsConnectionsApi.md#updatestatereportingconnection) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connections/{connectionId} | Updates a Connection. |

<a id="createstatereportingconnection"></a>
# **CreateStateReportingConnection**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse CreateStateReportingConnection (Guid tenantId, Guid environmentId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = null)

Creates a new Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest** | [**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletestatereportingconnection"></a>
# **DeleteStateReportingConnection**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse DeleteStateReportingConnection (Guid tenantId, Guid environmentId, Guid connectionId)

Deletes a Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="findstatereportingconnections"></a>
# **FindStateReportingConnections**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse FindStateReportingConnections (string tenantId, Guid environmentId, string instanceType = null, string connectionType = null)

Retrieves a list of Connections.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **environmentId** | **Guid** |  |  |
| **instanceType** | **string** |  | [optional]  |
| **connectionType** | **string** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse.md)

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

<a id="getstatereportingconnection"></a>
# **GetStateReportingConnection**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse GetStateReportingConnection (Guid tenantId, Guid environmentId, Guid connectionId)

Retrieves a Connection by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse.md)

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

<a id="teststatereportingconnectionbyid"></a>
# **TestStateReportingConnectionById**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse TestStateReportingConnectionById (Guid tenantId, Guid environmentId, Guid connectionId)

Tests a Connection by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="teststatereportingconnectionbytype"></a>
# **TestStateReportingConnectionByType**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse TestStateReportingConnectionByType (Guid tenantId, Guid environmentId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest = null)

Tests a Connection by Type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest** | [**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatestatereportingconnection"></a>
# **UpdateStateReportingConnection**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse UpdateStateReportingConnection (Guid tenantId, Guid environmentId, Guid connectionId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest = null)

Updates a Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest** | [**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

