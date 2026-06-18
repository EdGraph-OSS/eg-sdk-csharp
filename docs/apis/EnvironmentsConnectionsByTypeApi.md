# EdGraph.Platform.Client.Api.EnvironmentsConnectionsByTypeApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOrUpdateStateReportingConnectionByType**](EnvironmentsConnectionsByTypeApi.md#createorupdatestatereportingconnectionbytype) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Creates or Update a Connection by ConnectionType. |
| [**DeleteStateReportingByTypeConnection**](EnvironmentsConnectionsByTypeApi.md#deletestatereportingbytypeconnection) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Deletes a Connection by Type |
| [**GetStateReportingConnectionByType**](EnvironmentsConnectionsByTypeApi.md#getstatereportingconnectionbytype) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/connectionsByType/{connectionType} | Retrieves a Connection by Type. |

<a id="createorupdatestatereportingconnectionbytype"></a>
# **CreateOrUpdateStateReportingConnectionByType**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse CreateOrUpdateStateReportingConnectionByType (Guid tenantId, Guid environmentId, string connectionType, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = null)

Creates or Update a Connection by ConnectionType.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **connectionType** | **string** |  |  |
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

<a id="deletestatereportingbytypeconnection"></a>
# **DeleteStateReportingByTypeConnection**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse DeleteStateReportingByTypeConnection (Guid tenantId, Guid environmentId, string connectionType)

Deletes a Connection by Type


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **connectionType** | **string** |  |  |

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

<a id="getstatereportingconnectionbytype"></a>
# **GetStateReportingConnectionByType**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse GetStateReportingConnectionByType (Guid tenantId, Guid environmentId, string connectionType)

Retrieves a Connection by Type.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **connectionType** | **string** |  |  |

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

