# EdGraph.Platform.Client.Api.ConnectionsDEPRECATEDApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#createstatereportingconnectionv1) | **POST** /tenants/{tenantId}/statereporting/connections | Creates a new Connection. |
| [**DeleteStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#deletestatereportingconnectionv1) | **DELETE** /tenants/{tenantId}/statereporting/connections/{connectionId} | Deletes a Connection. |
| [**FindStateReportingConnectionsV1**](ConnectionsDEPRECATEDApi.md#findstatereportingconnectionsv1) | **GET** /tenants/{tenantId}/statereporting/connections | Retrieves a list of Connections. |
| [**GetStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#getstatereportingconnectionv1) | **GET** /tenants/{tenantId}/statereporting/connections/{connectionId} | Retrieves a Connection by ID. |
| [**TestStateReportingConnectionByIdV1**](ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbyidv1) | **POST** /tenants/{tenantId}/statereporting/connections/{connectionId}/testconnection | Tests a Connection by ID. |
| [**TestStateReportingConnectionByTypeV1**](ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbytypev1) | **POST** /tenants/{tenantId}/statereporting/connections/testconnection | Tests a Connection by Type. |
| [**UpdateStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#updatestatereportingconnectionv1) | **PUT** /tenants/{tenantId}/statereporting/connections/{connectionId} | Updates a Connection. |

<a id="createstatereportingconnectionv1"></a>
# **CreateStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse CreateStateReportingConnectionV1 (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = null)

Creates a new Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
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

<a id="deletestatereportingconnectionv1"></a>
# **DeleteStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse DeleteStateReportingConnectionV1 (Guid tenantId, Guid connectionId)

Deletes a Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
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

<a id="findstatereportingconnectionsv1"></a>
# **FindStateReportingConnectionsV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse FindStateReportingConnectionsV1 (string tenantId, string instanceType = null, string connectionType = null)

Retrieves a list of Connections.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
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

<a id="getstatereportingconnectionv1"></a>
# **GetStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse GetStateReportingConnectionV1 (Guid tenantId, Guid connectionId)

Retrieves a Connection by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
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

<a id="teststatereportingconnectionbyidv1"></a>
# **TestStateReportingConnectionByIdV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse TestStateReportingConnectionByIdV1 (Guid tenantId, Guid connectionId)

Tests a Connection by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
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

<a id="teststatereportingconnectionbytypev1"></a>
# **TestStateReportingConnectionByTypeV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse TestStateReportingConnectionByTypeV1 (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest = null)

Tests a Connection by Type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
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

<a id="updatestatereportingconnectionv1"></a>
# **UpdateStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse UpdateStateReportingConnectionV1 (Guid tenantId, Guid connectionId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest = null)

Updates a Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
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

