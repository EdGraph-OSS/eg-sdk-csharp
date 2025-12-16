# EdGraph.Platform.Client.Api.InvitationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteTenantInvitationAsync**](InvitationsApi.md#deletetenantinvitationasync) | **DELETE** /tenants/{tenantId}/invitations/{invitationId} | Deletes an invitation |
| [**GetAllTenantInvitationsAsync**](InvitationsApi.md#getalltenantinvitationsasync) | **GET** /tenants/{tenantId}/invitations | Retrieves a list of invitations associated to this tenant |
| [**GetTenantInvitationByIdAsync**](InvitationsApi.md#gettenantinvitationbyidasync) | **GET** /tenants/{tenantId}/invitations/{invitationId} | Retrieves a specific invitation |
| [**SendTenantInvitationAsync**](InvitationsApi.md#sendtenantinvitationasync) | **POST** /tenants/{tenantId}/invitations | Creates and sends an invitation to a user |

<a id="deletetenantinvitationasync"></a>
# **DeleteTenantInvitationAsync**
> void DeleteTenantInvitationAsync (string tenantId, string invitationId)

Deletes an invitation

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteTenantInvitationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InvitationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var invitationId = "invitationId_example";  // string | 

            try
            {
                // Deletes an invitation
                apiInstance.DeleteTenantInvitationAsync(tenantId, invitationId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvitationsApi.DeleteTenantInvitationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTenantInvitationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an invitation
    apiInstance.DeleteTenantInvitationAsyncWithHttpInfo(tenantId, invitationId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvitationsApi.DeleteTenantInvitationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **invitationId** | **string** |  |  |

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

<a id="getalltenantinvitationsasync"></a>
# **GetAllTenantInvitationsAsync**
> IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel GetAllTenantInvitationsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of invitations associated to this tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllTenantInvitationsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InvitationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of invitations associated to this tenant
                IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel result = apiInstance.GetAllTenantInvitationsAsync(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvitationsApi.GetAllTenantInvitationsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantInvitationsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of invitations associated to this tenant
    ApiResponse<IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel> response = apiInstance.GetAllTenantInvitationsAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvitationsApi.GetAllTenantInvitationsAsyncWithHttpInfo: " + e.Message);
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

[**IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel**](IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel.md)

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

<a id="gettenantinvitationbyidasync"></a>
# **GetTenantInvitationByIdAsync**
> IdentityApiInvitationV1InvitationResponse GetTenantInvitationByIdAsync (string tenantId, string invitationId)

Retrieves a specific invitation

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantInvitationByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InvitationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var invitationId = "invitationId_example";  // string | 

            try
            {
                // Retrieves a specific invitation
                IdentityApiInvitationV1InvitationResponse result = apiInstance.GetTenantInvitationByIdAsync(tenantId, invitationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvitationsApi.GetTenantInvitationByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantInvitationByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a specific invitation
    ApiResponse<IdentityApiInvitationV1InvitationResponse> response = apiInstance.GetTenantInvitationByIdAsyncWithHttpInfo(tenantId, invitationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvitationsApi.GetTenantInvitationByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **invitationId** | **string** |  |  |

### Return type

[**IdentityApiInvitationV1InvitationResponse**](IdentityApiInvitationV1InvitationResponse.md)

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

<a id="sendtenantinvitationasync"></a>
# **SendTenantInvitationAsync**
> IdentityApiInvitationV1InvitationSentResponse SendTenantInvitationAsync (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest = null)

Creates and sends an invitation to a user

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SendTenantInvitationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InvitationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest |  (optional) 

            try
            {
                // Creates and sends an invitation to a user
                IdentityApiInvitationV1InvitationSentResponse result = apiInstance.SendTenantInvitationAsync(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InvitationsApi.SendTenantInvitationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SendTenantInvitationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates and sends an invitation to a user
    ApiResponse<IdentityApiInvitationV1InvitationSentResponse> response = apiInstance.SendTenantInvitationAsyncWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InvitationsApi.SendTenantInvitationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiInvitationV1InvitationSentResponse**](IdentityApiInvitationV1InvitationSentResponse.md)

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

