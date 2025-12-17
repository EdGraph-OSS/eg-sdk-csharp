# EdGraph.Platform.Client.Api.GatewaysApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAllAnalyticsGatewaysAsync**](GatewaysApi.md#getallanalyticsgatewaysasync) | **GET** /tenants/{tenantId}/analytics/gateways | Retrieves a list of gateways in Power Bi that the user has access to. |

<a id="getallanalyticsgatewaysasync"></a>
# **GetAllAnalyticsGatewaysAsync**
> EdfiAdminApiEdfiAdminV1Instance GetAllAnalyticsGatewaysAsync (string tenantId)

Retrieves a list of gateways in Power Bi that the user has access to.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllAnalyticsGatewaysAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new GatewaysApi(config);
            var tenantId = "tenantId_example";  // string | 

            try
            {
                // Retrieves a list of gateways in Power Bi that the user has access to.
                EdfiAdminApiEdfiAdminV1Instance result = apiInstance.GetAllAnalyticsGatewaysAsync(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GatewaysApi.GetAllAnalyticsGatewaysAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllAnalyticsGatewaysAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of gateways in Power Bi that the user has access to.
    ApiResponse<EdfiAdminApiEdfiAdminV1Instance> response = apiInstance.GetAllAnalyticsGatewaysAsyncWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GatewaysApi.GetAllAnalyticsGatewaysAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

