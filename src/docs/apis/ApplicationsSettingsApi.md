# EdGraph.Platform.Client.Api.ApplicationsSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetClientSettingsAsync**](ApplicationsSettingsApi.md#getclientsettingsasync) | **GET** /tenants/{tenantId}/clients/{clientId}/settings | Retrieves a list of a Tenant&#39;s ClientSettings. |
| [**GetClientSettingsTypesAsync**](ApplicationsSettingsApi.md#getclientsettingstypesasync) | **GET** /tenants/{tenantId}/clients/{clientId}/settingstypes | Retrieves a list of ClientSettingsTypes. |
| [**SetClientSettingsAsync**](ApplicationsSettingsApi.md#setclientsettingsasync) | **POST** /tenants/{tenantId}/clients/{clientId}/settings | Creates/updates a Tenant&#39;s ClientSettings. |

<a id="getclientsettingsasync"></a>
# **GetClientSettingsAsync**
> TenantApiTenantV1GetAppSettingsResponse GetClientSettingsAsync (Guid tenantId, string clientId)

Retrieves a list of a Tenant's ClientSettings.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetClientSettingsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ApplicationsSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var clientId = "clientId_example";  // string | 

            try
            {
                // Retrieves a list of a Tenant's ClientSettings.
                TenantApiTenantV1GetAppSettingsResponse result = apiInstance.GetClientSettingsAsync(tenantId, clientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApplicationsSettingsApi.GetClientSettingsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetClientSettingsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of a Tenant's ClientSettings.
    ApiResponse<TenantApiTenantV1GetAppSettingsResponse> response = apiInstance.GetClientSettingsAsyncWithHttpInfo(tenantId, clientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApplicationsSettingsApi.GetClientSettingsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |

### Return type

[**TenantApiTenantV1GetAppSettingsResponse**](TenantApiTenantV1GetAppSettingsResponse.md)

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

<a id="getclientsettingstypesasync"></a>
# **GetClientSettingsTypesAsync**
> IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse GetClientSettingsTypesAsync (Guid tenantId, string clientId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of ClientSettingsTypes.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetClientSettingsTypesAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ApplicationsSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var clientId = "clientId_example";  // string | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of ClientSettingsTypes.
                IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse result = apiInstance.GetClientSettingsTypesAsync(tenantId, clientId, pageIndex, pageSize, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApplicationsSettingsApi.GetClientSettingsTypesAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetClientSettingsTypesAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of ClientSettingsTypes.
    ApiResponse<IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse> response = apiInstance.GetClientSettingsTypesAsyncWithHttpInfo(tenantId, clientId, pageIndex, pageSize, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApplicationsSettingsApi.GetClientSettingsTypesAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse**](IdentityApiClientSettingsTypeV1GetClientSettingsTypesResponse.md)

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

<a id="setclientsettingsasync"></a>
# **SetClientSettingsAsync**
> TenantApiTenantV1SetAppSettingsResponse SetClientSettingsAsync (Guid tenantId, string clientId, TenantApiTenantV1SetAppSettingsRequest tenantApiTenantV1SetAppSettingsRequest = null)

Creates/updates a Tenant's ClientSettings.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetClientSettingsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ApplicationsSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var clientId = "clientId_example";  // string | 
            var tenantApiTenantV1SetAppSettingsRequest = new TenantApiTenantV1SetAppSettingsRequest(); // TenantApiTenantV1SetAppSettingsRequest |  (optional) 

            try
            {
                // Creates/updates a Tenant's ClientSettings.
                TenantApiTenantV1SetAppSettingsResponse result = apiInstance.SetClientSettingsAsync(tenantId, clientId, tenantApiTenantV1SetAppSettingsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ApplicationsSettingsApi.SetClientSettingsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetClientSettingsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates/updates a Tenant's ClientSettings.
    ApiResponse<TenantApiTenantV1SetAppSettingsResponse> response = apiInstance.SetClientSettingsAsyncWithHttpInfo(tenantId, clientId, tenantApiTenantV1SetAppSettingsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ApplicationsSettingsApi.SetClientSettingsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **tenantApiTenantV1SetAppSettingsRequest** | [**TenantApiTenantV1SetAppSettingsRequest**](TenantApiTenantV1SetAppSettingsRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1SetAppSettingsResponse**](TenantApiTenantV1SetAppSettingsResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

