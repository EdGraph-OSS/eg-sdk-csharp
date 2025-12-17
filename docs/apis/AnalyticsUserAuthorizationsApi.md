# EdGraph.Platform.Client.Api.AnalyticsUserAuthorizationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetPaginatedUserAuthorizations**](AnalyticsUserAuthorizationsApi.md#getpaginateduserauthorizations) | **GET** /tenants/{tenantId}/analytics/userauthorizations | Retrieves paginated user authorizations |
| [**SoftDeleteUserAuthorization**](AnalyticsUserAuthorizationsApi.md#softdeleteuserauthorization) | **DELETE** /tenants/{tenantId}/analytics/userauthorizations/{userAuthorizationId} | Soft Deletes a user authorization by Id |

<a id="getpaginateduserauthorizations"></a>
# **GetPaginatedUserAuthorizations**
> AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse GetPaginatedUserAuthorizations (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves paginated user authorizations

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedUserAuthorizationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AnalyticsUserAuthorizationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves paginated user authorizations
                AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse result = apiInstance.GetPaginatedUserAuthorizations(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsUserAuthorizationsApi.GetPaginatedUserAuthorizations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedUserAuthorizationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves paginated user authorizations
    ApiResponse<AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse> response = apiInstance.GetPaginatedUserAuthorizationsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsUserAuthorizationsApi.GetPaginatedUserAuthorizationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse**](AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse.md)

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

<a id="softdeleteuserauthorization"></a>
# **SoftDeleteUserAuthorization**
> AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse SoftDeleteUserAuthorization (string tenantId, string userAuthorizationId)

Soft Deletes a user authorization by Id

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SoftDeleteUserAuthorizationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AnalyticsUserAuthorizationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userAuthorizationId = "userAuthorizationId_example";  // string | 

            try
            {
                // Soft Deletes a user authorization by Id
                AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse result = apiInstance.SoftDeleteUserAuthorization(tenantId, userAuthorizationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsUserAuthorizationsApi.SoftDeleteUserAuthorization: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SoftDeleteUserAuthorizationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Soft Deletes a user authorization by Id
    ApiResponse<AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse> response = apiInstance.SoftDeleteUserAuthorizationWithHttpInfo(tenantId, userAuthorizationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsUserAuthorizationsApi.SoftDeleteUserAuthorizationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userAuthorizationId** | **string** |  |  |

### Return type

[**AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse**](AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse.md)

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

