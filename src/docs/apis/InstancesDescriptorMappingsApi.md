# EdGraph.Platform.Client.Api.InstancesDescriptorMappingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateDescriptorMapping**](InstancesDescriptorMappingsApi.md#createdescriptormapping) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Creates a Descriptor Mapping. |
| [**DeleteDescriptorMapping**](InstancesDescriptorMappingsApi.md#deletedescriptormapping) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Deletes a Descriptor Mapping. |
| [**GetDescriptorMappingById**](InstancesDescriptorMappingsApi.md#getdescriptormappingbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Retrieves a Descriptor Mapping by ID. |
| [**GetDescriptorMappings**](InstancesDescriptorMappingsApi.md#getdescriptormappings) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings | Retrieves a list of Descriptors Mappings. |
| [**UpdateDescriptorMapping**](InstancesDescriptorMappingsApi.md#updatedescriptormapping) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/descriptorMappings/{descriptorMappingId} | Updates a Descriptor Mapping. |

<a id="createdescriptormapping"></a>
# **CreateDescriptorMapping**
> EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse CreateDescriptorMapping (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest = null)

Creates a Descriptor Mapping.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateDescriptorMappingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorMappingsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest = new EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest(); // EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest |  (optional) 

            try
            {
                // Creates a Descriptor Mapping.
                EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse result = apiInstance.CreateDescriptorMapping(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorMappingsApi.CreateDescriptorMapping: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateDescriptorMappingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a Descriptor Mapping.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse> response = apiInstance.CreateDescriptorMappingWithHttpInfo(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorMappingsApi.CreateDescriptorMappingWithHttpInfo: " + e.Message);
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
| **edfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest** | [**EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest**](EdfiAdminApiEdfiAdminV1CreateDescriptorMappingRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorMappingCreatedResponse.md)

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

<a id="deletedescriptormapping"></a>
# **DeleteDescriptorMapping**
> void DeleteDescriptorMapping (string tenantId, string instanceId, int year, string descriptorMappingId)

Deletes a Descriptor Mapping.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteDescriptorMappingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorMappingsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var descriptorMappingId = "descriptorMappingId_example";  // string | 

            try
            {
                // Deletes a Descriptor Mapping.
                apiInstance.DeleteDescriptorMapping(tenantId, instanceId, year, descriptorMappingId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorMappingsApi.DeleteDescriptorMapping: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteDescriptorMappingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Descriptor Mapping.
    apiInstance.DeleteDescriptorMappingWithHttpInfo(tenantId, instanceId, year, descriptorMappingId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorMappingsApi.DeleteDescriptorMappingWithHttpInfo: " + e.Message);
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
| **descriptorMappingId** | **string** |  |  |

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

<a id="getdescriptormappingbyid"></a>
# **GetDescriptorMappingById**
> EdfiAdminApiEdfiAdminV1DescriptorMapping GetDescriptorMappingById (string tenantId, string instanceId, int year, string descriptorMappingId)

Retrieves a Descriptor Mapping by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetDescriptorMappingByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorMappingsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var descriptorMappingId = "descriptorMappingId_example";  // string | 

            try
            {
                // Retrieves a Descriptor Mapping by ID.
                EdfiAdminApiEdfiAdminV1DescriptorMapping result = apiInstance.GetDescriptorMappingById(tenantId, instanceId, year, descriptorMappingId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorMappingsApi.GetDescriptorMappingById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDescriptorMappingByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Descriptor Mapping by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorMapping> response = apiInstance.GetDescriptorMappingByIdWithHttpInfo(tenantId, instanceId, year, descriptorMappingId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorMappingsApi.GetDescriptorMappingByIdWithHttpInfo: " + e.Message);
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
| **descriptorMappingId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMapping**](EdfiAdminApiEdfiAdminV1DescriptorMapping.md)

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

<a id="getdescriptormappings"></a>
# **GetDescriptorMappings**
> EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse GetDescriptorMappings (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null, string varNamespace = null)

Retrieves a list of Descriptors Mappings.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetDescriptorMappingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorMappingsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var varNamespace = "varNamespace_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Descriptors Mappings.
                EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse result = apiInstance.GetDescriptorMappings(tenantId, instanceId, year, pageSize, pageIndex, varNamespace);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorMappingsApi.GetDescriptorMappings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDescriptorMappingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Descriptors Mappings.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse> response = apiInstance.GetDescriptorMappingsWithHttpInfo(tenantId, instanceId, year, pageSize, pageIndex, varNamespace);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorMappingsApi.GetDescriptorMappingsWithHttpInfo: " + e.Message);
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
| **varNamespace** | **string** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse**](EdfiAdminApiEdfiAdminV1DescriptorMappingsPaginatedItemsResponse.md)

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

<a id="updatedescriptormapping"></a>
# **UpdateDescriptorMapping**
> EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse UpdateDescriptorMapping (string tenantId, string instanceId, int year, string descriptorMappingId, EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest = null)

Updates a Descriptor Mapping.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateDescriptorMappingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesDescriptorMappingsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var descriptorMappingId = "descriptorMappingId_example";  // string | 
            var edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest = new EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest(); // EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest |  (optional) 

            try
            {
                // Updates a Descriptor Mapping.
                EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse result = apiInstance.UpdateDescriptorMapping(tenantId, instanceId, year, descriptorMappingId, edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesDescriptorMappingsApi.UpdateDescriptorMapping: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateDescriptorMappingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Descriptor Mapping.
    ApiResponse<EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse> response = apiInstance.UpdateDescriptorMappingWithHttpInfo(tenantId, instanceId, year, descriptorMappingId, edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesDescriptorMappingsApi.UpdateDescriptorMappingWithHttpInfo: " + e.Message);
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
| **descriptorMappingId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest** | [**EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest**](EdfiAdminApiEdfiAdminV1UpdateDescriptorMappingRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse**](EdfiAdminApiEdfiAdminV1DescriptorMappingUpdatedResponse.md)

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

