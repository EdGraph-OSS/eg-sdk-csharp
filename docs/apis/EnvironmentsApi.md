# EdGraph.Platform.Client.Api.EnvironmentsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEnvironment**](EnvironmentsApi.md#createenvironment) | **POST** /tenants/{tenantId}/validations/environments | Creates an Environment. |
| [**CreateStateReportingEnvironment**](EnvironmentsApi.md#createstatereportingenvironment) | **POST** /tenants/{tenantId}/statereporting/environments | Creates a new Environment. |
| [**DeleteEnvironment**](EnvironmentsApi.md#deleteenvironment) | **DELETE** /tenants/{tenantId}/validations/environments/{environmentId} | Deletes an Environment. |
| [**DeleteStateReportingEnvironment**](EnvironmentsApi.md#deletestatereportingenvironment) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId} | Deletes an Environment. |
| [**GetEnvironmentById**](EnvironmentsApi.md#getenvironmentbyid) | **GET** /tenants/{tenantId}/validations/environments/{environmentId} | Retrieves an Environment by ID. |
| [**GetEnvironments**](EnvironmentsApi.md#getenvironments) | **GET** /tenants/{tenantId}/validations/environments | Retrieves a list of Environments. |
| [**GetStateReportingEnvironment**](EnvironmentsApi.md#getstatereportingenvironment) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId} | Retrieves an Environment by ID. |
| [**SearchStateReportingEnvironments**](EnvironmentsApi.md#searchstatereportingenvironments) | **GET** /tenants/{tenantId}/statereporting/environments | Retrieves a list of Environments. |
| [**TestEnvironmentConnection**](EnvironmentsApi.md#testenvironmentconnection) | **POST** /tenants/{tenantId}/validations/environments/testconnection | Tests if the provided connection string can establish a valid connection. |
| [**UpdateEnvironment**](EnvironmentsApi.md#updateenvironment) | **PUT** /tenants/{tenantId}/validations/environments/{environmentId} | Updates an Environment. |
| [**UpdateStateReportingEnvironment**](EnvironmentsApi.md#updatestatereportingenvironment) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId} | Updates an Environment. |

<a id="createenvironment"></a>
# **CreateEnvironment**
> ValidationsApiCoreV1CreatedResponse CreateEnvironment (string tenantId, ValidationsApiDbEnvironmentsV1CreateRequest validationsApiDbEnvironmentsV1CreateRequest = null)

Creates an Environment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **validationsApiDbEnvironmentsV1CreateRequest** | [**ValidationsApiDbEnvironmentsV1CreateRequest**](ValidationsApiDbEnvironmentsV1CreateRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiCoreV1CreatedResponse**](ValidationsApiCoreV1CreatedResponse.md)

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

<a id="createstatereportingenvironment"></a>
# **CreateStateReportingEnvironment**
> EdGraphServicesStateReportingV1EnvironmentCreatedResponse CreateStateReportingEnvironment (Guid tenantId, EdGraphServicesStateReportingV1CreateEnvironmentRequest edGraphServicesStateReportingV1CreateEnvironmentRequest = null)

Creates a new Environment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1CreateEnvironmentRequest** | [**EdGraphServicesStateReportingV1CreateEnvironmentRequest**](EdGraphServicesStateReportingV1CreateEnvironmentRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1EnvironmentCreatedResponse**](EdGraphServicesStateReportingV1EnvironmentCreatedResponse.md)

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

<a id="deleteenvironment"></a>
# **DeleteEnvironment**
> void DeleteEnvironment (string tenantId, string environmentId)

Deletes an Environment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **environmentId** | **string** |  |  |

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

<a id="deletestatereportingenvironment"></a>
# **DeleteStateReportingEnvironment**
> EdGraphServicesStateReportingV1EnvironmentDeletedResponse DeleteStateReportingEnvironment (Guid tenantId, Guid environmentId)

Deletes an Environment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1EnvironmentDeletedResponse**](EdGraphServicesStateReportingV1EnvironmentDeletedResponse.md)

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

<a id="getenvironmentbyid"></a>
# **GetEnvironmentById**
> ValidationsApiDbEnvironmentsV1DbEnvironmentDto GetEnvironmentById (string tenantId, string environmentId)

Retrieves an Environment by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **environmentId** | **string** |  |  |

### Return type

[**ValidationsApiDbEnvironmentsV1DbEnvironmentDto**](ValidationsApiDbEnvironmentsV1DbEnvironmentDto.md)

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

<a id="getenvironments"></a>
# **GetEnvironments**
> ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments GetEnvironments (string tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Environments.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments**](ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments.md)

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

<a id="getstatereportingenvironment"></a>
# **GetStateReportingEnvironment**
> EdGraphServicesStateReportingV1EnvironmentProfileResponse GetStateReportingEnvironment (Guid tenantId, Guid environmentId)

Retrieves an Environment by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1EnvironmentProfileResponse**](EdGraphServicesStateReportingV1EnvironmentProfileResponse.md)

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

<a id="searchstatereportingenvironments"></a>
# **SearchStateReportingEnvironments**
> EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse SearchStateReportingEnvironments (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of Environments.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional]  |
| **filter** | **string** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse**](EdGraphServicesStateReportingV1PaginatedEnvironmentsResponse.md)

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

<a id="testenvironmentconnection"></a>
# **TestEnvironmentConnection**
> ValidationsApiDbEnvironmentsV1TestConnectionResponse TestEnvironmentConnection (string tenantId, ValidationsApiDbEnvironmentsV1TestConnectionRequest validationsApiDbEnvironmentsV1TestConnectionRequest = null)

Tests if the provided connection string can establish a valid connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **validationsApiDbEnvironmentsV1TestConnectionRequest** | [**ValidationsApiDbEnvironmentsV1TestConnectionRequest**](ValidationsApiDbEnvironmentsV1TestConnectionRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiDbEnvironmentsV1TestConnectionResponse**](ValidationsApiDbEnvironmentsV1TestConnectionResponse.md)

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

<a id="updateenvironment"></a>
# **UpdateEnvironment**
> Object UpdateEnvironment (string tenantId, string environmentId, ValidationsApiDbEnvironmentsV1UpdateRequest validationsApiDbEnvironmentsV1UpdateRequest = null)

Updates an Environment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **environmentId** | **string** |  |  |
| **validationsApiDbEnvironmentsV1UpdateRequest** | [**ValidationsApiDbEnvironmentsV1UpdateRequest**](ValidationsApiDbEnvironmentsV1UpdateRequest.md) |  | [optional]  |

### Return type

**Object**

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

<a id="updatestatereportingenvironment"></a>
# **UpdateStateReportingEnvironment**
> EdGraphServicesStateReportingV1EnvironmentUpdatedResponse UpdateStateReportingEnvironment (Guid tenantId, Guid environmentId, EdGraphServicesStateReportingV1UpdateEnvironmentRequest edGraphServicesStateReportingV1UpdateEnvironmentRequest = null)

Updates an Environment.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1UpdateEnvironmentRequest** | [**EdGraphServicesStateReportingV1UpdateEnvironmentRequest**](EdGraphServicesStateReportingV1UpdateEnvironmentRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1EnvironmentUpdatedResponse**](EdGraphServicesStateReportingV1EnvironmentUpdatedResponse.md)

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

