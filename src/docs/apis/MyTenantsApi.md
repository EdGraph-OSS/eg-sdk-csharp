# EdGraph.Platform.Client.Api.MyTenantsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetUserTenants**](MyTenantsApi.md#getusertenants) | **GET** /me/tenants | Retrieves the Tenants of the User that is currently logged in. |
| [**SearchMyLicenses**](MyTenantsApi.md#searchmylicenses) | **GET** /v2/me/tenants/{tenantId}/licenses | Search the user&#39;s licenses. |
| [**SearchMyTenants**](MyTenantsApi.md#searchmytenants) | **GET** /v2/me/tenants | Searches tenants associated to the user. |

<a id="getusertenants"></a>
# **GetUserTenants**
> IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel GetUserTenants (int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves the Tenants of the User that is currently logged in.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetUserTenantsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new MyTenantsApi(config);
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves the Tenants of the User that is currently logged in.
                IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel result = apiInstance.GetUserTenants(pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MyTenantsApi.GetUserTenants: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUserTenantsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Tenants of the User that is currently logged in.
    ApiResponse<IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel> response = apiInstance.GetUserTenantsWithHttpInfo(pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MyTenantsApi.GetUserTenantsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel**](IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchmylicenses"></a>
# **SearchMyLicenses**
> IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel SearchMyLicenses (Guid tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Search the user's licenses.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchMyLicensesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new MyTenantsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Search the user's licenses.
                IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel result = apiInstance.SearchMyLicenses(tenantId, pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MyTenantsApi.SearchMyLicenses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchMyLicensesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search the user's licenses.
    ApiResponse<IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel> response = apiInstance.SearchMyLicensesWithHttpInfo(tenantId, pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MyTenantsApi.SearchMyLicensesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel**](IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchmytenants"></a>
# **SearchMyTenants**
> IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel SearchMyTenants (int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Searches tenants associated to the user.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchMyTenantsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new MyTenantsApi(config);
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches tenants associated to the user.
                IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel result = apiInstance.SearchMyTenants(pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling MyTenantsApi.SearchMyTenants: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchMyTenantsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches tenants associated to the user.
    ApiResponse<IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel> response = apiInstance.SearchMyTenantsWithHttpInfo(pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling MyTenantsApi.SearchMyTenantsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel**](IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

