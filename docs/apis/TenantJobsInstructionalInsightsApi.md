# EdGraph.Platform.Client.Api.TenantJobsInstructionalInsightsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateInstructionalInsightsSecuritySyncJob**](TenantJobsInstructionalInsightsApi.md#createinstructionalinsightssecuritysyncjob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights | Creates an Instructional Insights Security Sync Job for a given tenant |
| [**ExecuteInstructionalInsightsSecuritySyncJob**](TenantJobsInstructionalInsightsApi.md#executeinstructionalinsightssecuritysyncjob) | **POST** /tenants/{tenantId}/jobs/instructionalinsights/execute | Executes an Instructional Insights Security Sync Job |
| [**GetInstructionalInsightsSecuritySyncJob**](TenantJobsInstructionalInsightsApi.md#getinstructionalinsightssecuritysyncjob) | **GET** /tenants/{tenantId}/jobs/instructionalinsights | Retrieves an Instructional Insights Security Sync Job for a given tenant |
| [**SearchInstructionalInsightsSecuritySyncJobExecutionLogs**](TenantJobsInstructionalInsightsApi.md#searchinstructionalinsightssecuritysyncjobexecutionlogs) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions/{executionId}/logs | Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution |
| [**SearchInstructionalInsightsSecuritySyncJobExecutions**](TenantJobsInstructionalInsightsApi.md#searchinstructionalinsightssecuritysyncjobexecutions) | **GET** /tenants/{tenantId}/jobs/instructionalinsights/executions | Searches Instructional Insights Security Sync Job Executions for a given tenant |
| [**UpdateInstructionalInsightsSecuritySyncJob**](TenantJobsInstructionalInsightsApi.md#updateinstructionalinsightssecuritysyncjob) | **PUT** /tenants/{tenantId}/jobs/instructionalinsights | Updates an Instructional Insights Security Sync Job for a given tenant |

<a id="createinstructionalinsightssecuritysyncjob"></a>
# **CreateInstructionalInsightsSecuritySyncJob**
> IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse CreateInstructionalInsightsSecuritySyncJob (string tenantId, IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest = null)

Creates an Instructional Insights Security Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateInstructionalInsightsSecuritySyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantJobsInstructionalInsightsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest = new IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest(); // IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest |  (optional) 

            try
            {
                // Creates an Instructional Insights Security Sync Job for a given tenant
                IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse result = apiInstance.CreateInstructionalInsightsSecuritySyncJob(tenantId, identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.CreateInstructionalInsightsSecuritySyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInstructionalInsightsSecuritySyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Instructional Insights Security Sync Job for a given tenant
    ApiResponse<IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse> response = apiInstance.CreateInstructionalInsightsSecuritySyncJobWithHttpInfo(tenantId, identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.CreateInstructionalInsightsSecuritySyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **identityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest** | [**IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest**](IdentityApiInstructionalInsightsV1CreateInstructionalInsightsSecuritySyncJobRequest.md) |  | [optional]  |

### Return type

[**IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse**](IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobCreatedResponse.md)

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

<a id="executeinstructionalinsightssecuritysyncjob"></a>
# **ExecuteInstructionalInsightsSecuritySyncJob**
> IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse ExecuteInstructionalInsightsSecuritySyncJob (Guid tenantId)

Executes an Instructional Insights Security Sync Job

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ExecuteInstructionalInsightsSecuritySyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantJobsInstructionalInsightsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Executes an Instructional Insights Security Sync Job
                IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse result = apiInstance.ExecuteInstructionalInsightsSecuritySyncJob(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.ExecuteInstructionalInsightsSecuritySyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExecuteInstructionalInsightsSecuritySyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Executes an Instructional Insights Security Sync Job
    ApiResponse<IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse> response = apiInstance.ExecuteInstructionalInsightsSecuritySyncJobWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.ExecuteInstructionalInsightsSecuritySyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse**](IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobExecutedResponse.md)

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
| **202** | The job execution was successfully requested. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getinstructionalinsightssecuritysyncjob"></a>
# **GetInstructionalInsightsSecuritySyncJob**
> IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse GetInstructionalInsightsSecuritySyncJob (Guid tenantId)

Retrieves an Instructional Insights Security Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstructionalInsightsSecuritySyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantJobsInstructionalInsightsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Retrieves an Instructional Insights Security Sync Job for a given tenant
                IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse result = apiInstance.GetInstructionalInsightsSecuritySyncJob(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.GetInstructionalInsightsSecuritySyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstructionalInsightsSecuritySyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an Instructional Insights Security Sync Job for a given tenant
    ApiResponse<IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse> response = apiInstance.GetInstructionalInsightsSecuritySyncJobWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.GetInstructionalInsightsSecuritySyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse**](IdentityApiInstructionalInsightsV1InstructionalInsightsSecuritySyncJobResponse.md)

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

<a id="searchinstructionalinsightssecuritysyncjobexecutionlogs"></a>
# **SearchInstructionalInsightsSecuritySyncJobExecutionLogs**
> IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse SearchInstructionalInsightsSecuritySyncJobExecutionLogs (Guid tenantId, Guid executionId, string jobId = null, int pageIndex = null, int pageSize = null, string orderBy = null, string level = null, string message = null)

Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchInstructionalInsightsSecuritySyncJobExecutionLogsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantJobsInstructionalInsightsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var executionId = "executionId_example";  // Guid | 
            var jobId = "\"\"";  // string |  (optional)  (default to "")
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var level = "\"\"";  // string |  (optional)  (default to "")
            var message = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution
                IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse result = apiInstance.SearchInstructionalInsightsSecuritySyncJobExecutionLogs(tenantId, executionId, jobId, pageIndex, pageSize, orderBy, level, message);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.SearchInstructionalInsightsSecuritySyncJobExecutionLogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchInstructionalInsightsSecuritySyncJobExecutionLogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches Instructional Insights Security Sync Job Execution Logs for a given tenant and execution
    ApiResponse<IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse> response = apiInstance.SearchInstructionalInsightsSecuritySyncJobExecutionLogsWithHttpInfo(tenantId, executionId, jobId, pageIndex, pageSize, orderBy, level, message);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.SearchInstructionalInsightsSecuritySyncJobExecutionLogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **executionId** | **Guid** |  |  |
| **jobId** | **string** |  | [optional] [default to &quot;&quot;] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **level** | **string** |  | [optional] [default to &quot;&quot;] |
| **message** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse**](IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionLogsResponse.md)

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

<a id="searchinstructionalinsightssecuritysyncjobexecutions"></a>
# **SearchInstructionalInsightsSecuritySyncJobExecutions**
> IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse SearchInstructionalInsightsSecuritySyncJobExecutions (Guid tenantId, string jobId = null, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Searches Instructional Insights Security Sync Job Executions for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchInstructionalInsightsSecuritySyncJobExecutionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantJobsInstructionalInsightsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "\"\"";  // string |  (optional)  (default to "")
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches Instructional Insights Security Sync Job Executions for a given tenant
                IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse result = apiInstance.SearchInstructionalInsightsSecuritySyncJobExecutions(tenantId, jobId, pageIndex, pageSize, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.SearchInstructionalInsightsSecuritySyncJobExecutions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchInstructionalInsightsSecuritySyncJobExecutionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches Instructional Insights Security Sync Job Executions for a given tenant
    ApiResponse<IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse> response = apiInstance.SearchInstructionalInsightsSecuritySyncJobExecutionsWithHttpInfo(tenantId, jobId, pageIndex, pageSize, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.SearchInstructionalInsightsSecuritySyncJobExecutionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **string** |  | [optional] [default to &quot;&quot;] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse**](IdentityApiInstructionalInsightsV1SearchInstructionalInsightsSecuritySyncJobExecutionsResponse.md)

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

<a id="updateinstructionalinsightssecuritysyncjob"></a>
# **UpdateInstructionalInsightsSecuritySyncJob**
> MicrosoftAspNetCoreMvcNoContentResult UpdateInstructionalInsightsSecuritySyncJob (Guid tenantId, IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest = null)

Updates an Instructional Insights Security Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateInstructionalInsightsSecuritySyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantJobsInstructionalInsightsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest = new IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest(); // IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest |  (optional) 

            try
            {
                // Updates an Instructional Insights Security Sync Job for a given tenant
                MicrosoftAspNetCoreMvcNoContentResult result = apiInstance.UpdateInstructionalInsightsSecuritySyncJob(tenantId, identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.UpdateInstructionalInsightsSecuritySyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateInstructionalInsightsSecuritySyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Instructional Insights Security Sync Job for a given tenant
    ApiResponse<MicrosoftAspNetCoreMvcNoContentResult> response = apiInstance.UpdateInstructionalInsightsSecuritySyncJobWithHttpInfo(tenantId, identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantJobsInstructionalInsightsApi.UpdateInstructionalInsightsSecuritySyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **identityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest** | [**IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest**](IdentityApiInstructionalInsightsV1UpdateInstructionalInsightsSecuritySyncJobRequest.md) |  | [optional]  |

### Return type

[**MicrosoftAspNetCoreMvcNoContentResult**](MicrosoftAspNetCoreMvcNoContentResult.md)

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
| **204** | The resource was successfully updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

