# EdGraph.Platform.Client.Api.InstancesApplicationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateApplicationAsync**](InstancesApplicationsApi.md#createapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Creates an Application. |
| [**CreateApplicationUserAccessAsync**](InstancesApplicationsApi.md#createapplicationuseraccessasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Creates a new application access. |
| [**DeleteApplicationAsync**](InstancesApplicationsApi.md#deleteapplicationasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Deletes an Application. |
| [**DeleteApplicationUserAccessAsync**](InstancesApplicationsApi.md#deleteapplicationuseraccessasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Deletes an application user access. |
| [**GetApplicationAccessAsync**](InstancesApplicationsApi.md#getapplicationaccessasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Retrieves a list of application accesses. |
| [**GetApplicationAccessByIdAsync**](InstancesApplicationsApi.md#getapplicationaccessbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Retrieves an application access by ID. |
| [**GetApplicationApiClientByIdAsync**](InstancesApplicationsApi.md#getapplicationapiclientbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId} | Retrieves an API Client of an Application by ID. |
| [**GetApplicationApiClientsAsync**](InstancesApplicationsApi.md#getapplicationapiclientsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients | Retrieves the API Clients of an Application. |
| [**GetApplicationByIdAsync**](InstancesApplicationsApi.md#getapplicationbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Retrieves an Application by ID. |
| [**GetApplicationsAsync**](InstancesApplicationsApi.md#getapplicationsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Retrieves a list of Applications. |
| [**RegenerateApiClientSecretAsync**](InstancesApplicationsApi.md#regenerateapiclientsecretasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/regenerate | Regenerates the secret of an API Client. |
| [**RegenerateApplicationApiClientCredentials**](InstancesApplicationsApi.md#regenerateapplicationapiclientcredentials) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/regenerate | Regenerates an application&#39;s API Client Credentials |
| [**SyncApplicationAsync**](InstancesApplicationsApi.md#syncapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/sync | Copies an Application from one instance to another/other instance(s) |
| [**UpdateApplicationAsync**](InstancesApplicationsApi.md#updateapplicationasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Updates an Application. |
| [**UpdateApplicationUserAccessAsync**](InstancesApplicationsApi.md#updateapplicationuseraccessasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Updates a new application access. |

<a id="createapplicationasync"></a>
# **CreateApplicationAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse CreateApplicationAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest = null)

Creates an Application.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest** | [**EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest**](EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse**](EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse.md)

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

<a id="createapplicationuseraccessasync"></a>
# **CreateApplicationUserAccessAsync**
> void CreateApplicationUserAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest = null)

Creates a new application access.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest** | [**EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest**](EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest.md) |  | [optional]  |

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteapplicationasync"></a>
# **DeleteApplicationAsync**
> void DeleteApplicationAsync (string tenantId, string instanceId, int applicationId)

Deletes an Application.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |

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

<a id="deleteapplicationuseraccessasync"></a>
# **DeleteApplicationUserAccessAsync**
> void DeleteApplicationUserAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, string accessId)

Deletes an application user access.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **accessId** | **string** |  |  |

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

<a id="getapplicationaccessasync"></a>
# **GetApplicationAccessAsync**
> EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel GetApplicationAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of application accesses.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel**](EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel.md)

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

<a id="getapplicationaccessbyidasync"></a>
# **GetApplicationAccessByIdAsync**
> EdFiAdminApiApplicationAccessV1ApplicationAccessResponse GetApplicationAccessByIdAsync (string tenantId, string instanceId, int applicationId, int apiClientId, string accessId)

Retrieves an application access by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **apiClientId** | **int** |  |  |
| **accessId** | **string** |  |  |

### Return type

[**EdFiAdminApiApplicationAccessV1ApplicationAccessResponse**](EdFiAdminApiApplicationAccessV1ApplicationAccessResponse.md)

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

<a id="getapplicationapiclientbyidasync"></a>
# **GetApplicationApiClientByIdAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse GetApplicationApiClientByIdAsync (string tenantId, string instanceId, string applicationId, int apiClientId)

Retrieves an API Client of an Application by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse**](EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse.md)

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

<a id="getapplicationapiclientsasync"></a>
# **GetApplicationApiClientsAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel GetApplicationApiClientsAsync (string tenantId, string instanceId, string applicationId)

Retrieves the API Clients of an Application.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel.md)

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

<a id="getapplicationbyidasync"></a>
# **GetApplicationByIdAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse GetApplicationByIdAsync (string tenantId, string instanceId, int applicationId, int year = null, bool loadEducationOrganizations = null)

Retrieves an Application by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **year** | **int** |  | [optional]  |
| **loadEducationOrganizations** | **bool** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse**](EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse.md)

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

<a id="getapplicationsasync"></a>
# **GetApplicationsAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel GetApplicationsAsync (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Applications.


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

[**EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel.md)

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

<a id="regenerateapiclientsecretasync"></a>
# **RegenerateApiClientSecretAsync**
> EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse RegenerateApiClientSecretAsync (string tenantId, string instanceId, int applicationId, int apiClientId)

Regenerates the secret of an API Client.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **apiClientId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse**](EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse.md)

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

<a id="regenerateapplicationapiclientcredentials"></a>
# **RegenerateApplicationApiClientCredentials**
> EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse RegenerateApplicationApiClientCredentials (string tenantId, string instanceId, int applicationId)

Regenerates an application's API Client Credentials


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse**](EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse.md)

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

<a id="syncapplicationasync"></a>
# **SyncApplicationAsync**
> void SyncApplicationAsync (string tenantId, string instanceId, int applicationId, EdfiAdminApiEdfiAdminV1SyncApplicationRequest edfiAdminApiEdfiAdminV1SyncApplicationRequest = null)

Copies an Application from one instance to another/other instance(s)


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SyncApplicationRequest** | [**EdfiAdminApiEdfiAdminV1SyncApplicationRequest**](EdfiAdminApiEdfiAdminV1SyncApplicationRequest.md) |  | [optional]  |

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

<a id="updateapplicationasync"></a>
# **UpdateApplicationAsync**
> void UpdateApplicationAsync (string tenantId, string instanceId, string applicationId, EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest = null)

Updates an Application.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest** | [**EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest**](EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest.md) |  | [optional]  |

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

<a id="updateapplicationuseraccessasync"></a>
# **UpdateApplicationUserAccessAsync**
> void UpdateApplicationUserAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, string accessId, EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest = null)

Updates a new application access.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **accessId** | **string** |  |  |
| **edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest** | [**EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest**](EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest.md) |  | [optional]  |

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

