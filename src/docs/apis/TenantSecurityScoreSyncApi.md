# EdGraph.Platform.Client.Api.TenantSecurityScoreSyncApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#createsecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore | Creates an Security Score Sync Job for a given tenant |
| [**ExecuteSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#executesecurityscoresyncjob) | **POST** /tenants/{tenantId}/jobs/securityscore/execute | Executes an Security Score Sync Job |
| [**GetSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#getsecurityscoresyncjob) | **GET** /tenants/{tenantId}/jobs/securityscore | Retrieves a Security Score Sync Job for a given tenant |
| [**GetSecurityScoreSyncJobExecution**](TenantSecurityScoreSyncApi.md#getsecurityscoresyncjobexecution) | **GET** /tenants/{tenantId}/jobs/securityscore/{jobId}/executions/{jobExecutionId} | Retrieves a Security Score Sync Job Execution for a given tenant |
| [**UpdateSecurityScoreSyncJob**](TenantSecurityScoreSyncApi.md#updatesecurityscoresyncjob) | **PUT** /tenants/{tenantId}/jobs/securityscore | Updates a Security Score Sync for a given tenant |

<a id="createsecurityscoresyncjob"></a>
# **CreateSecurityScoreSyncJob**
> EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult CreateSecurityScoreSyncJob (string tenantId, EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest = null)

Creates an Security Score Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateSecurityScoreSyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantSecurityScoreSyncApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest = new EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest(); // EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest |  (optional) 

            try
            {
                // Creates an Security Score Sync Job for a given tenant
                EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult result = apiInstance.CreateSecurityScoreSyncJob(tenantId, edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantSecurityScoreSyncApi.CreateSecurityScoreSyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSecurityScoreSyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Security Score Sync Job for a given tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult> response = apiInstance.CreateSecurityScoreSyncJobWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantSecurityScoreSyncApi.CreateSecurityScoreSyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest** | [**EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest**](EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncCreateSecurityScoreSyncJobRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult**](EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncJobCreatedResult.md)

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

<a id="executesecurityscoresyncjob"></a>
# **ExecuteSecurityScoreSyncJob**
> void ExecuteSecurityScoreSyncJob (Guid tenantId)

Executes an Security Score Sync Job

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ExecuteSecurityScoreSyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantSecurityScoreSyncApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Executes an Security Score Sync Job
                apiInstance.ExecuteSecurityScoreSyncJob(tenantId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantSecurityScoreSyncApi.ExecuteSecurityScoreSyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExecuteSecurityScoreSyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Executes an Security Score Sync Job
    apiInstance.ExecuteSecurityScoreSyncJobWithHttpInfo(tenantId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantSecurityScoreSyncApi.ExecuteSecurityScoreSyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

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
| **202** | Accepted |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getsecurityscoresyncjob"></a>
# **GetSecurityScoreSyncJob**
> DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile GetSecurityScoreSyncJob (Guid tenantId)

Retrieves a Security Score Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetSecurityScoreSyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantSecurityScoreSyncApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Retrieves a Security Score Sync Job for a given tenant
                DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile result = apiInstance.GetSecurityScoreSyncJob(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantSecurityScoreSyncApi.GetSecurityScoreSyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSecurityScoreSyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Security Score Sync Job for a given tenant
    ApiResponse<DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile> response = apiInstance.GetSecurityScoreSyncJobWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantSecurityScoreSyncApi.GetSecurityScoreSyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile**](DataSyncApiSecurityScoreSyncV1SecurityScoreSyncProfile.md)

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

<a id="getsecurityscoresyncjobexecution"></a>
# **GetSecurityScoreSyncJobExecution**
> DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile GetSecurityScoreSyncJobExecution (Guid tenantId, Guid jobId, Guid jobExecutionId)

Retrieves a Security Score Sync Job Execution for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetSecurityScoreSyncJobExecutionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantSecurityScoreSyncApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "jobId_example";  // Guid | 
            var jobExecutionId = "jobExecutionId_example";  // Guid | 

            try
            {
                // Retrieves a Security Score Sync Job Execution for a given tenant
                DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile result = apiInstance.GetSecurityScoreSyncJobExecution(tenantId, jobId, jobExecutionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantSecurityScoreSyncApi.GetSecurityScoreSyncJobExecution: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSecurityScoreSyncJobExecutionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Security Score Sync Job Execution for a given tenant
    ApiResponse<DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile> response = apiInstance.GetSecurityScoreSyncJobExecutionWithHttpInfo(tenantId, jobId, jobExecutionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantSecurityScoreSyncApi.GetSecurityScoreSyncJobExecutionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |
| **jobExecutionId** | **Guid** |  |  |

### Return type

[**DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile**](DataSyncApiSecurityScoreSyncV1SecurityScoreSyncExecutionProfile.md)

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

<a id="updatesecurityscoresyncjob"></a>
# **UpdateSecurityScoreSyncJob**
> void UpdateSecurityScoreSyncJob (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest = null)

Updates a Security Score Sync for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateSecurityScoreSyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantSecurityScoreSyncApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest = new EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest(); // EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest |  (optional) 

            try
            {
                // Updates a Security Score Sync for a given tenant
                apiInstance.UpdateSecurityScoreSyncJob(tenantId, edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantSecurityScoreSyncApi.UpdateSecurityScoreSyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSecurityScoreSyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Security Score Sync for a given tenant
    apiInstance.UpdateSecurityScoreSyncJobWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantSecurityScoreSyncApi.UpdateSecurityScoreSyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest** | [**EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest**](EdGraphHttpAggregatorsTenantApiServicesSecurityScoreSyncUpdateSecurityScoreSyncJobRequest.md) |  | [optional]  |

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
| **204** | No Content |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

