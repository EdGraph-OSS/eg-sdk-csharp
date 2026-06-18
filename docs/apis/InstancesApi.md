# EdGraph.Platform.Client.Api.InstancesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddRelatedInstances**](InstancesApi.md#addrelatedinstances) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/relatedinstances | Add related instances to root instance by Id |
| [**AddSchoolYear**](InstancesApi.md#addschoolyear) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years | Adds an ODS database to an Instance. |
| [**AddSchoolYearRange**](InstancesApi.md#addschoolyearrange) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/bulk | Adds multiple ODS databases to an instance. |
| [**ChangeInstanceDatabaseTierAsync**](InstancesApi.md#changeinstancedatabasetierasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/tiers | Changes the selected tier of an ODS database. |
| [**CloneInstanceAsync**](InstancesApi.md#cloneinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/clone | Clones an instance. |
| [**CreateInstance**](InstancesApi.md#createinstance) | **POST** /tenants/{tenantId}/oneroster/instances | Creates a new Instance. |
| [**CreateInstanceAsync**](InstancesApi.md#createinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances | Creates a new Instance. |
| [**DeleteInstance**](InstancesApi.md#deleteinstance) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId} | Deletes an Instance. |
| [**DeleteInstanceAsync**](InstancesApi.md#deleteinstanceasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Deletes an Instance. |
| [**DeleteSchoolYearAsync**](InstancesApi.md#deleteschoolyearasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year} | Removes an ODS database from an Instance. |
| [**GetEdFiAdminInstanceEndpoints**](InstancesApi.md#getedfiadmininstanceendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance. |
| [**GetEdFiAdminInstanceYearEndpoints**](InstancesApi.md#getedfiadmininstanceyearendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance. |
| [**GetInstanceById**](InstancesApi.md#getinstancebyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId} | Retrieves an Instance by ID. |
| [**GetInstanceByIdAsync**](InstancesApi.md#getinstancebyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Retrieves an Instance by ID. |
| [**GetInstanceCsvExport**](InstancesApi.md#getinstancecsvexport) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves an Instance by ID. |
| [**GetInstanceCsvExportV2**](InstancesApi.md#getinstancecsvexportv2) | **GET** /v2/tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format |
| [**GetInstanceEndpoints**](InstancesApi.md#getinstanceendpoints) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/endpoints | Retrieves the One Roster endpoint URLs of an Instance. |
| [**GetInstancesAsync**](InstancesApi.md#getinstancesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances | Retrieves a list of Instances. |
| [**GetPagedInstances**](InstancesApi.md#getpagedinstances) | **GET** /tenants/{tenantId}/oneroster/instances | Retrieves a list of Instances. |
| [**GetTenantInstancesV2**](InstancesApi.md#gettenantinstancesv2) | **GET** /v2/tenants/{tenantId}/instances | Get list of all instances for a tenant - V2 |
| [**IsInstanceCustomIdAvailable**](InstancesApi.md#isinstancecustomidavailable) | **GET** /tenants/{tenantId}/oneroster/instances/isinstancecustomidavailable/{customId} | Validate if instance is available |
| [**LoadApiMetadata**](InstancesApi.md#loadapimetadata) | **POST** /tenants/{tenantId}/edfiadmin/api-metadata | Loads connection metadata. |
| [**ResetInstance**](InstancesApi.md#resetinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/resetinstance | Resets an Instance. |
| [**ResetInstanceAsync**](InstancesApi.md#resetinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/resetinstance | Resets an Instance. |
| [**ResetInstanceCacheAsync**](InstancesApi.md#resetinstancecacheasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetcache | Resets the cache of an Instance and the specified ODS database. |
| [**ResetSchoolYearAsync**](InstancesApi.md#resetschoolyearasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetods | Resets the ODS database with the specified school year. |
| [**SetInstanceIsDefault**](InstancesApi.md#setinstanceisdefault) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/default | Updates the isDefault property for an instance |
| [**TestConnectionDetailsByInstanceIdAsync**](InstancesApi.md#testconnectiondetailsbyinstanceidasync) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/test | Tests the connection by obtaining the details by Instance ID |
| [**TestCredentialsConnection**](InstancesApi.md#testcredentialsconnection) | **POST** /tenants/{tenantId}/edfiadmin/testconnection | Tests availability of provided connection metadata. |
| [**TestInstanceConnection**](InstancesApi.md#testinstanceconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/testconnection | Tests the connection of the Instance. |
| [**TestInstanceYearConnection**](InstancesApi.md#testinstanceyearconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/testconnection | Tests the connection of the Instance. |
| [**TruncateInstance**](InstancesApi.md#truncateinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/truncate | Truncates the Instance&#39;s database |
| [**UpdateInstance**](InstancesApi.md#updateinstance) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId} | Updates an Instance. |
| [**UpdateInstanceAsync**](InstancesApi.md#updateinstanceasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Updates an Instance. |
| [**ValidateCustomIdAvailable**](InstancesApi.md#validatecustomidavailable) | **GET** /tenants/{tenantId}/edfiadmin/instances/validatecustomidavailable/{customId} | Validate if instance is available |

<a id="addrelatedinstances"></a>
# **AddRelatedInstances**
> EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse AddRelatedInstances (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest = null)

Add related instances to root instance by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest** | [**EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest**](EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse**](EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse.md)

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

<a id="addschoolyear"></a>
# **AddSchoolYear**
> void AddSchoolYear (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1AddSchoolYearRequest edfiAdminApiEdfiAdminV1AddSchoolYearRequest = null)

Adds an ODS database to an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1AddSchoolYearRequest** | [**EdfiAdminApiEdfiAdminV1AddSchoolYearRequest**](EdfiAdminApiEdfiAdminV1AddSchoolYearRequest.md) |  | [optional]  |

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

<a id="addschoolyearrange"></a>
# **AddSchoolYearRange**
> void AddSchoolYearRange (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest = null)

Adds multiple ODS databases to an instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest** | [**EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest**](EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest.md) |  | [optional]  |

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

<a id="changeinstancedatabasetierasync"></a>
# **ChangeInstanceDatabaseTierAsync**
> void ChangeInstanceDatabaseTierAsync (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest = null)

Changes the selected tier of an ODS database.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest** | [**EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest**](EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest.md) |  | [optional]  |

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

<a id="cloneinstanceasync"></a>
# **CloneInstanceAsync**
> EdfiAdminApiEdfiAdminV1CloneInstanceResponse CloneInstanceAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1CloneInstanceRequest edfiAdminApiEdfiAdminV1CloneInstanceRequest = null)

Clones an instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CloneInstanceRequest** | [**EdfiAdminApiEdfiAdminV1CloneInstanceRequest**](EdfiAdminApiEdfiAdminV1CloneInstanceRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1CloneInstanceResponse**](EdfiAdminApiEdfiAdminV1CloneInstanceResponse.md)

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

<a id="createinstance"></a>
# **CreateInstance**
> void CreateInstance (string tenantId, IMSAdminApiV1InstancesCreateInstanceRequest iMSAdminApiV1InstancesCreateInstanceRequest = null)

Creates a new Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **iMSAdminApiV1InstancesCreateInstanceRequest** | [**IMSAdminApiV1InstancesCreateInstanceRequest**](IMSAdminApiV1InstancesCreateInstanceRequest.md) |  | [optional]  |

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

<a id="createinstanceasync"></a>
# **CreateInstanceAsync**
> void CreateInstanceAsync (string tenantId, EdfiAdminApiEdfiAdminV1CreateInstanceRequest edfiAdminApiEdfiAdminV1CreateInstanceRequest = null)

Creates a new Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateInstanceRequest** | [**EdfiAdminApiEdfiAdminV1CreateInstanceRequest**](EdfiAdminApiEdfiAdminV1CreateInstanceRequest.md) |  | [optional]  |

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

<a id="deleteinstance"></a>
# **DeleteInstance**
> void DeleteInstance (string tenantId, string instanceId)

Deletes an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

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

<a id="deleteinstanceasync"></a>
# **DeleteInstanceAsync**
> void DeleteInstanceAsync (string tenantId, string instanceId)

Deletes an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

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

<a id="deleteschoolyearasync"></a>
# **DeleteSchoolYearAsync**
> void DeleteSchoolYearAsync (string tenantId, string instanceId, int year)

Removes an ODS database from an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getedfiadmininstanceendpoints"></a>
# **GetEdFiAdminInstanceEndpoints**
> EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse GetEdFiAdminInstanceEndpoints (string tenantId, string instanceId)

Retrieves the Ed-Fi API endpoint URLs of an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse**](EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)

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

<a id="getedfiadmininstanceyearendpoints"></a>
# **GetEdFiAdminInstanceYearEndpoints**
> EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse GetEdFiAdminInstanceYearEndpoints (string tenantId, string instanceId, int year)

Retrieves the Ed-Fi API endpoint URLs of an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse**](EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)

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

<a id="getinstancebyid"></a>
# **GetInstanceById**
> IMSAdminApiV1InstancesInstanceProfileResponse GetInstanceById (string tenantId, string instanceId)

Retrieves an Instance by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**IMSAdminApiV1InstancesInstanceProfileResponse**](IMSAdminApiV1InstancesInstanceProfileResponse.md)

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

<a id="getinstancebyidasync"></a>
# **GetInstanceByIdAsync**
> EdfiAdminApiEdfiAdminV1Instance GetInstanceByIdAsync (string tenantId, string instanceId)

Retrieves an Instance by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1Instance**](EdfiAdminApiEdfiAdminV1Instance.md)

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

<a id="getinstancecsvexport"></a>
# **GetInstanceCsvExport**
> IMSAdminApiV1InstancesGetInstanceCsvExportResponse GetInstanceCsvExport (string tenantId, string instanceId)

Retrieves an Instance by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**IMSAdminApiV1InstancesGetInstanceCsvExportResponse**](IMSAdminApiV1InstancesGetInstanceCsvExportResponse.md)

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

<a id="getinstancecsvexportv2"></a>
# **GetInstanceCsvExportV2**
> IMSAdminApiV1InstancesInstanceCsvExportedResponse GetInstanceCsvExportV2 (string tenantId, string instanceId)

Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**IMSAdminApiV1InstancesInstanceCsvExportedResponse**](IMSAdminApiV1InstancesInstanceCsvExportedResponse.md)

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

<a id="getinstanceendpoints"></a>
# **GetInstanceEndpoints**
> IMSAdminApiV1InstancesInstanceEndpointsResponse GetInstanceEndpoints (string tenantId, string instanceId)

Retrieves the One Roster endpoint URLs of an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**IMSAdminApiV1InstancesInstanceEndpointsResponse**](IMSAdminApiV1InstancesInstanceEndpointsResponse.md)

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

<a id="getinstancesasync"></a>
# **GetInstancesAsync**
> EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel GetInstancesAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, bool deleted = null, string targetTenantId = null)

Retrieves a list of Instances.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **deleted** | **bool** |  | [optional] [default to false] |
| **targetTenantId** | **string** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel.md)

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

<a id="getpagedinstances"></a>
# **GetPagedInstances**
> IMSAdminApiV1InstancesPagedInstancesResponse GetPagedInstances (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Instances.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IMSAdminApiV1InstancesPagedInstancesResponse**](IMSAdminApiV1InstancesPagedInstancesResponse.md)

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

<a id="gettenantinstancesv2"></a>
# **GetTenantInstancesV2**
> EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel GetTenantInstancesV2 (string tenantId, int pageSize = null, int pageIndex = null, string searchTerm = null, string type = null)

Get list of all instances for a tenant - V2


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **searchTerm** | **string** |  | [optional] [default to &quot;&quot;] |
| **type** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel.md)

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

<a id="isinstancecustomidavailable"></a>
# **IsInstanceCustomIdAvailable**
> bool IsInstanceCustomIdAvailable (string tenantId, string customId)

Validate if instance is available


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **customId** | **string** |  |  |

### Return type

**bool**

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

<a id="loadapimetadata"></a>
# **LoadApiMetadata**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult LoadApiMetadata (string tenantId, EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest edGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest = null)

Loads connection metadata.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest** | [**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsUseCasesEdFiApiMetadataRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult.md)

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

<a id="resetinstance"></a>
# **ResetInstance**
> IMSAdminApiV1InstancesInstanceResetResponse ResetInstance (string tenantId, string instanceId)

Resets an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**IMSAdminApiV1InstancesInstanceResetResponse**](IMSAdminApiV1InstancesInstanceResetResponse.md)

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

<a id="resetinstanceasync"></a>
# **ResetInstanceAsync**
> EdfiAdminApiEdfiAdminV1ResetInstanceResponse ResetInstanceAsync (string tenantId, string instanceId)

Resets an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1ResetInstanceResponse**](EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)

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

<a id="resetinstancecacheasync"></a>
# **ResetInstanceCacheAsync**
> EdfiAdminApiEdfiAdminV1ResetInstanceResponse ResetInstanceCacheAsync (string tenantId, string instanceId, int year)

Resets the cache of an Instance and the specified ODS database.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1ResetInstanceResponse**](EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)

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

<a id="resetschoolyearasync"></a>
# **ResetSchoolYearAsync**
> void ResetSchoolYearAsync (string tenantId, string instanceId, int year)

Resets the ODS database with the specified school year.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setinstanceisdefault"></a>
# **SetInstanceIsDefault**
> void SetInstanceIsDefault (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest = null)

Updates the isDefault property for an instance


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest** | [**EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest**](EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest.md) |  | [optional]  |

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

<a id="testconnectiondetailsbyinstanceidasync"></a>
# **TestConnectionDetailsByInstanceIdAsync**
> IMSAdminApiV1ConnectionsConnectionTestedResponse TestConnectionDetailsByInstanceIdAsync (Guid tenantId, Guid instanceId, IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest = null)

Tests the connection by obtaining the details by Instance ID


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest** | [**IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest**](IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest.md) |  | [optional]  |

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

<a id="testcredentialsconnection"></a>
# **TestCredentialsConnection**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse TestCredentialsConnection (string tenantId, Object body = null)

Tests availability of provided connection metadata.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse.md)

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

<a id="testinstanceconnection"></a>
# **TestInstanceConnection**
> EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse TestInstanceConnection (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest = null)

Tests the connection of the Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest** | [**EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest**](EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse**](EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)

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

<a id="testinstanceyearconnection"></a>
# **TestInstanceYearConnection**
> EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse TestInstanceYearConnection (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest = null)

Tests the connection of the Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1TestInstanceConnectionRequest** | [**EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest**](EdfiAdminApiEdfiAdminV1TestInstanceConnectionRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse**](EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)

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

<a id="truncateinstance"></a>
# **TruncateInstance**
> IMSAdminApiV1InstancesInstanceTruncatedResponse TruncateInstance (Guid tenantId, Guid instanceId)

Truncates the Instance's database


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |

### Return type

[**IMSAdminApiV1InstancesInstanceTruncatedResponse**](IMSAdminApiV1InstancesInstanceTruncatedResponse.md)

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

<a id="updateinstance"></a>
# **UpdateInstance**
> void UpdateInstance (string tenantId, string instanceId, IMSAdminApiV1InstancesUpdateInstanceRequest iMSAdminApiV1InstancesUpdateInstanceRequest = null)

Updates an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **iMSAdminApiV1InstancesUpdateInstanceRequest** | [**IMSAdminApiV1InstancesUpdateInstanceRequest**](IMSAdminApiV1InstancesUpdateInstanceRequest.md) |  | [optional]  |

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateinstanceasync"></a>
# **UpdateInstanceAsync**
> void UpdateInstanceAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1UpdateInstanceRequest edfiAdminApiEdfiAdminV1UpdateInstanceRequest = null)

Updates an Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateInstanceRequest** | [**EdfiAdminApiEdfiAdminV1UpdateInstanceRequest**](EdfiAdminApiEdfiAdminV1UpdateInstanceRequest.md) |  | [optional]  |

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="validatecustomidavailable"></a>
# **ValidateCustomIdAvailable**
> bool ValidateCustomIdAvailable (string tenantId, string customId)

Validate if instance is available


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **customId** | **string** |  |  |

### Return type

**bool**

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

