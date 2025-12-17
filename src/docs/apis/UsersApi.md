# EdGraph.Platform.Client.Api.UsersApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**ActivateTenantUserAsync**](UsersApi.md#activatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/activate | Activates a user |
| [**CreateTenantLocalUserAsync**](UsersApi.md#createtenantlocaluserasync) | **POST** /tenants/{tenantId}/users | Creates a user in the local identity provider |
| [**DeactivateTenantUserAsync**](UsersApi.md#deactivatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/deactivate | Deactivates a user |
| [**DeleteTenantUserAsync**](UsersApi.md#deletetenantuserasync) | **DELETE** /tenants/{tenantId}/users/{userId} | Deletes a user |
| [**GetAllTenantUsersAsync**](UsersApi.md#getalltenantusersasync) | **GET** /tenants/{tenantId}/users | Retrieves a list of users associated to this tenant |
| [**GetAllUsers**](UsersApi.md#getallusers) | **GET** /tenants/{tenantId}/statereporting/users | Get All Users |
| [**GetTenantUser**](UsersApi.md#gettenantuser) | **GET** /v2/tenants/{tenantId}/users/{userId} | Get User |
| [**GetTenantUserProfileByIdAsync**](UsersApi.md#gettenantuserprofilebyidasync) | **GET** /tenants/{tenantId}/users/{userId} | Retrieves a user |
| [**GetUserTenant**](UsersApi.md#getusertenant) | **GET** /v2/tenants/{tenantId}/users/{userId}/tenant | Get User Tenant |
| [**GetUserTenantStatusProfile**](UsersApi.md#getusertenantstatusprofile) | **GET** /tenants/{tenantId}/users/{email}/status | Searches a user by email and retrieves it&#39;s minimal information and status. |
| [**ResetMfaStatusAsync**](UsersApi.md#resetmfastatusasync) | **PUT** /tenants/{tenantId}/users/{userId}/resetmfa | Reset the MFA Status for the User |
| [**ResetPasswordTenantUserAsync**](UsersApi.md#resetpasswordtenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/resetpassword | Resets a user&#39;s password |
| [**SearchTenantUsers**](UsersApi.md#searchtenantusers) | **GET** /v2/tenants/{tenantId}/users | Search Users |
| [**SearchUserLicenses**](UsersApi.md#searchuserlicenses) | **GET** /v2/tenants/{tenantId}/users/{userId}/licenses | Search User Licenses |
| [**SearchUserLicensesBulk**](UsersApi.md#searchuserlicensesbulk) | **GET** /v2/tenants/{tenantId}/users/licensesBulk | Search user licenses in bulk. |
| [**UpdateTenantUserAsync**](UsersApi.md#updatetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId} | Creates or updates a user |

<a id="activatetenantuserasync"></a>
# **ActivateTenantUserAsync**
> IdentityApiUserV1UserActivatedResponse ActivateTenantUserAsync (string tenantId, string userId, IdentityApiUserV1ActivateUserRequest identityApiUserV1ActivateUserRequest = null)

Activates a user

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ActivateTenantUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var identityApiUserV1ActivateUserRequest = new IdentityApiUserV1ActivateUserRequest(); // IdentityApiUserV1ActivateUserRequest |  (optional) 

            try
            {
                // Activates a user
                IdentityApiUserV1UserActivatedResponse result = apiInstance.ActivateTenantUserAsync(tenantId, userId, identityApiUserV1ActivateUserRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.ActivateTenantUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ActivateTenantUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Activates a user
    ApiResponse<IdentityApiUserV1UserActivatedResponse> response = apiInstance.ActivateTenantUserAsyncWithHttpInfo(tenantId, userId, identityApiUserV1ActivateUserRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.ActivateTenantUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **identityApiUserV1ActivateUserRequest** | [**IdentityApiUserV1ActivateUserRequest**](IdentityApiUserV1ActivateUserRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1UserActivatedResponse**](IdentityApiUserV1UserActivatedResponse.md)

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

<a id="createtenantlocaluserasync"></a>
# **CreateTenantLocalUserAsync**
> IdentityApiUserV1LocalUserCreatedResponse CreateTenantLocalUserAsync (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest = null)

Creates a user in the local identity provider

Note: This is only used to create a user in the local identity provider, i.e. this cannot be used to create a user in an external identity providers such as Microsoft or Google.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateTenantLocalUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest |  (optional) 

            try
            {
                // Creates a user in the local identity provider
                IdentityApiUserV1LocalUserCreatedResponse result = apiInstance.CreateTenantLocalUserAsync(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.CreateTenantLocalUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTenantLocalUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a user in the local identity provider
    ApiResponse<IdentityApiUserV1LocalUserCreatedResponse> response = apiInstance.CreateTenantLocalUserAsyncWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.CreateTenantLocalUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateLocalUserRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LocalUserCreatedResponse**](IdentityApiUserV1LocalUserCreatedResponse.md)

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deactivatetenantuserasync"></a>
# **DeactivateTenantUserAsync**
> IdentityApiUserV1UserDeactivatedResponse DeactivateTenantUserAsync (string tenantId, string userId, IdentityApiUserV1DeactivateUserRequest identityApiUserV1DeactivateUserRequest = null)

Deactivates a user

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeactivateTenantUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var identityApiUserV1DeactivateUserRequest = new IdentityApiUserV1DeactivateUserRequest(); // IdentityApiUserV1DeactivateUserRequest |  (optional) 

            try
            {
                // Deactivates a user
                IdentityApiUserV1UserDeactivatedResponse result = apiInstance.DeactivateTenantUserAsync(tenantId, userId, identityApiUserV1DeactivateUserRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.DeactivateTenantUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeactivateTenantUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deactivates a user
    ApiResponse<IdentityApiUserV1UserDeactivatedResponse> response = apiInstance.DeactivateTenantUserAsyncWithHttpInfo(tenantId, userId, identityApiUserV1DeactivateUserRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.DeactivateTenantUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **identityApiUserV1DeactivateUserRequest** | [**IdentityApiUserV1DeactivateUserRequest**](IdentityApiUserV1DeactivateUserRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1UserDeactivatedResponse**](IdentityApiUserV1UserDeactivatedResponse.md)

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

<a id="deletetenantuserasync"></a>
# **DeleteTenantUserAsync**
> void DeleteTenantUserAsync (string tenantId, string userId)

Deletes a user

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteTenantUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 

            try
            {
                // Deletes a user
                apiInstance.DeleteTenantUserAsync(tenantId, userId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.DeleteTenantUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTenantUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a user
    apiInstance.DeleteTenantUserAsyncWithHttpInfo(tenantId, userId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.DeleteTenantUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |

### Return type

void (empty response body)

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
| **204** | The resource was successfully deleted. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getalltenantusersasync"></a>
# **GetAllTenantUsersAsync**
> EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel GetAllTenantUsersAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of users associated to this tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllTenantUsersAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of users associated to this tenant
                EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel result = apiInstance.GetAllTenantUsersAsync(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.GetAllTenantUsersAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantUsersAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of users associated to this tenant
    ApiResponse<EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel> response = apiInstance.GetAllTenantUsersAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.GetAllTenantUsersAsyncWithHttpInfo: " + e.Message);
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

[**EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserListResponseWithApplicationLicensePaginatedItemsViewModel.md)

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

<a id="getallusers"></a>
# **GetAllUsers**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel GetAllUsers (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Get All Users

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllUsersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get All Users
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel result = apiInstance.GetAllUsers(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.GetAllUsers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllUsersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get All Users
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel> response = apiInstance.GetAllUsersWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.GetAllUsersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserBasicListResponsePaginatedItemsViewModel.md)

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
| **200** |  |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettenantuser"></a>
# **GetTenantUser**
> IdentityApiUserV2UserProfileResponse GetTenantUser (string tenantId, string userId)

Get User

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantUserExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 

            try
            {
                // Get User
                IdentityApiUserV2UserProfileResponse result = apiInstance.GetTenantUser(tenantId, userId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.GetTenantUser: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantUserWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get User
    ApiResponse<IdentityApiUserV2UserProfileResponse> response = apiInstance.GetTenantUserWithHttpInfo(tenantId, userId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.GetTenantUserWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |

### Return type

[**IdentityApiUserV2UserProfileResponse**](IdentityApiUserV2UserProfileResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="gettenantuserprofilebyidasync"></a>
# **GetTenantUserProfileByIdAsync**
> EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense GetTenantUserProfileByIdAsync (string tenantId, string userId)

Retrieves a user

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantUserProfileByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 

            try
            {
                // Retrieves a user
                EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense result = apiInstance.GetTenantUserProfileByIdAsync(tenantId, userId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.GetTenantUserProfileByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantUserProfileByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a user
    ApiResponse<EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense> response = apiInstance.GetTenantUserProfileByIdAsyncWithHttpInfo(tenantId, userId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.GetTenantUserProfileByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |

### Return type

[**EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserProfileResponseWithApplicationLicense.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getusertenant"></a>
# **GetUserTenant**
> IdentityApiUserV2UserTenantProfileResponse GetUserTenant (string tenantId, string userId)

Get User Tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetUserTenantExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 

            try
            {
                // Get User Tenant
                IdentityApiUserV2UserTenantProfileResponse result = apiInstance.GetUserTenant(tenantId, userId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.GetUserTenant: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUserTenantWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get User Tenant
    ApiResponse<IdentityApiUserV2UserTenantProfileResponse> response = apiInstance.GetUserTenantWithHttpInfo(tenantId, userId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.GetUserTenantWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |

### Return type

[**IdentityApiUserV2UserTenantProfileResponse**](IdentityApiUserV2UserTenantProfileResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getusertenantstatusprofile"></a>
# **GetUserTenantStatusProfile**
> IdentityApiUserV1UserTenantStatusProfile GetUserTenantStatusProfile (Guid tenantId, string email)

Searches a user by email and retrieves it's minimal information and status.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetUserTenantStatusProfileExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var email = "email_example";  // string | 

            try
            {
                // Searches a user by email and retrieves it's minimal information and status.
                IdentityApiUserV1UserTenantStatusProfile result = apiInstance.GetUserTenantStatusProfile(tenantId, email);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.GetUserTenantStatusProfile: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUserTenantStatusProfileWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches a user by email and retrieves it's minimal information and status.
    ApiResponse<IdentityApiUserV1UserTenantStatusProfile> response = apiInstance.GetUserTenantStatusProfileWithHttpInfo(tenantId, email);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.GetUserTenantStatusProfileWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **email** | **string** |  |  |

### Return type

[**IdentityApiUserV1UserTenantStatusProfile**](IdentityApiUserV1UserTenantStatusProfile.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="resetmfastatusasync"></a>
# **ResetMfaStatusAsync**
> void ResetMfaStatusAsync (string tenantId, string userId)

Reset the MFA Status for the User

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ResetMfaStatusAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 

            try
            {
                // Reset the MFA Status for the User
                apiInstance.ResetMfaStatusAsync(tenantId, userId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.ResetMfaStatusAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetMfaStatusAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Reset the MFA Status for the User
    apiInstance.ResetMfaStatusAsyncWithHttpInfo(tenantId, userId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.ResetMfaStatusAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |

### Return type

void (empty response body)

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
| **202** | Accepted |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="resetpasswordtenantuserasync"></a>
# **ResetPasswordTenantUserAsync**
> IdentityApiUserV1PasswordResettedResponse ResetPasswordTenantUserAsync (string tenantId, string userId, IdentityApiUserV1ResetPasswordRequest identityApiUserV1ResetPasswordRequest = null)

Resets a user's password

Note: This is only applicable to user created in the local identity provider.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ResetPasswordTenantUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var identityApiUserV1ResetPasswordRequest = new IdentityApiUserV1ResetPasswordRequest(); // IdentityApiUserV1ResetPasswordRequest |  (optional) 

            try
            {
                // Resets a user's password
                IdentityApiUserV1PasswordResettedResponse result = apiInstance.ResetPasswordTenantUserAsync(tenantId, userId, identityApiUserV1ResetPasswordRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.ResetPasswordTenantUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetPasswordTenantUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resets a user's password
    ApiResponse<IdentityApiUserV1PasswordResettedResponse> response = apiInstance.ResetPasswordTenantUserAsyncWithHttpInfo(tenantId, userId, identityApiUserV1ResetPasswordRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.ResetPasswordTenantUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **identityApiUserV1ResetPasswordRequest** | [**IdentityApiUserV1ResetPasswordRequest**](IdentityApiUserV1ResetPasswordRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1PasswordResettedResponse**](IdentityApiUserV1PasswordResettedResponse.md)

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

<a id="searchtenantusers"></a>
# **SearchTenantUsers**
> IdentityApiUserV2UsersSearchResponse SearchTenantUsers (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search Users

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchTenantUsersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Search Users
                IdentityApiUserV2UsersSearchResponse result = apiInstance.SearchTenantUsers(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.SearchTenantUsers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchTenantUsersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Users
    ApiResponse<IdentityApiUserV2UsersSearchResponse> response = apiInstance.SearchTenantUsersWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.SearchTenantUsersWithHttpInfo: " + e.Message);
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

[**IdentityApiUserV2UsersSearchResponse**](IdentityApiUserV2UsersSearchResponse.md)

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

<a id="searchuserlicenses"></a>
# **SearchUserLicenses**
> IdentityApiUserV2UserLicensesResponse SearchUserLicenses (string tenantId, string userId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search User Licenses

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchUserLicensesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = "userId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Search User Licenses
                IdentityApiUserV2UserLicensesResponse result = apiInstance.SearchUserLicenses(tenantId, userId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.SearchUserLicenses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchUserLicensesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search User Licenses
    ApiResponse<IdentityApiUserV2UserLicensesResponse> response = apiInstance.SearchUserLicensesWithHttpInfo(tenantId, userId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.SearchUserLicensesWithHttpInfo: " + e.Message);
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

[**IdentityApiUserV2UserLicensesResponse**](IdentityApiUserV2UserLicensesResponse.md)

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

<a id="searchuserlicensesbulk"></a>
# **SearchUserLicensesBulk**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk&gt; SearchUserLicensesBulk (string tenantId, List<Guid> userId = null, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search user licenses in bulk.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchUserLicensesBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // string | 
            var userId = new List<Guid>(); // List<Guid> |  (optional) 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Search user licenses in bulk.
                List<EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk> result = apiInstance.SearchUserLicensesBulk(tenantId, userId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.SearchUserLicensesBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchUserLicensesBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search user licenses in bulk.
    ApiResponse<List<EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk>> response = apiInstance.SearchUserLicensesBulkWithHttpInfo(tenantId, userId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.SearchUserLicensesBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | [**List&lt;Guid&gt;**](Guid.md) |  | [optional]  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk&gt;**](EdGraphHttpAggregatorsTenantApiControllersV2ResponsesUserLicenseSearchResultBulk.md)

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

<a id="updatetenantuserasync"></a>
# **UpdateTenantUserAsync**
> IdentityApiUserV1UserUpdatedResponse UpdateTenantUserAsync (Guid tenantId, Guid userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest = null)

Creates or updates a user

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateTenantUserAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest |  (optional) 

            try
            {
                // Creates or updates a user
                IdentityApiUserV1UserUpdatedResponse result = apiInstance.UpdateTenantUserAsync(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersApi.UpdateTenantUserAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTenantUserAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates or updates a user
    ApiResponse<IdentityApiUserV1UserUpdatedResponse> response = apiInstance.UpdateTenantUserAsyncWithHttpInfo(tenantId, userId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersApi.UpdateTenantUserAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateTenantUserRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1UserUpdatedResponse**](IdentityApiUserV1UserUpdatedResponse.md)

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

