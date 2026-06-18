# EdGraph.Platform.Client.Api.JobsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ActivateTenantDataSyncJob**](JobsApi.md#activatetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/activate | Activate a DataSync job matching the primary key |
| [**CancelJob**](JobsApi.md#canceljob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/cancel | Requests a Job cancellation. |
| [**CancelTenantDataSyncJob**](JobsApi.md#canceltenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/cancel | Cancel a DataSync job matching the primary key |
| [**CreateJob**](JobsApi.md#createjob) | **POST** /tenants/{tenantId}/validations/jobs | Creates a Job. |
| [**CreateTenantDataSyncJob**](JobsApi.md#createtenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs | Creates a new DataSync job |
| [**DeactivateTenantDataSyncJob**](JobsApi.md#deactivatetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/deactivate | Deactivate a DataSync job matching the primary key |
| [**DeleteJob**](JobsApi.md#deletejob) | **DELETE** /tenants/{tenantId}/validations/jobs/{jobId} | Deletes a Job. |
| [**DeleteTenantDataSyncJob**](JobsApi.md#deletetenantdatasyncjob) | **DELETE** /tenants/{tenantId}/datasync/jobs/{jobId} | Delete a DataSync job matching the primary key |
| [**ExecuteJob**](JobsApi.md#executejob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/execute | Requests a Job execution. |
| [**ExecuteTenantDataSyncJob**](JobsApi.md#executetenantdatasyncjob) | **POST** /tenants/{tenantId}/datasync/jobs/{jobId}/execute | Execute a DataSync job matching the primary key |
| [**GetAllTenantDataSyncJobs**](JobsApi.md#getalltenantdatasyncjobs) | **GET** /tenants/{tenantId}/datasync/jobs | Retrieves a list of DataSync Jobs |
| [**GetJobById**](JobsApi.md#getjobbyid) | **GET** /tenants/{tenantId}/validations/jobs/{jobId} | Retrieves a Job by ID. |
| [**GetJobs**](JobsApi.md#getjobs) | **GET** /tenants/{tenantId}/validations/jobs | Retrieves a list of Jobs. |
| [**GetTenantDataSyncJobProfileById**](JobsApi.md#gettenantdatasyncjobprofilebyid) | **GET** /tenants/{tenantId}/datasync/jobs/{jobId} | Retrieves a specific DataSync job using its primary key |
| [**RestartJobSchedule**](JobsApi.md#restartjobschedule) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/restart | Requests a Job schedule restart. |
| [**UpdateJob**](JobsApi.md#updatejob) | **PUT** /tenants/{tenantId}/validations/jobs/{jobId} | Updates a Job. |
| [**UpdateTenantDataSyncJob**](JobsApi.md#updatetenantdatasyncjob) | **PUT** /tenants/{tenantId}/datasync/jobs/{jobId} | Updates a DataSync job matching the primary key |

<a id="activatetenantdatasyncjob"></a>
# **ActivateTenantDataSyncJob**
> void ActivateTenantDataSyncJob (string tenantId, string jobId, DataSyncApiJobV1ActivateJobRequest dataSyncApiJobV1ActivateJobRequest = null)

Activate a DataSync job matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **dataSyncApiJobV1ActivateJobRequest** | [**DataSyncApiJobV1ActivateJobRequest**](DataSyncApiJobV1ActivateJobRequest.md) |  | [optional]  |

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
| **202** | The request has been accepted for processing, but the processing is not yet complete. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="canceljob"></a>
# **CancelJob**
> Object CancelJob (string tenantId, string jobId)

Requests a Job cancellation.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |

### Return type

**Object**

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

<a id="canceltenantdatasyncjob"></a>
# **CancelTenantDataSyncJob**
> void CancelTenantDataSyncJob (string tenantId, string jobId, DataSyncApiJobV1CancelJobRequest dataSyncApiJobV1CancelJobRequest = null)

Cancel a DataSync job matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **dataSyncApiJobV1CancelJobRequest** | [**DataSyncApiJobV1CancelJobRequest**](DataSyncApiJobV1CancelJobRequest.md) |  | [optional]  |

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
| **202** | The request has been accepted for processing, but the processing is not yet complete. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createjob"></a>
# **CreateJob**
> ValidationsApiCoreV1CreatedResponse CreateJob (Guid tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest = null)

Creates a Job.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest.md) |  | [optional]  |

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createtenantdatasyncjob"></a>
# **CreateTenantDataSyncJob**
> void CreateTenantDataSyncJob (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest = null)

Creates a new DataSync job


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsCreateJobRequest.md) |  | [optional]  |

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

<a id="deactivatetenantdatasyncjob"></a>
# **DeactivateTenantDataSyncJob**
> void DeactivateTenantDataSyncJob (string tenantId, string jobId, DataSyncApiJobV1DeactivateJobRequest dataSyncApiJobV1DeactivateJobRequest = null)

Deactivate a DataSync job matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **dataSyncApiJobV1DeactivateJobRequest** | [**DataSyncApiJobV1DeactivateJobRequest**](DataSyncApiJobV1DeactivateJobRequest.md) |  | [optional]  |

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
| **202** | The request has been accepted for processing, but the processing is not yet complete. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletejob"></a>
# **DeleteJob**
> void DeleteJob (Guid tenantId, string jobId)

Deletes a Job.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **string** |  |  |

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

<a id="deletetenantdatasyncjob"></a>
# **DeleteTenantDataSyncJob**
> void DeleteTenantDataSyncJob (string tenantId, string jobId)

Delete a DataSync job matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |

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

<a id="executejob"></a>
# **ExecuteJob**
> Object ExecuteJob (Guid tenantId, string jobId)

Requests a Job execution.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **string** |  |  |

### Return type

**Object**

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

<a id="executetenantdatasyncjob"></a>
# **ExecuteTenantDataSyncJob**
> void ExecuteTenantDataSyncJob (string tenantId, string jobId, DataSyncApiJobV1ExecuteJobRequest dataSyncApiJobV1ExecuteJobRequest = null)

Execute a DataSync job matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **dataSyncApiJobV1ExecuteJobRequest** | [**DataSyncApiJobV1ExecuteJobRequest**](DataSyncApiJobV1ExecuteJobRequest.md) |  | [optional]  |

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
| **202** | The request has been accepted for processing, but the processing is not yet complete. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getalltenantdatasyncjobs"></a>
# **GetAllTenantDataSyncJobs**
> DataSyncApiJobV1JobListResponsePaginatedItemsViewModel GetAllTenantDataSyncJobs (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of DataSync Jobs


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**DataSyncApiJobV1JobListResponsePaginatedItemsViewModel**](DataSyncApiJobV1JobListResponsePaginatedItemsViewModel.md)

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

<a id="getjobbyid"></a>
# **GetJobById**
> ValidationsApiJobsV1JobProfileResponse GetJobById (string tenantId, string jobId)

Retrieves a Job by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |

### Return type

[**ValidationsApiJobsV1JobProfileResponse**](ValidationsApiJobsV1JobProfileResponse.md)

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

<a id="getjobs"></a>
# **GetJobs**
> ValidationsApiJobsV1PaginatedItemsResponse GetJobs (string tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Jobs.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**ValidationsApiJobsV1PaginatedItemsResponse**](ValidationsApiJobsV1PaginatedItemsResponse.md)

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

<a id="gettenantdatasyncjobprofilebyid"></a>
# **GetTenantDataSyncJobProfileById**
> DataSyncApiJobV1JobProfileResponse GetTenantDataSyncJobProfileById (string tenantId, string jobId)

Retrieves a specific DataSync job using its primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |

### Return type

[**DataSyncApiJobV1JobProfileResponse**](DataSyncApiJobV1JobProfileResponse.md)

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

<a id="restartjobschedule"></a>
# **RestartJobSchedule**
> void RestartJobSchedule (string tenantId, string jobId)

Requests a Job schedule restart.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |

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

<a id="updatejob"></a>
# **UpdateJob**
> void UpdateJob (Guid tenantId, Guid jobId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest = null)

Updates a Job.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest.md) |  | [optional]  |

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

<a id="updatetenantdatasyncjob"></a>
# **UpdateTenantDataSyncJob**
> void UpdateTenantDataSyncJob (string tenantId, string jobId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest = null)

Updates a DataSync job matching the primary key


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateJobRequest.md) |  | [optional]  |

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
| **202** | The request has been accepted for processing, but the processing is not yet complete. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

