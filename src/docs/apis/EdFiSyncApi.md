# EdGraph.Platform.Client.Api.EdFiSyncApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEdFiSync**](EdFiSyncApi.md#createedfisync) | **POST** /tenants/{tenantId}/jobs/edfisync | Creates an Ed-Fi Sync Job for a given tenant |
| [**ExecuteEdFiSyncJob**](EdFiSyncApi.md#executeedfisyncjob) | **PUT** /tenants/{tenantId}/jobs/edfisync/execute | Executes an Ed-Fi Sync Job |
| [**GetEdFiSyncData**](EdFiSyncApi.md#getedfisyncdata) | **GET** /tenants/{tenantId}/jobs/edfisync | Retrieves Ed-Fi Sync Connection Data for a given tenant |
| [**UpdateEdFiSync**](EdFiSyncApi.md#updateedfisync) | **PUT** /tenants/{tenantId}/jobs/edfisync | Updates an Ed-Fi Sync for a given tenant |

<a id="createedfisync"></a>
# **CreateEdFiSync**
> EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult CreateEdFiSync (string tenantId, EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto = null)

Creates an Ed-Fi Sync Job for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateEdFiSyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EdFiSyncApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto = new EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto(); // EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto |  (optional) 

            try
            {
                // Creates an Ed-Fi Sync Job for a given tenant
                EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult result = apiInstance.CreateEdFiSync(tenantId, edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EdFiSyncApi.CreateEdFiSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEdFiSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Ed-Fi Sync Job for a given tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult> response = apiInstance.CreateEdFiSyncWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EdFiSyncApi.CreateEdFiSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto** | [**EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto**](EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncCreateEdFiRosterSyncJobRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult**](EdGraphHttpAggregatorsTenantApiServicesEdFiRosterSyncJobCreatedResult.md)

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

<a id="executeedfisyncjob"></a>
# **ExecuteEdFiSyncJob**
> DataSyncApiJobV1JobExecutionRequestedResponse ExecuteEdFiSyncJob (Guid tenantId)

Executes an Ed-Fi Sync Job

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ExecuteEdFiSyncJobExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EdFiSyncApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Executes an Ed-Fi Sync Job
                DataSyncApiJobV1JobExecutionRequestedResponse result = apiInstance.ExecuteEdFiSyncJob(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EdFiSyncApi.ExecuteEdFiSyncJob: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExecuteEdFiSyncJobWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Executes an Ed-Fi Sync Job
    ApiResponse<DataSyncApiJobV1JobExecutionRequestedResponse> response = apiInstance.ExecuteEdFiSyncJobWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EdFiSyncApi.ExecuteEdFiSyncJobWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**DataSyncApiJobV1JobExecutionRequestedResponse**](DataSyncApiJobV1JobExecutionRequestedResponse.md)

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

<a id="getedfisyncdata"></a>
# **GetEdFiSyncData**
> DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile GetEdFiSyncData (Guid tenantId)

Retrieves Ed-Fi Sync Connection Data for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEdFiSyncDataExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EdFiSyncApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Retrieves Ed-Fi Sync Connection Data for a given tenant
                DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile result = apiInstance.GetEdFiSyncData(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EdFiSyncApi.GetEdFiSyncData: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEdFiSyncDataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves Ed-Fi Sync Connection Data for a given tenant
    ApiResponse<DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile> response = apiInstance.GetEdFiSyncDataWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EdFiSyncApi.GetEdFiSyncDataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile**](DataSyncApiEdFiRosterSyncV1EdFiRosterSyncJobProfile.md)

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

<a id="updateedfisync"></a>
# **UpdateEdFiSync**
> MicrosoftAspNetCoreMvcNoContentResult UpdateEdFiSync (Guid tenantId, Object body = null)

Updates an Ed-Fi Sync for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateEdFiSyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EdFiSyncApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var body = null;  // Object |  (optional) 

            try
            {
                // Updates an Ed-Fi Sync for a given tenant
                MicrosoftAspNetCoreMvcNoContentResult result = apiInstance.UpdateEdFiSync(tenantId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EdFiSyncApi.UpdateEdFiSync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEdFiSyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Ed-Fi Sync for a given tenant
    ApiResponse<MicrosoftAspNetCoreMvcNoContentResult> response = apiInstance.UpdateEdFiSyncWithHttpInfo(tenantId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EdFiSyncApi.UpdateEdFiSyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **body** | **Object** |  | [optional]  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

