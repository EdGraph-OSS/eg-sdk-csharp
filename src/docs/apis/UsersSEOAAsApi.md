# EdGraph.Platform.Client.Api.UsersSEOAAsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUserSEOAA**](UsersSEOAAsApi.md#adduserseoaa) | **POST** /v2/tenants/{tenantId}/users/{userId}/seoaas | Add User SEOAAs |
| [**DeleteUserSEOAA**](UsersSEOAAsApi.md#deleteuserseoaa) | **DELETE** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Delete User SEOAAs |
| [**SearchUserSEOAA**](UsersSEOAAsApi.md#searchuserseoaa) | **GET** /v2/tenants/{tenantId}/users/{userId}/seoaas | Search User SEOAAs |
| [**UpdateUserSEOAA**](UsersSEOAAsApi.md#updateuserseoaa) | **PUT** /v2/tenants/{tenantId}/users/{userId}/seoaas/{seoaaId} | Update User SEOAAs |

<a id="adduserseoaa"></a>
# **AddUserSEOAA**
> IdentityApiUserV1SEOAAAddedResponse AddUserSEOAA (Guid tenantId, Guid userId, EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest = null)

Add User SEOAAs

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddUserSEOAAExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSEOAAsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest = new EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest(); // EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest |  (optional) 

            try
            {
                // Add User SEOAAs
                IdentityApiUserV1SEOAAAddedResponse result = apiInstance.AddUserSEOAA(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSEOAAsApi.AddUserSEOAA: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddUserSEOAAWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add User SEOAAs
    ApiResponse<IdentityApiUserV1SEOAAAddedResponse> response = apiInstance.AddUserSEOAAWithHttpInfo(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSEOAAsApi.AddUserSEOAAWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest**](EdGraphHttpAggregatorsTenantApiControllersV2RequestsAddSeoaaRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SEOAAAddedResponse**](IdentityApiUserV1SEOAAAddedResponse.md)

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

<a id="deleteuserseoaa"></a>
# **DeleteUserSEOAA**
> IdentityApiUserV1SEOAAUpdatedResponse DeleteUserSEOAA (Guid tenantId, Guid userId, string seoaaId)

Delete User SEOAAs

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteUserSEOAAExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSEOAAsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var seoaaId = "seoaaId_example";  // string | 

            try
            {
                // Delete User SEOAAs
                IdentityApiUserV1SEOAAUpdatedResponse result = apiInstance.DeleteUserSEOAA(tenantId, userId, seoaaId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSEOAAsApi.DeleteUserSEOAA: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteUserSEOAAWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete User SEOAAs
    ApiResponse<IdentityApiUserV1SEOAAUpdatedResponse> response = apiInstance.DeleteUserSEOAAWithHttpInfo(tenantId, userId, seoaaId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSEOAAsApi.DeleteUserSEOAAWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **seoaaId** | **string** |  |  |

### Return type

[**IdentityApiUserV1SEOAAUpdatedResponse**](IdentityApiUserV1SEOAAUpdatedResponse.md)

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

<a id="searchuserseoaa"></a>
# **SearchUserSEOAA**
> IdentityApiUserV1GetSEOAAsResponse SearchUserSEOAA (Guid tenantId, Guid userId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search User SEOAAs

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchUserSEOAAExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSEOAAsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Search User SEOAAs
                IdentityApiUserV1GetSEOAAsResponse result = apiInstance.SearchUserSEOAA(tenantId, userId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSEOAAsApi.SearchUserSEOAA: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchUserSEOAAWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search User SEOAAs
    ApiResponse<IdentityApiUserV1GetSEOAAsResponse> response = apiInstance.SearchUserSEOAAWithHttpInfo(tenantId, userId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSEOAAsApi.SearchUserSEOAAWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV1GetSEOAAsResponse**](IdentityApiUserV1GetSEOAAsResponse.md)

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

<a id="updateuserseoaa"></a>
# **UpdateUserSEOAA**
> IdentityApiUserV1SEOAAUpdatedResponse UpdateUserSEOAA (Guid tenantId, Guid userId, string seoaaId, EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest = null)

Update User SEOAAs

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateUserSEOAAExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSEOAAsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var seoaaId = "seoaaId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest = new EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest(); // EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest |  (optional) 

            try
            {
                // Update User SEOAAs
                IdentityApiUserV1SEOAAUpdatedResponse result = apiInstance.UpdateUserSEOAA(tenantId, userId, seoaaId, edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSEOAAsApi.UpdateUserSEOAA: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateUserSEOAAWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update User SEOAAs
    ApiResponse<IdentityApiUserV1SEOAAUpdatedResponse> response = apiInstance.UpdateUserSEOAAWithHttpInfo(tenantId, userId, seoaaId, edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSEOAAsApi.UpdateUserSEOAAWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **seoaaId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest**](EdGraphHttpAggregatorsTenantApiControllersV2RequestsUpdateSeoaaRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SEOAAUpdatedResponse**](IdentityApiUserV1SEOAAUpdatedResponse.md)

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

