# EdGraph.Platform.Client.Api.WebhooksApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateWebhookAsync**](WebhooksApi.md#createwebhookasync) | **POST** /tenants/{tenantId}/webhooks | Creates a new Webhook |
| [**DeleteWebhookAsync**](WebhooksApi.md#deletewebhookasync) | **DELETE** /tenants/{tenantId}/webhooks/{webhookId} | Removes a webhook. |
| [**GetAllWebhookSubscriptionsAsync**](WebhooksApi.md#getallwebhooksubscriptionsasync) | **GET** /tenants/{tenantId}/webhooks/events |  |
| [**GetAllWebhooksAsync**](WebhooksApi.md#getallwebhooksasync) | **GET** /tenants/{tenantId}/webhooks | Retrieves a list of webhooks. |
| [**GetWebhookByIdAsync**](WebhooksApi.md#getwebhookbyidasync) | **GET** /tenants/{tenantId}/webhooks/{webhookId} | Retrieves a webhook by ID. |
| [**UpdateWebhookAsync**](WebhooksApi.md#updatewebhookasync) | **PUT** /tenants/{tenantId}/webhooks/{webhookId} | Updates a webhook |

<a id="createwebhookasync"></a>
# **CreateWebhookAsync**
> TenantApiWebhookV1WebhookIdResponse CreateWebhookAsync (string tenantId, TenantApiWebhookV1CreateWebhookRequest tenantApiWebhookV1CreateWebhookRequest = null)

Creates a new Webhook

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateWebhookAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var tenantId = "tenantId_example";  // string | 
            var tenantApiWebhookV1CreateWebhookRequest = new TenantApiWebhookV1CreateWebhookRequest(); // TenantApiWebhookV1CreateWebhookRequest |  (optional) 

            try
            {
                // Creates a new Webhook
                TenantApiWebhookV1WebhookIdResponse result = apiInstance.CreateWebhookAsync(tenantId, tenantApiWebhookV1CreateWebhookRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.CreateWebhookAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateWebhookAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Webhook
    ApiResponse<TenantApiWebhookV1WebhookIdResponse> response = apiInstance.CreateWebhookAsyncWithHttpInfo(tenantId, tenantApiWebhookV1CreateWebhookRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.CreateWebhookAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **tenantApiWebhookV1CreateWebhookRequest** | [**TenantApiWebhookV1CreateWebhookRequest**](TenantApiWebhookV1CreateWebhookRequest.md) |  | [optional]  |

### Return type

[**TenantApiWebhookV1WebhookIdResponse**](TenantApiWebhookV1WebhookIdResponse.md)

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

<a id="deletewebhookasync"></a>
# **DeleteWebhookAsync**
> TenantApiWebhookV1WebhookIdResponse DeleteWebhookAsync (string tenantId, string webhookId)

Removes a webhook.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteWebhookAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var tenantId = "tenantId_example";  // string | 
            var webhookId = "webhookId_example";  // string | 

            try
            {
                // Removes a webhook.
                TenantApiWebhookV1WebhookIdResponse result = apiInstance.DeleteWebhookAsync(tenantId, webhookId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.DeleteWebhookAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteWebhookAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Removes a webhook.
    ApiResponse<TenantApiWebhookV1WebhookIdResponse> response = apiInstance.DeleteWebhookAsyncWithHttpInfo(tenantId, webhookId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.DeleteWebhookAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **webhookId** | **string** |  |  |

### Return type

[**TenantApiWebhookV1WebhookIdResponse**](TenantApiWebhookV1WebhookIdResponse.md)

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

<a id="getallwebhooksubscriptionsasync"></a>
# **GetAllWebhookSubscriptionsAsync**
> TenantApiWebhookV1WebhookEventsResponse GetAllWebhookSubscriptionsAsync (string tenantId)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllWebhookSubscriptionsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var tenantId = "tenantId_example";  // string | 

            try
            {
                TenantApiWebhookV1WebhookEventsResponse result = apiInstance.GetAllWebhookSubscriptionsAsync(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.GetAllWebhookSubscriptionsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllWebhookSubscriptionsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<TenantApiWebhookV1WebhookEventsResponse> response = apiInstance.GetAllWebhookSubscriptionsAsyncWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.GetAllWebhookSubscriptionsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**TenantApiWebhookV1WebhookEventsResponse**](TenantApiWebhookV1WebhookEventsResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getallwebhooksasync"></a>
# **GetAllWebhooksAsync**
> TenantApiWebhookV1PaginatedItemsResponse GetAllWebhooksAsync (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of webhooks.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllWebhooksAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of webhooks.
                TenantApiWebhookV1PaginatedItemsResponse result = apiInstance.GetAllWebhooksAsync(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.GetAllWebhooksAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllWebhooksAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of webhooks.
    ApiResponse<TenantApiWebhookV1PaginatedItemsResponse> response = apiInstance.GetAllWebhooksAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.GetAllWebhooksAsyncWithHttpInfo: " + e.Message);
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

[**TenantApiWebhookV1PaginatedItemsResponse**](TenantApiWebhookV1PaginatedItemsResponse.md)

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

<a id="getwebhookbyidasync"></a>
# **GetWebhookByIdAsync**
> TenantApiWebhookV1WebhookResponse GetWebhookByIdAsync (string tenantId, string webhookId)

Retrieves a webhook by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetWebhookByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var tenantId = "tenantId_example";  // string | 
            var webhookId = "webhookId_example";  // string | 

            try
            {
                // Retrieves a webhook by ID.
                TenantApiWebhookV1WebhookResponse result = apiInstance.GetWebhookByIdAsync(tenantId, webhookId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.GetWebhookByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetWebhookByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a webhook by ID.
    ApiResponse<TenantApiWebhookV1WebhookResponse> response = apiInstance.GetWebhookByIdAsyncWithHttpInfo(tenantId, webhookId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.GetWebhookByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **webhookId** | **string** |  |  |

### Return type

[**TenantApiWebhookV1WebhookResponse**](TenantApiWebhookV1WebhookResponse.md)

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

<a id="updatewebhookasync"></a>
# **UpdateWebhookAsync**
> TenantApiWebhookV1WebhookIdResponse UpdateWebhookAsync (string tenantId, string webhookId, TenantApiWebhookV1UpdateWebhookRequest tenantApiWebhookV1UpdateWebhookRequest = null)

Updates a webhook

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateWebhookAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new WebhooksApi(config);
            var tenantId = "tenantId_example";  // string | 
            var webhookId = "webhookId_example";  // string | 
            var tenantApiWebhookV1UpdateWebhookRequest = new TenantApiWebhookV1UpdateWebhookRequest(); // TenantApiWebhookV1UpdateWebhookRequest |  (optional) 

            try
            {
                // Updates a webhook
                TenantApiWebhookV1WebhookIdResponse result = apiInstance.UpdateWebhookAsync(tenantId, webhookId, tenantApiWebhookV1UpdateWebhookRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling WebhooksApi.UpdateWebhookAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateWebhookAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a webhook
    ApiResponse<TenantApiWebhookV1WebhookIdResponse> response = apiInstance.UpdateWebhookAsyncWithHttpInfo(tenantId, webhookId, tenantApiWebhookV1UpdateWebhookRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling WebhooksApi.UpdateWebhookAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **webhookId** | **string** |  |  |
| **tenantApiWebhookV1UpdateWebhookRequest** | [**TenantApiWebhookV1UpdateWebhookRequest**](TenantApiWebhookV1UpdateWebhookRequest.md) |  | [optional]  |

### Return type

[**TenantApiWebhookV1WebhookIdResponse**](TenantApiWebhookV1WebhookIdResponse.md)

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

