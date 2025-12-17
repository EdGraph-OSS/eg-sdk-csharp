# EdGraph.Platform.Client.Api.LogsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetLogs**](LogsApi.md#getlogs) | **GET** /tenants/{tenantId}/validations/logs | Retrieves a list of Logs. |

<a id="getlogs"></a>
# **GetLogs**
> ValidationsApiValidationResultsV1FindResponse GetLogs (string tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string environmentId = null, string collectionId = null, string containerId = null, string ruleId = null, string jobId = null, string jobExecutionId = null)

Retrieves a list of Logs.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetLogsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new LogsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "orderBy_example";  // string |  (optional) 
            var environmentId = "environmentId_example";  // string |  (optional) 
            var collectionId = "collectionId_example";  // string |  (optional) 
            var containerId = "containerId_example";  // string |  (optional) 
            var ruleId = "ruleId_example";  // string |  (optional) 
            var jobId = "jobId_example";  // string |  (optional) 
            var jobExecutionId = "jobExecutionId_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Logs.
                ValidationsApiValidationResultsV1FindResponse result = apiInstance.GetLogs(tenantId, pageIndex, pageSize, orderBy, environmentId, collectionId, containerId, ruleId, jobId, jobExecutionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling LogsApi.GetLogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Logs.
    ApiResponse<ValidationsApiValidationResultsV1FindResponse> response = apiInstance.GetLogsWithHttpInfo(tenantId, pageIndex, pageSize, orderBy, environmentId, collectionId, containerId, ruleId, jobId, jobExecutionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling LogsApi.GetLogsWithHttpInfo: " + e.Message);
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
| **orderBy** | **string** |  | [optional]  |
| **environmentId** | **string** |  | [optional]  |
| **collectionId** | **string** |  | [optional]  |
| **containerId** | **string** |  | [optional]  |
| **ruleId** | **string** |  | [optional]  |
| **jobId** | **string** |  | [optional]  |
| **jobExecutionId** | **string** |  | [optional]  |

### Return type

[**ValidationsApiValidationResultsV1FindResponse**](ValidationsApiValidationResultsV1FindResponse.md)

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

