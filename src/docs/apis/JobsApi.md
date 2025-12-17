# EdGraph.Platform.Client.Api.JobsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelJob**](JobsApi.md#canceljob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/cancel | Requests a Job cancellation. |
| [**CreateJob**](JobsApi.md#createjob) | **POST** /tenants/{tenantId}/validations/jobs | Creates a Job. |
| [**DeleteJob**](JobsApi.md#deletejob) | **DELETE** /tenants/{tenantId}/validations/jobs/{jobId} | Deletes a Job. |
| [**ExecuteJob**](JobsApi.md#executejob) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/execute | Requests a Job execution. |
| [**GetJobById**](JobsApi.md#getjobbyid) | **GET** /tenants/{tenantId}/validations/jobs/{jobId} | Retrieves a Job by ID. |
| [**GetJobs**](JobsApi.md#getjobs) | **GET** /tenants/{tenantId}/validations/jobs | Retrieves a list of Jobs. |
| [**RestartJobSchedule**](JobsApi.md#restartjobschedule) | **POST** /tenants/{tenantId}/validations/jobs/{jobId}/restart | Requests a Job schedule restart. |
| [**UpdateJob**](JobsApi.md#updatejob) | **PUT** /tenants/{tenantId}/validations/jobs/{jobId} | Updates a Job. |

<a id="canceljob"></a>
# **CancelJob**
> Object CancelJob (string tenantId, string jobId)

Requests a Job cancellation.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CancelJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var jobId = "jobId_example";  // string | 

            try
            {
                // Requests a Job cancellation.
                Object result = apiInstance.CancelJob(tenantId, jobId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.CancelJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Requests a Job cancellation.
    ApiResponse<Object> response = apiInstance.CancelJobWithHttpInfo(tenantId, jobId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.CancelJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="createjob"></a>
# **CreateJob**
> ValidationsApiCoreV1CreatedResponse CreateJob (Guid tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest = null)

Creates a Job.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest |  (optional) 

            try
            {
                // Creates a Job.
                ValidationsApiCoreV1CreatedResponse result = apiInstance.CreateJob(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.CreateJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a Job.
    ApiResponse<ValidationsApiCoreV1CreatedResponse> response = apiInstance.CreateJobWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsValidationsCreateValidationJobRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.CreateJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="deletejob"></a>
# **DeleteJob**
> void DeleteJob (Guid tenantId, string jobId)

Deletes a Job.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "jobId_example";  // string | 

            try
            {
                // Deletes a Job.
                apiInstance.DeleteJob(tenantId, jobId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.DeleteJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Job.
    apiInstance.DeleteJobWithHttpInfo(tenantId, jobId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.DeleteJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="executejob"></a>
# **ExecuteJob**
> Object ExecuteJob (Guid tenantId, string jobId)

Requests a Job execution.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ExecuteJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "jobId_example";  // string | 

            try
            {
                // Requests a Job execution.
                Object result = apiInstance.ExecuteJob(tenantId, jobId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.ExecuteJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExecuteJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Requests a Job execution.
    ApiResponse<Object> response = apiInstance.ExecuteJobWithHttpInfo(tenantId, jobId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.ExecuteJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="getjobbyid"></a>
# **GetJobById**
> ValidationsApiJobsV1JobProfileResponse GetJobById (string tenantId, string jobId)

Retrieves a Job by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetJobByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var jobId = "jobId_example";  // string | 

            try
            {
                // Retrieves a Job by ID.
                ValidationsApiJobsV1JobProfileResponse result = apiInstance.GetJobById(tenantId, jobId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.GetJobById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetJobByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Job by ID.
    ApiResponse<ValidationsApiJobsV1JobProfileResponse> response = apiInstance.GetJobByIdWithHttpInfo(tenantId, jobId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.GetJobByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetJobsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "filter_example";  // string |  (optional) 
            var orderBy = "orderBy_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Jobs.
                ValidationsApiJobsV1PaginatedItemsResponse result = apiInstance.GetJobs(tenantId, pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.GetJobs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetJobsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Jobs.
    ApiResponse<ValidationsApiJobsV1PaginatedItemsResponse> response = apiInstance.GetJobsWithHttpInfo(tenantId, pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.GetJobsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="restartjobschedule"></a>
# **RestartJobSchedule**
> void RestartJobSchedule (string tenantId, string jobId)

Requests a Job schedule restart.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RestartJobScheduleExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var jobId = "jobId_example";  // string | 

            try
            {
                // Requests a Job schedule restart.
                apiInstance.RestartJobSchedule(tenantId, jobId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.RestartJobSchedule: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RestartJobScheduleWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Requests a Job schedule restart.
    apiInstance.RestartJobScheduleWithHttpInfo(tenantId, jobId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.RestartJobScheduleWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "jobId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest |  (optional) 

            try
            {
                // Updates a Job.
                apiInstance.UpdateJob(tenantId, jobId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobsApi.UpdateJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Job.
    apiInstance.UpdateJobWithHttpInfo(tenantId, jobId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsJobsUpdateValidationJobRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobsApi.UpdateJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

