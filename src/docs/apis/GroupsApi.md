# EdGraph.Platform.Client.Api.GroupsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUsersToGroupAsync**](GroupsApi.md#adduserstogroupasync) | **POST** /tenants/{tenantId}/analytics/groups/{groupId}/users/bulk | Adds users to group. |
| [**CreateAnalyticsPowerBiGroup**](GroupsApi.md#createanalyticspowerbigroup) | **POST** /tenants/{tenantId}/analytics/groups | Creates a group. |
| [**DeleteAnalyticsPowerBiGroup**](GroupsApi.md#deleteanalyticspowerbigroup) | **DELETE** /tenants/{tenantId}/analytics/groups/{groupId} | Deletes a group. |
| [**GetAnalyticsPowerBiGroupUsers**](GroupsApi.md#getanalyticspowerbigroupusers) | **GET** /tenants/{tenantId}/analytics/groups/{groupId}/users | Retrieves all users for a specific group. |
| [**GetGroupsAsync**](GroupsApi.md#getgroupsasync) | **GET** /tenants/{tenantId}/analytics/groups | Retrieves a list of groups. |

<a id="adduserstogroupasync"></a>
# **AddUsersToGroupAsync**
> void AddUsersToGroupAsync (string tenantId, string groupId, AnalyticsApiGroupsV1AddGroupUsersRequest analyticsApiGroupsV1AddGroupUsersRequest = null)

Adds users to group.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddUsersToGroupAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new GroupsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var groupId = "groupId_example";  // string | 
            var analyticsApiGroupsV1AddGroupUsersRequest = new AnalyticsApiGroupsV1AddGroupUsersRequest(); // AnalyticsApiGroupsV1AddGroupUsersRequest |  (optional) 

            try
            {
                // Adds users to group.
                apiInstance.AddUsersToGroupAsync(tenantId, groupId, analyticsApiGroupsV1AddGroupUsersRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GroupsApi.AddUsersToGroupAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddUsersToGroupAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds users to group.
    apiInstance.AddUsersToGroupAsyncWithHttpInfo(tenantId, groupId, analyticsApiGroupsV1AddGroupUsersRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GroupsApi.AddUsersToGroupAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **groupId** | **string** |  |  |
| **analyticsApiGroupsV1AddGroupUsersRequest** | [**AnalyticsApiGroupsV1AddGroupUsersRequest**](AnalyticsApiGroupsV1AddGroupUsersRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createanalyticspowerbigroup"></a>
# **CreateAnalyticsPowerBiGroup**
> AnalyticsApiGroupsV1GroupResponse CreateAnalyticsPowerBiGroup (string tenantId, AnalyticsApiGroupsV1CreateGroupRequest analyticsApiGroupsV1CreateGroupRequest = null)

Creates a group.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateAnalyticsPowerBiGroupExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new GroupsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var analyticsApiGroupsV1CreateGroupRequest = new AnalyticsApiGroupsV1CreateGroupRequest(); // AnalyticsApiGroupsV1CreateGroupRequest |  (optional) 

            try
            {
                // Creates a group.
                AnalyticsApiGroupsV1GroupResponse result = apiInstance.CreateAnalyticsPowerBiGroup(tenantId, analyticsApiGroupsV1CreateGroupRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GroupsApi.CreateAnalyticsPowerBiGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAnalyticsPowerBiGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a group.
    ApiResponse<AnalyticsApiGroupsV1GroupResponse> response = apiInstance.CreateAnalyticsPowerBiGroupWithHttpInfo(tenantId, analyticsApiGroupsV1CreateGroupRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GroupsApi.CreateAnalyticsPowerBiGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiGroupsV1CreateGroupRequest** | [**AnalyticsApiGroupsV1CreateGroupRequest**](AnalyticsApiGroupsV1CreateGroupRequest.md) |  | [optional]  |

### Return type

[**AnalyticsApiGroupsV1GroupResponse**](AnalyticsApiGroupsV1GroupResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteanalyticspowerbigroup"></a>
# **DeleteAnalyticsPowerBiGroup**
> void DeleteAnalyticsPowerBiGroup (string tenantId, string groupId)

Deletes a group.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteAnalyticsPowerBiGroupExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new GroupsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var groupId = "groupId_example";  // string | 

            try
            {
                // Deletes a group.
                apiInstance.DeleteAnalyticsPowerBiGroup(tenantId, groupId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GroupsApi.DeleteAnalyticsPowerBiGroup: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAnalyticsPowerBiGroupWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a group.
    apiInstance.DeleteAnalyticsPowerBiGroupWithHttpInfo(tenantId, groupId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GroupsApi.DeleteAnalyticsPowerBiGroupWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **groupId** | **string** |  |  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getanalyticspowerbigroupusers"></a>
# **GetAnalyticsPowerBiGroupUsers**
> AnalyticsApiGroupsV1GroupUsersResponse GetAnalyticsPowerBiGroupUsers (string tenantId, string groupId, int skipFirstN = null, int topFirstN = null)

Retrieves all users for a specific group.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAnalyticsPowerBiGroupUsersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new GroupsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var groupId = "groupId_example";  // string | 
            var skipFirstN = 56;  // int |  (optional) 
            var topFirstN = 56;  // int |  (optional) 

            try
            {
                // Retrieves all users for a specific group.
                AnalyticsApiGroupsV1GroupUsersResponse result = apiInstance.GetAnalyticsPowerBiGroupUsers(tenantId, groupId, skipFirstN, topFirstN);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GroupsApi.GetAnalyticsPowerBiGroupUsers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAnalyticsPowerBiGroupUsersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves all users for a specific group.
    ApiResponse<AnalyticsApiGroupsV1GroupUsersResponse> response = apiInstance.GetAnalyticsPowerBiGroupUsersWithHttpInfo(tenantId, groupId, skipFirstN, topFirstN);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GroupsApi.GetAnalyticsPowerBiGroupUsersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **groupId** | **string** |  |  |
| **skipFirstN** | **int** |  | [optional]  |
| **topFirstN** | **int** |  | [optional]  |

### Return type

[**AnalyticsApiGroupsV1GroupUsersResponse**](AnalyticsApiGroupsV1GroupUsersResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getgroupsasync"></a>
# **GetGroupsAsync**
> AnalyticsApiGroupsV1GroupsResponse GetGroupsAsync (string tenantId, string filter = null)

Retrieves a list of groups.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetGroupsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new GroupsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var filter = "filter_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of groups.
                AnalyticsApiGroupsV1GroupsResponse result = apiInstance.GetGroupsAsync(tenantId, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling GroupsApi.GetGroupsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetGroupsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of groups.
    ApiResponse<AnalyticsApiGroupsV1GroupsResponse> response = apiInstance.GetGroupsAsyncWithHttpInfo(tenantId, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling GroupsApi.GetGroupsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **filter** | **string** |  | [optional]  |

### Return type

[**AnalyticsApiGroupsV1GroupsResponse**](AnalyticsApiGroupsV1GroupsResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

