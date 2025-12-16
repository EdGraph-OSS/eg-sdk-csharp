# EdGraph.Platform.Client.Api.UsersLicensesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AssignLicenseTenantUserAsync**](UsersLicensesApi.md#assignlicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assign | Assigns a license to a user in the context of a specific tenant |
| [**AssignLicenseTenantUserBulkAsync**](UsersLicensesApi.md#assignlicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assignbulk | Assigns one or more licenses to a user in the context of a specific tenant |
| [**GetAllTenantUserApplicationLicensesAsync**](UsersLicensesApi.md#getalltenantuserapplicationlicensesasync) | **GET** /tenants/{tenantId}/users/{userId}/licenses | Retrieves a list of user licenses in the context of a specific tenant |
| [**RevokeLicenseTenantUserAsync**](UsersLicensesApi.md#revokelicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revoke | Revokes a license from a user in the context of a specific tenant |
| [**RevokeLicenseTenantUserBulkAsync**](UsersLicensesApi.md#revokelicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revokebulk | Revokes one or more licenses from a user in the context of a specific tenant |

<a id="assignlicensetenantuserasync"></a>
# **AssignLicenseTenantUserAsync**
> IdentityApiUserV1LicenseAssignedResponse AssignLicenseTenantUserAsync (string tenantId, string userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest = null)

Assigns a license to a user in the context of a specific tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AssignLicenseTenantUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersLicensesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest |  (optional) 

            try
            {
                // Assigns a license to a user in the context of a specific tenant
                IdentityApiUserV1LicenseAssignedResponse result = apiInstance.AssignLicenseTenantUserAsync(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersLicensesApi.AssignLicenseTenantUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AssignLicenseTenantUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Assigns a license to a user in the context of a specific tenant
    ApiResponse<IdentityApiUserV1LicenseAssignedResponse> response = apiInstance.AssignLicenseTenantUserAsyncWithHttpInfo(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersLicensesApi.AssignLicenseTenantUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseAssignedResponse**](IdentityApiUserV1LicenseAssignedResponse.md)

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

<a id="assignlicensetenantuserbulkasync"></a>
# **AssignLicenseTenantUserBulkAsync**
> IdentityApiUserV1LicenseAssignedBulkResponse AssignLicenseTenantUserBulkAsync (string tenantId, string userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest = null)

Assigns one or more licenses to a user in the context of a specific tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AssignLicenseTenantUserBulkAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersLicensesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest |  (optional) 

            try
            {
                // Assigns one or more licenses to a user in the context of a specific tenant
                IdentityApiUserV1LicenseAssignedBulkResponse result = apiInstance.AssignLicenseTenantUserBulkAsync(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersLicensesApi.AssignLicenseTenantUserBulkAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AssignLicenseTenantUserBulkAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Assigns one or more licenses to a user in the context of a specific tenant
    ApiResponse<IdentityApiUserV1LicenseAssignedBulkResponse> response = apiInstance.AssignLicenseTenantUserBulkAsyncWithHttpInfo(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersLicensesApi.AssignLicenseTenantUserBulkAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseAssignedBulkResponse**](IdentityApiUserV1LicenseAssignedBulkResponse.md)

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

<a id="getalltenantuserapplicationlicensesasync"></a>
# **GetAllTenantUserApplicationLicensesAsync**
> EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel GetAllTenantUserApplicationLicensesAsync (string tenantId, string userId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of user licenses in the context of a specific tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllTenantUserApplicationLicensesAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersLicensesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of user licenses in the context of a specific tenant
                EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel result = apiInstance.GetAllTenantUserApplicationLicensesAsync(tenantId, userId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersLicensesApi.GetAllTenantUserApplicationLicensesAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantUserApplicationLicensesAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of user licenses in the context of a specific tenant
    ApiResponse<EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel> response = apiInstance.GetAllTenantUserApplicationLicensesAsyncWithHttpInfo(tenantId, userId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersLicensesApi.GetAllTenantUserApplicationLicensesAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel.md)

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

<a id="revokelicensetenantuserasync"></a>
# **RevokeLicenseTenantUserAsync**
> IdentityApiUserV1LicenseRevokedResponse RevokeLicenseTenantUserAsync (string tenantId, string userId, IdentityApiUserV1RevokeLicenseRequest identityApiUserV1RevokeLicenseRequest = null)

Revokes a license from a user in the context of a specific tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RevokeLicenseTenantUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersLicensesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var identityApiUserV1RevokeLicenseRequest = new IdentityApiUserV1RevokeLicenseRequest(); // IdentityApiUserV1RevokeLicenseRequest |  (optional) 

            try
            {
                // Revokes a license from a user in the context of a specific tenant
                IdentityApiUserV1LicenseRevokedResponse result = apiInstance.RevokeLicenseTenantUserAsync(tenantId, userId, identityApiUserV1RevokeLicenseRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersLicensesApi.RevokeLicenseTenantUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RevokeLicenseTenantUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Revokes a license from a user in the context of a specific tenant
    ApiResponse<IdentityApiUserV1LicenseRevokedResponse> response = apiInstance.RevokeLicenseTenantUserAsyncWithHttpInfo(tenantId, userId, identityApiUserV1RevokeLicenseRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersLicensesApi.RevokeLicenseTenantUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **identityApiUserV1RevokeLicenseRequest** | [**IdentityApiUserV1RevokeLicenseRequest**](IdentityApiUserV1RevokeLicenseRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseRevokedResponse**](IdentityApiUserV1LicenseRevokedResponse.md)

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

<a id="revokelicensetenantuserbulkasync"></a>
# **RevokeLicenseTenantUserBulkAsync**
> IdentityApiUserV1LicenseRevokedBulkResponse RevokeLicenseTenantUserBulkAsync (string tenantId, string userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest = null)

Revokes one or more licenses from a user in the context of a specific tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RevokeLicenseTenantUserBulkAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersLicensesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest |  (optional) 

            try
            {
                // Revokes one or more licenses from a user in the context of a specific tenant
                IdentityApiUserV1LicenseRevokedBulkResponse result = apiInstance.RevokeLicenseTenantUserBulkAsync(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersLicensesApi.RevokeLicenseTenantUserBulkAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RevokeLicenseTenantUserBulkAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Revokes one or more licenses from a user in the context of a specific tenant
    ApiResponse<IdentityApiUserV1LicenseRevokedBulkResponse> response = apiInstance.RevokeLicenseTenantUserBulkAsyncWithHttpInfo(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersLicensesApi.RevokeLicenseTenantUserBulkAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseRevokedBulkResponse**](IdentityApiUserV1LicenseRevokedBulkResponse.md)

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

