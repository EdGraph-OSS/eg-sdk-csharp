# EdGraph.Platform.Client.Api.InstanceResourcesCountApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAllInstanceResourcesCountAsync**](InstanceResourcesCountApi.md#getallinstanceresourcescountasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount | Retrieves a paginated list of Instance Resources Count |
| [**GetAllInstanceResourcesCountJson**](InstanceResourcesCountApi.md#getallinstanceresourcescountjson) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/applications/{applicationId}/apiclients/{apiClientId}/resourcescount/export | Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems. |

<a id="getallinstanceresourcescountasync"></a>
# **GetAllInstanceResourcesCountAsync**
> EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel GetAllInstanceResourcesCountAsync (string tenantId, string instanceId, int year, int applicationId, int apiClientId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a paginated list of Instance Resources Count

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllInstanceResourcesCountAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstanceResourcesCountApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var applicationId = 56;  // int | 
            var apiClientId = 56;  // int | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a paginated list of Instance Resources Count
                EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel result = apiInstance.GetAllInstanceResourcesCountAsync(tenantId, instanceId, year, applicationId, apiClientId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstanceResourcesCountApi.GetAllInstanceResourcesCountAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllInstanceResourcesCountAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a paginated list of Instance Resources Count
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel> response = apiInstance.GetAllInstanceResourcesCountAsyncWithHttpInfo(tenantId, instanceId, year, applicationId, apiClientId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstanceResourcesCountApi.GetAllInstanceResourcesCountAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **applicationId** | **int** |  |  |
| **apiClientId** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1InstanceResourcesCountListResponsePaginatedItemsViewModel.md)

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

<a id="getallinstanceresourcescountjson"></a>
# **GetAllInstanceResourcesCountJson**
> EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse GetAllInstanceResourcesCountJson (string tenantId, string instanceId, int year, int applicationId, int apiClientId, string filter = null)

Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllInstanceResourcesCountJsonExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstanceResourcesCountApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var applicationId = 56;  // int | 
            var apiClientId = 56;  // int | 
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems.
                EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse result = apiInstance.GetAllInstanceResourcesCountJson(tenantId, instanceId, year, applicationId, apiClientId, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstanceResourcesCountApi.GetAllInstanceResourcesCountJson: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllInstanceResourcesCountJsonWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the JSON representation of Instance Resources Count. Useful for exporting into other systems.
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse> response = apiInstance.GetAllInstanceResourcesCountJsonWithHttpInfo(tenantId, instanceId, year, applicationId, apiClientId, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstanceResourcesCountApi.GetAllInstanceResourcesCountJsonWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **applicationId** | **int** |  |  |
| **apiClientId** | **int** |  |  |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse**](EdfiAdminApiEdfiAdminV1InstanceResourcesCountJsonResponse.md)

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

