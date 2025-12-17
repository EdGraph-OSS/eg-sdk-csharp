# EdGraph.Platform.Client.Api.InstancesClaimSetsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateClaimSetAsync**](InstancesClaimSetsApi.md#createclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Creates a ClaimSet. |
| [**DeleteClaimSetAsync**](InstancesClaimSetsApi.md#deleteclaimsetasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Deletes a ClaimSet. |
| [**GetClaimSetByIdAsync**](InstancesClaimSetsApi.md#getclaimsetbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Retrieves a ClaimSet by ID. |
| [**GetClaimSetsAsync**](InstancesClaimSetsApi.md#getclaimsetsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Retrieves a list of ClaimSets. |
| [**GetResourceClaimsGridAsync**](InstancesClaimSetsApi.md#getresourceclaimsgridasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/resourceclaims | Retrieves a grid of Resource Claims. |
| [**SyncClaimSetAsync**](InstancesClaimSetsApi.md#syncclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/sync | Copies a Claim Set from one instance to another/other instance(s) |
| [**UpdateClaimSetAsync**](InstancesClaimSetsApi.md#updateclaimsetasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Updates a ClaimSet. |

<a id="createclaimsetasync"></a>
# **CreateClaimSetAsync**
> EdfiAdminApiEdfiAdminV1SaveClaimSetResponse CreateClaimSetAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1SaveClaimSetRequest edfiAdminApiEdfiAdminV1SaveClaimSetRequest = null)

Creates a ClaimSet.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateClaimSetAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClaimSetsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1SaveClaimSetRequest = new EdfiAdminApiEdfiAdminV1SaveClaimSetRequest(); // EdfiAdminApiEdfiAdminV1SaveClaimSetRequest |  (optional) 

            try
            {
                // Creates a ClaimSet.
                EdfiAdminApiEdfiAdminV1SaveClaimSetResponse result = apiInstance.CreateClaimSetAsync(tenantId, instanceId, edfiAdminApiEdfiAdminV1SaveClaimSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClaimSetsApi.CreateClaimSetAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateClaimSetAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a ClaimSet.
    ApiResponse<EdfiAdminApiEdfiAdminV1SaveClaimSetResponse> response = apiInstance.CreateClaimSetAsyncWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1SaveClaimSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClaimSetsApi.CreateClaimSetAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1SaveClaimSetRequest** | [**EdfiAdminApiEdfiAdminV1SaveClaimSetRequest**](EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SaveClaimSetResponse**](EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)

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

<a id="deleteclaimsetasync"></a>
# **DeleteClaimSetAsync**
> void DeleteClaimSetAsync (string tenantId, string instanceId, int claimSetId)

Deletes a ClaimSet.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteClaimSetAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClaimSetsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var claimSetId = 56;  // int | 

            try
            {
                // Deletes a ClaimSet.
                apiInstance.DeleteClaimSetAsync(tenantId, instanceId, claimSetId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClaimSetsApi.DeleteClaimSetAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteClaimSetAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a ClaimSet.
    apiInstance.DeleteClaimSetAsyncWithHttpInfo(tenantId, instanceId, claimSetId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClaimSetsApi.DeleteClaimSetAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getclaimsetbyidasync"></a>
# **GetClaimSetByIdAsync**
> EdfiAdminApiEdfiAdminV1ClaimSet GetClaimSetByIdAsync (string tenantId, string instanceId, int claimSetId)

Retrieves a ClaimSet by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetClaimSetByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClaimSetsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var claimSetId = 56;  // int | 

            try
            {
                // Retrieves a ClaimSet by ID.
                EdfiAdminApiEdfiAdminV1ClaimSet result = apiInstance.GetClaimSetByIdAsync(tenantId, instanceId, claimSetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClaimSetsApi.GetClaimSetByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetClaimSetByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a ClaimSet by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1ClaimSet> response = apiInstance.GetClaimSetByIdAsyncWithHttpInfo(tenantId, instanceId, claimSetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClaimSetsApi.GetClaimSetByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1ClaimSet**](EdfiAdminApiEdfiAdminV1ClaimSet.md)

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

<a id="getclaimsetsasync"></a>
# **GetClaimSetsAsync**
> EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel GetClaimSetsAsync (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of ClaimSets.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetClaimSetsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClaimSetsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of ClaimSets.
                EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel result = apiInstance.GetClaimSetsAsync(tenantId, instanceId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClaimSetsApi.GetClaimSetsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetClaimSetsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of ClaimSets.
    ApiResponse<EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel> response = apiInstance.GetClaimSetsAsyncWithHttpInfo(tenantId, instanceId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClaimSetsApi.GetClaimSetsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel.md)

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

<a id="getresourceclaimsgridasync"></a>
# **GetResourceClaimsGridAsync**
> EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse GetResourceClaimsGridAsync (string tenantId, string instanceId, int claimSetId)

Retrieves a grid of Resource Claims.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetResourceClaimsGridAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClaimSetsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var claimSetId = 56;  // int | 

            try
            {
                // Retrieves a grid of Resource Claims.
                EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse result = apiInstance.GetResourceClaimsGridAsync(tenantId, instanceId, claimSetId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClaimSetsApi.GetResourceClaimsGridAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetResourceClaimsGridAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a grid of Resource Claims.
    ApiResponse<EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse> response = apiInstance.GetResourceClaimsGridAsyncWithHttpInfo(tenantId, instanceId, claimSetId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClaimSetsApi.GetResourceClaimsGridAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse**](EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse.md)

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

<a id="syncclaimsetasync"></a>
# **SyncClaimSetAsync**
> void SyncClaimSetAsync (string tenantId, string instanceId, int claimSetId, EdfiAdminApiEdfiAdminV1SyncClaimSetRequest edfiAdminApiEdfiAdminV1SyncClaimSetRequest = null)

Copies a Claim Set from one instance to another/other instance(s)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SyncClaimSetAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClaimSetsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var claimSetId = 56;  // int | 
            var edfiAdminApiEdfiAdminV1SyncClaimSetRequest = new EdfiAdminApiEdfiAdminV1SyncClaimSetRequest(); // EdfiAdminApiEdfiAdminV1SyncClaimSetRequest |  (optional) 

            try
            {
                // Copies a Claim Set from one instance to another/other instance(s)
                apiInstance.SyncClaimSetAsync(tenantId, instanceId, claimSetId, edfiAdminApiEdfiAdminV1SyncClaimSetRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClaimSetsApi.SyncClaimSetAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SyncClaimSetAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Copies a Claim Set from one instance to another/other instance(s)
    apiInstance.SyncClaimSetAsyncWithHttpInfo(tenantId, instanceId, claimSetId, edfiAdminApiEdfiAdminV1SyncClaimSetRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClaimSetsApi.SyncClaimSetAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SyncClaimSetRequest** | [**EdfiAdminApiEdfiAdminV1SyncClaimSetRequest**](EdfiAdminApiEdfiAdminV1SyncClaimSetRequest.md) |  | [optional]  |

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
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateclaimsetasync"></a>
# **UpdateClaimSetAsync**
> EdfiAdminApiEdfiAdminV1SaveClaimSetResponse UpdateClaimSetAsync (string tenantId, string instanceId, int claimSetId, EdfiAdminApiEdfiAdminV1SaveClaimSetRequest edfiAdminApiEdfiAdminV1SaveClaimSetRequest = null)

Updates a ClaimSet.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateClaimSetAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClaimSetsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var claimSetId = 56;  // int | 
            var edfiAdminApiEdfiAdminV1SaveClaimSetRequest = new EdfiAdminApiEdfiAdminV1SaveClaimSetRequest(); // EdfiAdminApiEdfiAdminV1SaveClaimSetRequest |  (optional) 

            try
            {
                // Updates a ClaimSet.
                EdfiAdminApiEdfiAdminV1SaveClaimSetResponse result = apiInstance.UpdateClaimSetAsync(tenantId, instanceId, claimSetId, edfiAdminApiEdfiAdminV1SaveClaimSetRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClaimSetsApi.UpdateClaimSetAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateClaimSetAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a ClaimSet.
    ApiResponse<EdfiAdminApiEdfiAdminV1SaveClaimSetResponse> response = apiInstance.UpdateClaimSetAsyncWithHttpInfo(tenantId, instanceId, claimSetId, edfiAdminApiEdfiAdminV1SaveClaimSetRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClaimSetsApi.UpdateClaimSetAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SaveClaimSetRequest** | [**EdfiAdminApiEdfiAdminV1SaveClaimSetRequest**](EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SaveClaimSetResponse**](EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)

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

