# EdGraph.Platform.Client.Api.ConnectionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ConnectionTestedResponse**](ConnectionsApi.md#connectiontestedresponse) | **POST** /tenants/{tenantId}/datasync/connections/testconnection | Tests availability of provided connection metadata. |
| [**CreateEdFiConnection**](ConnectionsApi.md#createedficonnection) | **POST** /tenants/{tenantId}/edfiadmin/connections | Creates a new Ed-Fi Connection. |
| [**CreateTenantDataSyncConnection**](ConnectionsApi.md#createtenantdatasyncconnection) | **POST** /tenants/{tenantId}/datasync/connections | Creates a new DataSync connection |
| [**DeleteEdFiConnection**](ConnectionsApi.md#deleteedficonnection) | **DELETE** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Deletes an Ed-Fi Connection. |
| [**DeleteTenantDataSyncConnection**](ConnectionsApi.md#deletetenantdatasyncconnection) | **DELETE** /tenants/{tenantId}/datasync/connections/{connectionId} | Delete a DataSync connection matching the primary key |
| [**GetAllTenantDataSyncConnections**](ConnectionsApi.md#getalltenantdatasyncconnections) | **GET** /tenants/{tenantId}/datasync/connections | Retrieves a list of DataSync Connections |
| [**GetConnectionById**](ConnectionsApi.md#getconnectionbyid) | **GET** /tenants/{tenantId}/oneroster/connections/{connectionId} | Retrieves the profile of a Connection. |
| [**GetEdFiConnectionById**](ConnectionsApi.md#getedficonnectionbyid) | **GET** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Retrieves an Ed-Fi Connection by ID. |
| [**GetEdFiConnectionsAsync**](ConnectionsApi.md#getedficonnectionsasync) | **GET** /tenants/{tenantId}/edfiadmin/connections | Retrieves a list of Ed-Fi Connections. |
| [**GetEdFiOdsBackupCodesDescriptorsAsync**](ConnectionsApi.md#getedfiodsbackupcodesdescriptorsasync) | **GET** /tenants/{tenantId}/edfiadmin/connections/odsbackupcodes | Retrieves a list of Ed-Fi ODS backup codes. |
| [**GetPagedConnections**](ConnectionsApi.md#getpagedconnections) | **GET** /tenants/{tenantId}/oneroster/connections | Retrieves a list of Connections. |
| [**GetTenantDataSyncConnectionProfileById**](ConnectionsApi.md#gettenantdatasyncconnectionprofilebyid) | **GET** /tenants/{tenantId}/datasync/connections/{connectionId} | Retrieves a specific DataSync connection using its primary key |
| [**TestConnectionDetailsAsync**](ConnectionsApi.md#testconnectiondetailsasync) | **POST** /tenants/{tenantId}/oneroster/connections/test | Tests the connection by sending the connection details in the request payload |
| [**TestConnectionDetailsByIdAsync**](ConnectionsApi.md#testconnectiondetailsbyidasync) | **POST** /tenants/{tenantId}/oneroster/connections/{connectionId}/test | Tests the connection by obtaining the details by ID |
| [**UpdateEdFiConnection**](ConnectionsApi.md#updateedficonnection) | **PUT** /tenants/{tenantId}/edfiadmin/connections/{connectionId} | Updates an Ed-Fi Connection. |
| [**UpdateTenantDataSyncConnection**](ConnectionsApi.md#updatetenantdatasyncconnection) | **PUT** /tenants/{tenantId}/datasync/connections/{connectionId} | Updates a DataSync connection matching the primary key |

<a id="connectiontestedresponse"></a>
# **ConnectionTestedResponse**
> DataSyncApiConnectionV1ConnectionTestedResponse ConnectionTestedResponse (string tenantId, DataSyncApiConnectionV1TestConnectionRequest dataSyncApiConnectionV1TestConnectionRequest = null)

Tests availability of provided connection metadata.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **dataSyncApiConnectionV1TestConnectionRequest** | [**DataSyncApiConnectionV1TestConnectionRequest**](DataSyncApiConnectionV1TestConnectionRequest.md) |  | [optional]  |

### Return type

[**DataSyncApiConnectionV1ConnectionTestedResponse**](DataSyncApiConnectionV1ConnectionTestedResponse.md)

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

<a id="createedficonnection"></a>
# **CreateEdFiConnection**
> void CreateEdFiConnection (Guid tenantId, EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest edfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest = null)

Creates a new Ed-Fi Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest** | [**EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest**](EdfiAdminApiEdfiAdminV1CreateEdFiConnectionRequest.md) |  | [optional]  |

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

<a id="createtenantdatasyncconnection"></a>
# **CreateTenantDataSyncConnection**
> void CreateTenantDataSyncConnection (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest = null)

Creates a new DataSync connection


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsCreateConnectionRequest.md) |  | [optional]  |

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteedficonnection"></a>
# **DeleteEdFiConnection**
> EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse DeleteEdFiConnection (string tenantId, string connectionId)

Deletes an Ed-Fi Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse**](EdfiAdminApiEdfiAdminV1EdFiConnectionDeletedResponse.md)

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

<a id="deletetenantdatasyncconnection"></a>
# **DeleteTenantDataSyncConnection**
> void DeleteTenantDataSyncConnection (string tenantId, string connectionId)

Delete a DataSync connection matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

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

<a id="getalltenantdatasyncconnections"></a>
# **GetAllTenantDataSyncConnections**
> DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel GetAllTenantDataSyncConnections (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of DataSync Connections


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel**](DataSyncApiConnectionV1ConnectionListResponsePaginatedItemsViewModel.md)

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

<a id="getconnectionbyid"></a>
# **GetConnectionById**
> IMSAdminApiV1ConnectionsPagedConnectionsResponse GetConnectionById (string tenantId, string connectionId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves the profile of a Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IMSAdminApiV1ConnectionsPagedConnectionsResponse**](IMSAdminApiV1ConnectionsPagedConnectionsResponse.md)

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

<a id="getedficonnectionbyid"></a>
# **GetEdFiConnectionById**
> EdfiAdminApiEdfiAdminV1EdFiConnection GetEdFiConnectionById (Guid tenantId, Guid connectionId)

Retrieves an Ed-Fi Connection by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiConnection**](EdfiAdminApiEdfiAdminV1EdFiConnection.md)

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

<a id="getedficonnectionsasync"></a>
# **GetEdFiConnectionsAsync**
> EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse GetEdFiConnectionsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Ed-Fi Connections.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1EdFiConnectionPaginatedItemsResponse.md)

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

<a id="getedfiodsbackupcodesdescriptorsasync"></a>
# **GetEdFiOdsBackupCodesDescriptorsAsync**
> EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse GetEdFiOdsBackupCodesDescriptorsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Ed-Fi ODS backup codes.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1EdFiOdsBackupDescriptorsPaginatedItemsResponse.md)

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

<a id="getpagedconnections"></a>
# **GetPagedConnections**
> IMSAdminApiV1ConnectionsPagedConnectionsResponse GetPagedConnections (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Connections.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IMSAdminApiV1ConnectionsPagedConnectionsResponse**](IMSAdminApiV1ConnectionsPagedConnectionsResponse.md)

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

<a id="gettenantdatasyncconnectionprofilebyid"></a>
# **GetTenantDataSyncConnectionProfileById**
> DataSyncApiConnectionV1ConnectionProfileResponse GetTenantDataSyncConnectionProfileById (string tenantId, string connectionId)

Retrieves a specific DataSync connection using its primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**DataSyncApiConnectionV1ConnectionProfileResponse**](DataSyncApiConnectionV1ConnectionProfileResponse.md)

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

<a id="testconnectiondetailsasync"></a>
# **TestConnectionDetailsAsync**
> IMSAdminApiV1ConnectionsConnectionTestedResponse TestConnectionDetailsAsync (string tenantId, IMSAdminApiV1ConnectionsTestConnectionDetailsRequest iMSAdminApiV1ConnectionsTestConnectionDetailsRequest = null)

Tests the connection by sending the connection details in the request payload


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **iMSAdminApiV1ConnectionsTestConnectionDetailsRequest** | [**IMSAdminApiV1ConnectionsTestConnectionDetailsRequest**](IMSAdminApiV1ConnectionsTestConnectionDetailsRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ConnectionsConnectionTestedResponse**](IMSAdminApiV1ConnectionsConnectionTestedResponse.md)

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

<a id="testconnectiondetailsbyidasync"></a>
# **TestConnectionDetailsByIdAsync**
> IMSAdminApiV1ConnectionsConnectionTestedResponse TestConnectionDetailsByIdAsync (Guid tenantId, Guid connectionId, IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest iMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest = null)

Tests the connection by obtaining the details by ID


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |
| **iMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest** | [**IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest**](IMSAdminApiV1ConnectionsTestConnectionDetailsByIdRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ConnectionsConnectionTestedResponse**](IMSAdminApiV1ConnectionsConnectionTestedResponse.md)

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

<a id="updateedficonnection"></a>
# **UpdateEdFiConnection**
> EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse UpdateEdFiConnection (Guid tenantId, Guid connectionId, EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest edfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest = null)

Updates an Ed-Fi Connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest** | [**EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest**](EdfiAdminApiEdfiAdminV1UpdateEdFiConnectionRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse**](EdfiAdminApiEdfiAdminV1EdFiConnectionUpdatedResponse.md)

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

<a id="updatetenantdatasyncconnection"></a>
# **UpdateTenantDataSyncConnection**
> void UpdateTenantDataSyncConnection (string tenantId, string connectionId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest = null)

Updates a DataSync connection matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **connectionId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsConnectionsUpdateConnectionRequest.md) |  | [optional]  |

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

