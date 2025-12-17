# EdGraph.Platform.Client.Api.EnvironmentsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEnvironment**](EnvironmentsApi.md#createenvironment) | **POST** /tenants/{tenantId}/validations/environments | Creates an Environment. |
| [**DeleteEnvironment**](EnvironmentsApi.md#deleteenvironment) | **DELETE** /tenants/{tenantId}/validations/environments/{environmentId} | Deletes an Environment. |
| [**GetEnvironmentById**](EnvironmentsApi.md#getenvironmentbyid) | **GET** /tenants/{tenantId}/validations/environments/{environmentId} | Retrieves an Environment by ID. |
| [**GetEnvironments**](EnvironmentsApi.md#getenvironments) | **GET** /tenants/{tenantId}/validations/environments | Retrieves a list of Environments. |
| [**TestEnvironmentConnection**](EnvironmentsApi.md#testenvironmentconnection) | **POST** /tenants/{tenantId}/validations/environments/testconnection | Tests if the provided connection string can establish a valid connection. |
| [**UpdateEnvironment**](EnvironmentsApi.md#updateenvironment) | **PUT** /tenants/{tenantId}/validations/environments/{environmentId} | Updates an Environment. |

<a id="createenvironment"></a>
# **CreateEnvironment**
> ValidationsApiCoreV1CreatedResponse CreateEnvironment (string tenantId, ValidationsApiDbEnvironmentsV1CreateRequest validationsApiDbEnvironmentsV1CreateRequest = null)

Creates an Environment.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateEnvironmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var validationsApiDbEnvironmentsV1CreateRequest = new ValidationsApiDbEnvironmentsV1CreateRequest(); // ValidationsApiDbEnvironmentsV1CreateRequest |  (optional) 

            try
            {
                // Creates an Environment.
                ValidationsApiCoreV1CreatedResponse result = apiInstance.CreateEnvironment(tenantId, validationsApiDbEnvironmentsV1CreateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsApi.CreateEnvironment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEnvironmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Environment.
    ApiResponse<ValidationsApiCoreV1CreatedResponse> response = apiInstance.CreateEnvironmentWithHttpInfo(tenantId, validationsApiDbEnvironmentsV1CreateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsApi.CreateEnvironmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **validationsApiDbEnvironmentsV1CreateRequest** | [**ValidationsApiDbEnvironmentsV1CreateRequest**](ValidationsApiDbEnvironmentsV1CreateRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiCoreV1CreatedResponse**](ValidationsApiCoreV1CreatedResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteenvironment"></a>
# **DeleteEnvironment**
> void DeleteEnvironment (string tenantId, string environmentId)

Deletes an Environment.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteEnvironmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var environmentId = "environmentId_example";  // string | 

            try
            {
                // Deletes an Environment.
                apiInstance.DeleteEnvironment(tenantId, environmentId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsApi.DeleteEnvironment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteEnvironmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an Environment.
    apiInstance.DeleteEnvironmentWithHttpInfo(tenantId, environmentId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsApi.DeleteEnvironmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **environmentId** | **string** |  |  |

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

<a id="getenvironmentbyid"></a>
# **GetEnvironmentById**
> ValidationsApiDbEnvironmentsV1DbEnvironmentDto GetEnvironmentById (string tenantId, string environmentId)

Retrieves an Environment by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEnvironmentByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var environmentId = "environmentId_example";  // string | 

            try
            {
                // Retrieves an Environment by ID.
                ValidationsApiDbEnvironmentsV1DbEnvironmentDto result = apiInstance.GetEnvironmentById(tenantId, environmentId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsApi.GetEnvironmentById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEnvironmentByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an Environment by ID.
    ApiResponse<ValidationsApiDbEnvironmentsV1DbEnvironmentDto> response = apiInstance.GetEnvironmentByIdWithHttpInfo(tenantId, environmentId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsApi.GetEnvironmentByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **environmentId** | **string** |  |  |

### Return type

[**ValidationsApiDbEnvironmentsV1DbEnvironmentDto**](ValidationsApiDbEnvironmentsV1DbEnvironmentDto.md)

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

<a id="getenvironments"></a>
# **GetEnvironments**
> ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments GetEnvironments (string tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Environments.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEnvironmentsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "filter_example";  // string |  (optional) 
            var orderBy = "orderBy_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Environments.
                ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments result = apiInstance.GetEnvironments(tenantId, pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsApi.GetEnvironments: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEnvironmentsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Environments.
    ApiResponse<ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments> response = apiInstance.GetEnvironmentsWithHttpInfo(tenantId, pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsApi.GetEnvironmentsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments**](ValidationsApiDbEnvironmentsV1PaginatedDbEnvironments.md)

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

<a id="testenvironmentconnection"></a>
# **TestEnvironmentConnection**
> ValidationsApiDbEnvironmentsV1TestConnectionResponse TestEnvironmentConnection (string tenantId, ValidationsApiDbEnvironmentsV1TestConnectionRequest validationsApiDbEnvironmentsV1TestConnectionRequest = null)

Tests if the provided connection string can establish a valid connection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestEnvironmentConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var validationsApiDbEnvironmentsV1TestConnectionRequest = new ValidationsApiDbEnvironmentsV1TestConnectionRequest(); // ValidationsApiDbEnvironmentsV1TestConnectionRequest |  (optional) 

            try
            {
                // Tests if the provided connection string can establish a valid connection.
                ValidationsApiDbEnvironmentsV1TestConnectionResponse result = apiInstance.TestEnvironmentConnection(tenantId, validationsApiDbEnvironmentsV1TestConnectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsApi.TestEnvironmentConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestEnvironmentConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests if the provided connection string can establish a valid connection.
    ApiResponse<ValidationsApiDbEnvironmentsV1TestConnectionResponse> response = apiInstance.TestEnvironmentConnectionWithHttpInfo(tenantId, validationsApiDbEnvironmentsV1TestConnectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsApi.TestEnvironmentConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **validationsApiDbEnvironmentsV1TestConnectionRequest** | [**ValidationsApiDbEnvironmentsV1TestConnectionRequest**](ValidationsApiDbEnvironmentsV1TestConnectionRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiDbEnvironmentsV1TestConnectionResponse**](ValidationsApiDbEnvironmentsV1TestConnectionResponse.md)

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

<a id="updateenvironment"></a>
# **UpdateEnvironment**
> Object UpdateEnvironment (string tenantId, string environmentId, ValidationsApiDbEnvironmentsV1UpdateRequest validationsApiDbEnvironmentsV1UpdateRequest = null)

Updates an Environment.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateEnvironmentExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var environmentId = "environmentId_example";  // string | 
            var validationsApiDbEnvironmentsV1UpdateRequest = new ValidationsApiDbEnvironmentsV1UpdateRequest(); // ValidationsApiDbEnvironmentsV1UpdateRequest |  (optional) 

            try
            {
                // Updates an Environment.
                Object result = apiInstance.UpdateEnvironment(tenantId, environmentId, validationsApiDbEnvironmentsV1UpdateRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsApi.UpdateEnvironment: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEnvironmentWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Environment.
    ApiResponse<Object> response = apiInstance.UpdateEnvironmentWithHttpInfo(tenantId, environmentId, validationsApiDbEnvironmentsV1UpdateRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsApi.UpdateEnvironmentWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **environmentId** | **string** |  |  |
| **validationsApiDbEnvironmentsV1UpdateRequest** | [**ValidationsApiDbEnvironmentsV1UpdateRequest**](ValidationsApiDbEnvironmentsV1UpdateRequest.md) |  | [optional]  |

### Return type

**Object**

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

