# EdGraph.Platform.Client.Api.ApplicationsTilesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetTenantApplicationTilesAsync**](ApplicationsTilesApi.md#gettenantapplicationtilesasync) | **GET** /tenants/{tenantId}/applicationtiles | Retrieves a list of applications licensed to the user that is currently logged in the context of this tenant |

<a id="gettenantapplicationtilesasync"></a>
# **GetTenantApplicationTilesAsync**
> EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense GetTenantApplicationTilesAsync (string tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of applications licensed to the user that is currently logged in the context of this tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantApplicationTilesAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ApplicationsTilesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 100;  // int |  (optional)  (default to 100)
            var orderBy = "\"applicationName ASC\"";  // string |  (optional)  (default to "applicationName ASC")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of applications licensed to the user that is currently logged in the context of this tenant
                EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense result = apiInstance.GetTenantApplicationTilesAsync(tenantId, pageIndex, pageSize, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApplicationsTilesApi.GetTenantApplicationTilesAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantApplicationTilesAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of applications licensed to the user that is currently logged in the context of this tenant
    ApiResponse<EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense> response = apiInstance.GetTenantApplicationTilesAsyncWithHttpInfo(tenantId, pageIndex, pageSize, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApplicationsTilesApi.GetTenantApplicationTilesAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 100] |
| **orderBy** | **string** |  | [optional] [default to &quot;applicationName ASC&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesApplicationTilesResponseWithUserApplicationLicense.md)

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

