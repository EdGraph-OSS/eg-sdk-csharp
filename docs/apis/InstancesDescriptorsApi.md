# EdGraph.Platform.Client.Api.InstancesDescriptorsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDescriptorAsync**](InstancesDescriptorsApi.md#createdescriptorasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Creates a Descriptor. |
| [**DeleteDescriptorAsync**](InstancesDescriptorsApi.md#deletedescriptorasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Deletes a Descriptor. |
| [**GetDescriptorByIdAsync**](InstancesDescriptorsApi.md#getdescriptorbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Retrieves a Descriptor by ID. |
| [**GetDescriptorNamespacesAsync**](InstancesDescriptorsApi.md#getdescriptornamespacesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/namespaces | Retrieves a list of Descriptor Namespaces. |
| [**GetDescriptorsAsync**](InstancesDescriptorsApi.md#getdescriptorsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors | Retrieves a list of Descriptors. |
| [**UpdateDescriptorAsync**](InstancesDescriptorsApi.md#updatedescriptorasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptors/{descriptorId} | Updates a Descriptor. |

<a id="createdescriptorasync"></a>
# **CreateDescriptorAsync**
> EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse CreateDescriptorAsync (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1DescriptorType edfiAdminApiEdfiAdminV1DescriptorType = null)

Creates a Descriptor.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateDescriptorAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var edfiAdminApiEdfiAdminV1DescriptorType = new EdfiAdminApiEdfiAdminV1DescriptorType(); // EdfiAdminApiEdfiAdminV1DescriptorType |  (optional) 

            try
            {
                // Creates a Descriptor.
                EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse result = apiInstance.CreateDescriptorAsync(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1DescriptorType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorsApi.CreateDescriptorAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDescriptorAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a Descriptor.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse> response = apiInstance.CreateDescriptorAsyncWithHttpInfo(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1DescriptorType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorsApi.CreateDescriptorAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1DescriptorType** | [**EdfiAdminApiEdfiAdminV1DescriptorType**](EdfiAdminApiEdfiAdminV1DescriptorType.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorCreatedResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletedescriptorasync"></a>
# **DeleteDescriptorAsync**
> void DeleteDescriptorAsync (string tenantId, string instanceId, int year, int descriptorId)

Deletes a Descriptor.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteDescriptorAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var descriptorId = 56;  // int | 

            try
            {
                // Deletes a Descriptor.
                apiInstance.DeleteDescriptorAsync(tenantId, instanceId, year, descriptorId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorsApi.DeleteDescriptorAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDescriptorAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Descriptor.
    apiInstance.DeleteDescriptorAsyncWithHttpInfo(tenantId, instanceId, year, descriptorId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorsApi.DeleteDescriptorAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorId** | **int** |  |  |

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

<a id="getdescriptorbyidasync"></a>
# **GetDescriptorByIdAsync**
> EdfiAdminApiEdfiAdminV1DescriptorType GetDescriptorByIdAsync (string tenantId, string instanceId, int year, int descriptorId)

Retrieves a Descriptor by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetDescriptorByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var descriptorId = 56;  // int | 

            try
            {
                // Retrieves a Descriptor by ID.
                EdfiAdminApiEdfiAdminV1DescriptorType result = apiInstance.GetDescriptorByIdAsync(tenantId, instanceId, year, descriptorId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorsApi.GetDescriptorByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDescriptorByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Descriptor by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorType> response = apiInstance.GetDescriptorByIdAsyncWithHttpInfo(tenantId, instanceId, year, descriptorId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorsApi.GetDescriptorByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorType**](EdfiAdminApiEdfiAdminV1DescriptorType.md)

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

<a id="getdescriptornamespacesasync"></a>
# **GetDescriptorNamespacesAsync**
> EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse GetDescriptorNamespacesAsync (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null)

Retrieves a list of Descriptor Namespaces.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetDescriptorNamespacesAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)

            try
            {
                // Retrieves a list of Descriptor Namespaces.
                EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse result = apiInstance.GetDescriptorNamespacesAsync(tenantId, instanceId, year, pageSize, pageIndex);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorsApi.GetDescriptorNamespacesAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDescriptorNamespacesAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Descriptor Namespaces.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse> response = apiInstance.GetDescriptorNamespacesAsyncWithHttpInfo(tenantId, instanceId, year, pageSize, pageIndex);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorsApi.GetDescriptorNamespacesAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1DescriptorNamespacesPaginatedItemsResponse.md)

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

<a id="getdescriptorsasync"></a>
# **GetDescriptorsAsync**
> EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse GetDescriptorsAsync (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null, string filter = null, string orderBy = null)

Retrieves a list of Descriptors.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetDescriptorsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var filter = "filter_example";  // string |  (optional) 
            var orderBy = "orderBy_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Descriptors.
                EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse result = apiInstance.GetDescriptorsAsync(tenantId, instanceId, year, pageSize, pageIndex, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorsApi.GetDescriptorsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDescriptorsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Descriptors.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse> response = apiInstance.GetDescriptorsAsyncWithHttpInfo(tenantId, instanceId, year, pageSize, pageIndex, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorsApi.GetDescriptorsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1DescriptorsPaginatedItemsResponse.md)

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

<a id="updatedescriptorasync"></a>
# **UpdateDescriptorAsync**
> EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse UpdateDescriptorAsync (string tenantId, string instanceId, int year, int descriptorId, EdfiAdminApiEdfiAdminV1DescriptorType edfiAdminApiEdfiAdminV1DescriptorType = null)

Updates a Descriptor.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateDescriptorAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var descriptorId = 56;  // int | 
            var edfiAdminApiEdfiAdminV1DescriptorType = new EdfiAdminApiEdfiAdminV1DescriptorType(); // EdfiAdminApiEdfiAdminV1DescriptorType |  (optional) 

            try
            {
                // Updates a Descriptor.
                EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse result = apiInstance.UpdateDescriptorAsync(tenantId, instanceId, year, descriptorId, edfiAdminApiEdfiAdminV1DescriptorType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorsApi.UpdateDescriptorAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDescriptorAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Descriptor.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse> response = apiInstance.UpdateDescriptorAsyncWithHttpInfo(tenantId, instanceId, year, descriptorId, edfiAdminApiEdfiAdminV1DescriptorType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorsApi.UpdateDescriptorAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **descriptorId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1DescriptorType** | [**EdfiAdminApiEdfiAdminV1DescriptorType**](EdfiAdminApiEdfiAdminV1DescriptorType.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorUpdatedResponse.md)

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

