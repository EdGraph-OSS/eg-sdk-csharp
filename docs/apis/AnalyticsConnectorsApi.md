# EdGraph.Platform.Client.Api.AnalyticsConnectorsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateConnector**](AnalyticsConnectorsApi.md#createconnector) | **POST** /tenants/{tenantId}/analytics/connectors | Creates a new connector |
| [**DeleteConnector**](AnalyticsConnectorsApi.md#deleteconnector) | **DELETE** /tenants/{tenantId}/analytics/connectors/{connectorId} | Deletes a connector by Id |
| [**GetADLSGen2ConnectorById**](AnalyticsConnectorsApi.md#getadlsgen2connectorbyid) | **GET** /tenants/{tenantId}/analytics/connectors/{connectorId} | Retrieves a connector profile by Id |
| [**GetPaginatedConnectors**](AnalyticsConnectorsApi.md#getpaginatedconnectors) | **GET** /tenants/{tenantId}/analytics/connectors | Retrieves paginated connectors |
| [**UpdateConnector**](AnalyticsConnectorsApi.md#updateconnector) | **PUT** /tenants/{tenantId}/analytics/connectors/{connectorId} | Updates a connector by Id |

<a id="createconnector"></a>
# **CreateConnector**
> EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse CreateConnector (string tenantId, Object body = null)

Creates a new connector


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse**](EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeCreatedResponse.md)

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

<a id="deleteconnector"></a>
# **DeleteConnector**
> AnalyticsApiConnectorsV1ConnectorDeletedResponse DeleteConnector (string tenantId, string connectorId)

Deletes a connector by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectorId** | **string** |  |  |

### Return type

[**AnalyticsApiConnectorsV1ConnectorDeletedResponse**](AnalyticsApiConnectorsV1ConnectorDeletedResponse.md)

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

<a id="getadlsgen2connectorbyid"></a>
# **GetADLSGen2ConnectorById**
> EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO GetADLSGen2ConnectorById (string tenantId, string connectorId)

Retrieves a connector profile by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectorId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO**](EdGraphHttpAggregatorsTenantApiServicesConnectorsExtensionsADLSGen2ConnectorProfileDTO.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getpaginatedconnectors"></a>
# **GetPaginatedConnectors**
> EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse GetPaginatedConnectors (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves paginated connectors


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse**](EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorsPaginatedItemsResponse.md)

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

<a id="updateconnector"></a>
# **UpdateConnector**
> EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse UpdateConnector (string tenantId, string connectorId, Object body = null)

Updates a connector by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectorId** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse**](EdGraphHttpAggregatorsTenantApiServicesConnectorsResponsesConnectorByTypeUpdatedResponse.md)

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

