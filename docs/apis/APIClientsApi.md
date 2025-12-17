# EdGraph.Platform.Client.Api.APIClientsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTenantApiClientAsync**](APIClientsApi.md#createtenantapiclientasync) | **POST** /tenants/{tenantId}/apiclients | Creates a new OpenId API Client |
| [**DeleteTenantApiClientAsync**](APIClientsApi.md#deletetenantapiclientasync) | **DELETE** /tenants/{tenantId}/apiclients/{clientId} | Deletes an OpenId API Client |
| [**GetAllTenantApiClientsAsync**](APIClientsApi.md#getalltenantapiclientsasync) | **GET** /tenants/{tenantId}/apiclients | Retrieves a list of OpenId API Clients associated to this tenant |
| [**GetTenantApiClientByIdAsync**](APIClientsApi.md#gettenantapiclientbyidasync) | **GET** /tenants/{tenantId}/apiclients/{clientId} | Retrieves an OpenId API Client |
| [**RegenerateTenantApiClientSecretAsync**](APIClientsApi.md#regeneratetenantapiclientsecretasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId}/regeneratesecret | Regenerates an OpenId API Client&#39;s secret |
| [**UpdateTenantApiClientAsync**](APIClientsApi.md#updatetenantapiclientasync) | **PUT** /tenants/{tenantId}/apiclients/{clientId} | Updates an OpenId API Client |

<a id="createtenantapiclientasync"></a>
# **CreateTenantApiClientAsync**
> IdentityApiApiClientV1ApiClientCreatedResponse CreateTenantApiClientAsync (string tenantId, IdentityApiApiClientV1CreateApiClientRequest identityApiApiClientV1CreateApiClientRequest = null)

Creates a new OpenId API Client

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateTenantApiClientAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new APIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var identityApiApiClientV1CreateApiClientRequest = new IdentityApiApiClientV1CreateApiClientRequest(); // IdentityApiApiClientV1CreateApiClientRequest |  (optional) 

            try
            {
                // Creates a new OpenId API Client
                IdentityApiApiClientV1ApiClientCreatedResponse result = apiInstance.CreateTenantApiClientAsync(tenantId, identityApiApiClientV1CreateApiClientRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIClientsApi.CreateTenantApiClientAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTenantApiClientAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new OpenId API Client
    ApiResponse<IdentityApiApiClientV1ApiClientCreatedResponse> response = apiInstance.CreateTenantApiClientAsyncWithHttpInfo(tenantId, identityApiApiClientV1CreateApiClientRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIClientsApi.CreateTenantApiClientAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **identityApiApiClientV1CreateApiClientRequest** | [**IdentityApiApiClientV1CreateApiClientRequest**](IdentityApiApiClientV1CreateApiClientRequest.md) |  | [optional]  |

### Return type

[**IdentityApiApiClientV1ApiClientCreatedResponse**](IdentityApiApiClientV1ApiClientCreatedResponse.md)

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

<a id="deletetenantapiclientasync"></a>
# **DeleteTenantApiClientAsync**
> void DeleteTenantApiClientAsync (string tenantId, string clientId)

Deletes an OpenId API Client

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteTenantApiClientAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new APIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var clientId = "clientId_example";  // string | 

            try
            {
                // Deletes an OpenId API Client
                apiInstance.DeleteTenantApiClientAsync(tenantId, clientId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIClientsApi.DeleteTenantApiClientAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTenantApiClientAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an OpenId API Client
    apiInstance.DeleteTenantApiClientAsyncWithHttpInfo(tenantId, clientId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIClientsApi.DeleteTenantApiClientAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |

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

<a id="getalltenantapiclientsasync"></a>
# **GetAllTenantApiClientsAsync**
> IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel GetAllTenantApiClientsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of OpenId API Clients associated to this tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllTenantApiClientsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new APIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of OpenId API Clients associated to this tenant
                IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel result = apiInstance.GetAllTenantApiClientsAsync(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIClientsApi.GetAllTenantApiClientsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantApiClientsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of OpenId API Clients associated to this tenant
    ApiResponse<IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel> response = apiInstance.GetAllTenantApiClientsAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIClientsApi.GetAllTenantApiClientsAsyncWithHttpInfo: " + e.Message);
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

[**IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel**](IdentityApiApiClientV1ApiClientPaginatedItemsResponsePaginatedItemsViewModel.md)

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

<a id="gettenantapiclientbyidasync"></a>
# **GetTenantApiClientByIdAsync**
> IdentityApiApiClientV1ApiClientProfileResponse GetTenantApiClientByIdAsync (string tenantId, string clientId)

Retrieves an OpenId API Client

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantApiClientByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new APIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var clientId = "clientId_example";  // string | 

            try
            {
                // Retrieves an OpenId API Client
                IdentityApiApiClientV1ApiClientProfileResponse result = apiInstance.GetTenantApiClientByIdAsync(tenantId, clientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIClientsApi.GetTenantApiClientByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantApiClientByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an OpenId API Client
    ApiResponse<IdentityApiApiClientV1ApiClientProfileResponse> response = apiInstance.GetTenantApiClientByIdAsyncWithHttpInfo(tenantId, clientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIClientsApi.GetTenantApiClientByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |

### Return type

[**IdentityApiApiClientV1ApiClientProfileResponse**](IdentityApiApiClientV1ApiClientProfileResponse.md)

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

<a id="regeneratetenantapiclientsecretasync"></a>
# **RegenerateTenantApiClientSecretAsync**
> IdentityApiApiClientV1ApiClientSecretRegeneratedResponse RegenerateTenantApiClientSecretAsync (string tenantId, string clientId, IdentityApiApiClientV1RegenerateApiClientSecretRequest identityApiApiClientV1RegenerateApiClientSecretRequest = null)

Regenerates an OpenId API Client's secret

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RegenerateTenantApiClientSecretAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new APIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var clientId = "clientId_example";  // string | 
            var identityApiApiClientV1RegenerateApiClientSecretRequest = new IdentityApiApiClientV1RegenerateApiClientSecretRequest(); // IdentityApiApiClientV1RegenerateApiClientSecretRequest |  (optional) 

            try
            {
                // Regenerates an OpenId API Client's secret
                IdentityApiApiClientV1ApiClientSecretRegeneratedResponse result = apiInstance.RegenerateTenantApiClientSecretAsync(tenantId, clientId, identityApiApiClientV1RegenerateApiClientSecretRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIClientsApi.RegenerateTenantApiClientSecretAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RegenerateTenantApiClientSecretAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Regenerates an OpenId API Client's secret
    ApiResponse<IdentityApiApiClientV1ApiClientSecretRegeneratedResponse> response = apiInstance.RegenerateTenantApiClientSecretAsyncWithHttpInfo(tenantId, clientId, identityApiApiClientV1RegenerateApiClientSecretRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIClientsApi.RegenerateTenantApiClientSecretAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **identityApiApiClientV1RegenerateApiClientSecretRequest** | [**IdentityApiApiClientV1RegenerateApiClientSecretRequest**](IdentityApiApiClientV1RegenerateApiClientSecretRequest.md) |  | [optional]  |

### Return type

[**IdentityApiApiClientV1ApiClientSecretRegeneratedResponse**](IdentityApiApiClientV1ApiClientSecretRegeneratedResponse.md)

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

<a id="updatetenantapiclientasync"></a>
# **UpdateTenantApiClientAsync**
> IdentityApiApiClientV1ApiClientUpdatedResponse UpdateTenantApiClientAsync (string tenantId, string clientId, IdentityApiApiClientV1UpdateApiClientRequest identityApiApiClientV1UpdateApiClientRequest = null)

Updates an OpenId API Client

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateTenantApiClientAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new APIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var clientId = "clientId_example";  // string | 
            var identityApiApiClientV1UpdateApiClientRequest = new IdentityApiApiClientV1UpdateApiClientRequest(); // IdentityApiApiClientV1UpdateApiClientRequest |  (optional) 

            try
            {
                // Updates an OpenId API Client
                IdentityApiApiClientV1ApiClientUpdatedResponse result = apiInstance.UpdateTenantApiClientAsync(tenantId, clientId, identityApiApiClientV1UpdateApiClientRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling APIClientsApi.UpdateTenantApiClientAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTenantApiClientAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an OpenId API Client
    ApiResponse<IdentityApiApiClientV1ApiClientUpdatedResponse> response = apiInstance.UpdateTenantApiClientAsyncWithHttpInfo(tenantId, clientId, identityApiApiClientV1UpdateApiClientRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling APIClientsApi.UpdateTenantApiClientAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **identityApiApiClientV1UpdateApiClientRequest** | [**IdentityApiApiClientV1UpdateApiClientRequest**](IdentityApiApiClientV1UpdateApiClientRequest.md) |  | [optional]  |

### Return type

[**IdentityApiApiClientV1ApiClientUpdatedResponse**](IdentityApiApiClientV1ApiClientUpdatedResponse.md)

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

