# EdGraph.Platform.Client.Api.TenantDslApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDslSync**](TenantDslApi.md#createdslsync) | **POST** /tenants/{tenantId}/jobs/dsl | Creates a DSL Sync Job for a given tenant |
| [**ExecuteDslSyncJob**](TenantDslApi.md#executedslsyncjob) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId}/execute | Executes a DSL Sync Job for a given tenant |
| [**GetDslSyncData**](TenantDslApi.md#getdslsyncdata) | **GET** /tenants/{tenantId}/jobs/dsl/{jobId} | Retrieves a DSL jobs profile for a given tenant |
| [**UpdateDslSync**](TenantDslApi.md#updatedslsync) | **PUT** /tenants/{tenantId}/jobs/dsl/{jobId} | Updates a DSL Sync Job for a given tenant |

<a id="createdslsync"></a>
# **CreateDslSync**
> DataSyncApiDslV1JobCreatedResponse CreateDslSync (Guid tenantId, DataSyncApiDslV1CreateJobRequest dataSyncApiDslV1CreateJobRequest = null)

Creates a DSL Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateDslSyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantDslApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var dataSyncApiDslV1CreateJobRequest = new DataSyncApiDslV1CreateJobRequest(); // DataSyncApiDslV1CreateJobRequest |  (optional) 

            try
            {
                // Creates a DSL Sync Job for a given tenant
                DataSyncApiDslV1JobCreatedResponse result = apiInstance.CreateDslSync(tenantId, dataSyncApiDslV1CreateJobRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantDslApi.CreateDslSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDslSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a DSL Sync Job for a given tenant
    ApiResponse<DataSyncApiDslV1JobCreatedResponse> response = apiInstance.CreateDslSyncWithHttpInfo(tenantId, dataSyncApiDslV1CreateJobRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantDslApi.CreateDslSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **dataSyncApiDslV1CreateJobRequest** | [**DataSyncApiDslV1CreateJobRequest**](DataSyncApiDslV1CreateJobRequest.md) |  | [optional]  |

### Return type

[**DataSyncApiDslV1JobCreatedResponse**](DataSyncApiDslV1JobCreatedResponse.md)

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

<a id="executedslsyncjob"></a>
# **ExecuteDslSyncJob**
> DataSyncApiDslV1DslJobExecutedResponse ExecuteDslSyncJob (Guid tenantId, Guid jobId)

Executes a DSL Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ExecuteDslSyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantDslApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "jobId_example";  // Guid | 

            try
            {
                // Executes a DSL Sync Job for a given tenant
                DataSyncApiDslV1DslJobExecutedResponse result = apiInstance.ExecuteDslSyncJob(tenantId, jobId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantDslApi.ExecuteDslSyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExecuteDslSyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Executes a DSL Sync Job for a given tenant
    ApiResponse<DataSyncApiDslV1DslJobExecutedResponse> response = apiInstance.ExecuteDslSyncJobWithHttpInfo(tenantId, jobId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantDslApi.ExecuteDslSyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |

### Return type

[**DataSyncApiDslV1DslJobExecutedResponse**](DataSyncApiDslV1DslJobExecutedResponse.md)

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

<a id="getdslsyncdata"></a>
# **GetDslSyncData**
> DataSyncApiDslV1DslProfile GetDslSyncData (Guid tenantId, Guid jobId)

Retrieves a DSL jobs profile for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetDslSyncDataExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantDslApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "jobId_example";  // Guid | 

            try
            {
                // Retrieves a DSL jobs profile for a given tenant
                DataSyncApiDslV1DslProfile result = apiInstance.GetDslSyncData(tenantId, jobId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantDslApi.GetDslSyncData: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDslSyncDataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a DSL jobs profile for a given tenant
    ApiResponse<DataSyncApiDslV1DslProfile> response = apiInstance.GetDslSyncDataWithHttpInfo(tenantId, jobId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantDslApi.GetDslSyncDataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |

### Return type

[**DataSyncApiDslV1DslProfile**](DataSyncApiDslV1DslProfile.md)

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

<a id="updatedslsync"></a>
# **UpdateDslSync**
> Object UpdateDslSync (Guid tenantId, Guid jobId, DataSyncApiDslV1UpdateJobRequest dataSyncApiDslV1UpdateJobRequest = null)

Updates a DSL Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateDslSyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantDslApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var jobId = "jobId_example";  // Guid | 
            var dataSyncApiDslV1UpdateJobRequest = new DataSyncApiDslV1UpdateJobRequest(); // DataSyncApiDslV1UpdateJobRequest |  (optional) 

            try
            {
                // Updates a DSL Sync Job for a given tenant
                Object result = apiInstance.UpdateDslSync(tenantId, jobId, dataSyncApiDslV1UpdateJobRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantDslApi.UpdateDslSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDslSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a DSL Sync Job for a given tenant
    ApiResponse<Object> response = apiInstance.UpdateDslSyncWithHttpInfo(tenantId, jobId, dataSyncApiDslV1UpdateJobRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantDslApi.UpdateDslSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |
| **dataSyncApiDslV1UpdateJobRequest** | [**DataSyncApiDslV1UpdateJobRequest**](DataSyncApiDslV1UpdateJobRequest.md) |  | [optional]  |

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **204** | The resource was successfully updated. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

