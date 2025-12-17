# EdGraph.Platform.Client.Api.InstancesApplicationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateApplicationAsync**](InstancesApplicationsApi.md#createapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Creates an Application. |
| [**CreateApplicationUserAccessAsync**](InstancesApplicationsApi.md#createapplicationuseraccessasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Creates a new application access. |
| [**DeleteApplicationAsync**](InstancesApplicationsApi.md#deleteapplicationasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Deletes an Application. |
| [**DeleteApplicationUserAccessAsync**](InstancesApplicationsApi.md#deleteapplicationuseraccessasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Deletes an application user access. |
| [**GetApplicationAccessAsync**](InstancesApplicationsApi.md#getapplicationaccessasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access | Retrieves a list of application accesses. |
| [**GetApplicationAccessByIdAsync**](InstancesApplicationsApi.md#getapplicationaccessbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Retrieves an application access by ID. |
| [**GetApplicationApiClientByIdAsync**](InstancesApplicationsApi.md#getapplicationapiclientbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId} | Retrieves an API Client of an Application by ID. |
| [**GetApplicationApiClientsAsync**](InstancesApplicationsApi.md#getapplicationapiclientsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients | Retrieves the API Clients of an Application. |
| [**GetApplicationByIdAsync**](InstancesApplicationsApi.md#getapplicationbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Retrieves an Application by ID. |
| [**GetApplicationsAsync**](InstancesApplicationsApi.md#getapplicationsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications | Retrieves a list of Applications. |
| [**RegenerateApiClientSecretAsync**](InstancesApplicationsApi.md#regenerateapiclientsecretasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/regenerate | Regenerates the secret of an API Client. |
| [**SyncApplicationAsync**](InstancesApplicationsApi.md#syncapplicationasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/sync | Copies an Application from one instance to another/other instance(s) |
| [**UpdateApplicationAsync**](InstancesApplicationsApi.md#updateapplicationasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId} | Updates an Application. |
| [**UpdateApplicationUserAccessAsync**](InstancesApplicationsApi.md#updateapplicationuseraccessasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/applications/{applicationId}/apiclients/{apiClientId}/access/{accessId} | Updates a new application access. |

<a id="createapplicationasync"></a>
# **CreateApplicationAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse CreateApplicationAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest = null)

Creates an Application.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateApplicationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest = new EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest(); // EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest |  (optional) 

            try
            {
                // Creates an Application.
                EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse result = apiInstance.CreateApplicationAsync(tenantId, instanceId, edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.CreateApplicationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateApplicationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Application.
    ApiResponse<EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse> response = apiInstance.CreateApplicationAsyncWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.CreateApplicationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest** | [**EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest**](EdfiAdminApiEdfiAdminV1CreateEdFiApplicationRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse**](EdfiAdminApiEdfiAdminV1EdFiApplicationCreatedResponse.md)

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

<a id="createapplicationuseraccessasync"></a>
# **CreateApplicationUserAccessAsync**
> void CreateApplicationUserAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest = null)

Creates a new application access.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateApplicationUserAccessAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = "apiClientId_example";  // string | 
            var edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest = new EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest(); // EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest |  (optional) 

            try
            {
                // Creates a new application access.
                apiInstance.CreateApplicationUserAccessAsync(tenantId, instanceId, applicationId, apiClientId, edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.CreateApplicationUserAccessAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateApplicationUserAccessAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new application access.
    apiInstance.CreateApplicationUserAccessAsyncWithHttpInfo(tenantId, instanceId, applicationId, apiClientId, edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.CreateApplicationUserAccessAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **edFiAdminApiApplicationAccessV1CreateApplicationAccessRequest** | [**EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest**](EdFiAdminApiApplicationAccessV1CreateApplicationAccessRequest.md) |  | [optional]  |

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteapplicationasync"></a>
# **DeleteApplicationAsync**
> void DeleteApplicationAsync (string tenantId, string instanceId, int applicationId)

Deletes an Application.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteApplicationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = 56;  // int | 

            try
            {
                // Deletes an Application.
                apiInstance.DeleteApplicationAsync(tenantId, instanceId, applicationId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.DeleteApplicationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteApplicationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an Application.
    apiInstance.DeleteApplicationAsyncWithHttpInfo(tenantId, instanceId, applicationId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.DeleteApplicationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |

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

<a id="deleteapplicationuseraccessasync"></a>
# **DeleteApplicationUserAccessAsync**
> void DeleteApplicationUserAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, string accessId)

Deletes an application user access.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteApplicationUserAccessAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = "apiClientId_example";  // string | 
            var accessId = "accessId_example";  // string | 

            try
            {
                // Deletes an application user access.
                apiInstance.DeleteApplicationUserAccessAsync(tenantId, instanceId, applicationId, apiClientId, accessId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.DeleteApplicationUserAccessAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteApplicationUserAccessAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an application user access.
    apiInstance.DeleteApplicationUserAccessAsyncWithHttpInfo(tenantId, instanceId, applicationId, apiClientId, accessId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.DeleteApplicationUserAccessAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **accessId** | **string** |  |  |

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

<a id="getapplicationaccessasync"></a>
# **GetApplicationAccessAsync**
> EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel GetApplicationAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of application accesses.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetApplicationAccessAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = "apiClientId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of application accesses.
                EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel result = apiInstance.GetApplicationAccessAsync(tenantId, instanceId, applicationId, apiClientId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationAccessAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApplicationAccessAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of application accesses.
    ApiResponse<EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel> response = apiInstance.GetApplicationAccessAsyncWithHttpInfo(tenantId, instanceId, applicationId, apiClientId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationAccessAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel**](EdFiAdminApiApplicationAccessV1ApplicationAccessResponsePaginatedItemsViewModel.md)

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

<a id="getapplicationaccessbyidasync"></a>
# **GetApplicationAccessByIdAsync**
> EdFiAdminApiApplicationAccessV1ApplicationAccessResponse GetApplicationAccessByIdAsync (string tenantId, string instanceId, int applicationId, int apiClientId, string accessId)

Retrieves an application access by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetApplicationAccessByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = 56;  // int | 
            var apiClientId = 56;  // int | 
            var accessId = "accessId_example";  // string | 

            try
            {
                // Retrieves an application access by ID.
                EdFiAdminApiApplicationAccessV1ApplicationAccessResponse result = apiInstance.GetApplicationAccessByIdAsync(tenantId, instanceId, applicationId, apiClientId, accessId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationAccessByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApplicationAccessByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an application access by ID.
    ApiResponse<EdFiAdminApiApplicationAccessV1ApplicationAccessResponse> response = apiInstance.GetApplicationAccessByIdAsyncWithHttpInfo(tenantId, instanceId, applicationId, apiClientId, accessId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationAccessByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **apiClientId** | **int** |  |  |
| **accessId** | **string** |  |  |

### Return type

[**EdFiAdminApiApplicationAccessV1ApplicationAccessResponse**](EdFiAdminApiApplicationAccessV1ApplicationAccessResponse.md)

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

<a id="getapplicationapiclientbyidasync"></a>
# **GetApplicationApiClientByIdAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse GetApplicationApiClientByIdAsync (string tenantId, string instanceId, string applicationId, int apiClientId)

Retrieves an API Client of an Application by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetApplicationApiClientByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = 56;  // int | 

            try
            {
                // Retrieves an API Client of an Application by ID.
                EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse result = apiInstance.GetApplicationApiClientByIdAsync(tenantId, instanceId, applicationId, apiClientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationApiClientByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApplicationApiClientByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an API Client of an Application by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse> response = apiInstance.GetApplicationApiClientByIdAsyncWithHttpInfo(tenantId, instanceId, applicationId, apiClientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationApiClientByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse**](EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponse.md)

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

<a id="getapplicationapiclientsasync"></a>
# **GetApplicationApiClientsAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel GetApplicationApiClientsAsync (string tenantId, string instanceId, string applicationId)

Retrieves the API Clients of an Application.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetApplicationApiClientsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 

            try
            {
                // Retrieves the API Clients of an Application.
                EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel result = apiInstance.GetApplicationApiClientsAsync(tenantId, instanceId, applicationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationApiClientsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApplicationApiClientsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the API Clients of an Application.
    ApiResponse<EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel> response = apiInstance.GetApplicationApiClientsAsyncWithHttpInfo(tenantId, instanceId, applicationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationApiClientsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1EdFiApplicationApiClientProfileResponsePaginatedItemsViewModel.md)

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

<a id="getapplicationbyidasync"></a>
# **GetApplicationByIdAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse GetApplicationByIdAsync (string tenantId, string instanceId, int applicationId, int year = null)

Retrieves an Application by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetApplicationByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = 56;  // int | 
            var year = 56;  // int |  (optional) 

            try
            {
                // Retrieves an Application by ID.
                EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse result = apiInstance.GetApplicationByIdAsync(tenantId, instanceId, applicationId, year);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApplicationByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an Application by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse> response = apiInstance.GetApplicationByIdAsyncWithHttpInfo(tenantId, instanceId, applicationId, year);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **year** | **int** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse**](EdfiAdminApiEdfiAdminV1EdFiApplicationProfileResponse.md)

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

<a id="getapplicationsasync"></a>
# **GetApplicationsAsync**
> EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel GetApplicationsAsync (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Applications.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetApplicationsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of Applications.
                EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel result = apiInstance.GetApplicationsAsync(tenantId, instanceId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApplicationsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Applications.
    ApiResponse<EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel> response = apiInstance.GetApplicationsAsyncWithHttpInfo(tenantId, instanceId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.GetApplicationsAsyncWithHttpInfo: " + e.Message);
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

[**EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1EdFiApplicationListResponsePaginatedItemsViewModel.md)

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

<a id="regenerateapiclientsecretasync"></a>
# **RegenerateApiClientSecretAsync**
> EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse RegenerateApiClientSecretAsync (string tenantId, string instanceId, int applicationId, int apiClientId)

Regenerates the secret of an API Client.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RegenerateApiClientSecretAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = 56;  // int | 
            var apiClientId = 56;  // int | 

            try
            {
                // Regenerates the secret of an API Client.
                EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse result = apiInstance.RegenerateApiClientSecretAsync(tenantId, instanceId, applicationId, apiClientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.RegenerateApiClientSecretAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RegenerateApiClientSecretAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Regenerates the secret of an API Client.
    ApiResponse<EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse> response = apiInstance.RegenerateApiClientSecretAsyncWithHttpInfo(tenantId, instanceId, applicationId, apiClientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.RegenerateApiClientSecretAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **apiClientId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse**](EdfiAdminApiEdfiAdminV1RegenerateApiClientSecretResponse.md)

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

<a id="syncapplicationasync"></a>
# **SyncApplicationAsync**
> void SyncApplicationAsync (string tenantId, string instanceId, int applicationId, EdfiAdminApiEdfiAdminV1SyncApplicationRequest edfiAdminApiEdfiAdminV1SyncApplicationRequest = null)

Copies an Application from one instance to another/other instance(s)

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SyncApplicationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = 56;  // int | 
            var edfiAdminApiEdfiAdminV1SyncApplicationRequest = new EdfiAdminApiEdfiAdminV1SyncApplicationRequest(); // EdfiAdminApiEdfiAdminV1SyncApplicationRequest |  (optional) 

            try
            {
                // Copies an Application from one instance to another/other instance(s)
                apiInstance.SyncApplicationAsync(tenantId, instanceId, applicationId, edfiAdminApiEdfiAdminV1SyncApplicationRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.SyncApplicationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SyncApplicationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Copies an Application from one instance to another/other instance(s)
    apiInstance.SyncApplicationAsyncWithHttpInfo(tenantId, instanceId, applicationId, edfiAdminApiEdfiAdminV1SyncApplicationRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.SyncApplicationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SyncApplicationRequest** | [**EdfiAdminApiEdfiAdminV1SyncApplicationRequest**](EdfiAdminApiEdfiAdminV1SyncApplicationRequest.md) |  | [optional]  |

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

<a id="updateapplicationasync"></a>
# **UpdateApplicationAsync**
> void UpdateApplicationAsync (string tenantId, string instanceId, string applicationId, EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest = null)

Updates an Application.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateApplicationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest = new EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest(); // EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest |  (optional) 

            try
            {
                // Updates an Application.
                apiInstance.UpdateApplicationAsync(tenantId, instanceId, applicationId, edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.UpdateApplicationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateApplicationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Application.
    apiInstance.UpdateApplicationAsyncWithHttpInfo(tenantId, instanceId, applicationId, edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.UpdateApplicationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest** | [**EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest**](EdfiAdminApiEdfiAdminV1UpdateEdFiApplicationRequest.md) |  | [optional]  |

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

<a id="updateapplicationuseraccessasync"></a>
# **UpdateApplicationUserAccessAsync**
> void UpdateApplicationUserAccessAsync (string tenantId, string instanceId, string applicationId, string apiClientId, string accessId, EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest = null)

Updates a new application access.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateApplicationUserAccessAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApplicationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = "apiClientId_example";  // string | 
            var accessId = "accessId_example";  // string | 
            var edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest = new EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest(); // EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest |  (optional) 

            try
            {
                // Updates a new application access.
                apiInstance.UpdateApplicationUserAccessAsync(tenantId, instanceId, applicationId, apiClientId, accessId, edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApplicationsApi.UpdateApplicationUserAccessAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateApplicationUserAccessAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a new application access.
    apiInstance.UpdateApplicationUserAccessAsyncWithHttpInfo(tenantId, instanceId, applicationId, apiClientId, accessId, edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApplicationsApi.UpdateApplicationUserAccessAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **apiClientId** | **string** |  |  |
| **accessId** | **string** |  |  |
| **edFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest** | [**EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest**](EdFiAdminApiApplicationAccessV1UpdateApplicationAccessRequest.md) |  | [optional]  |

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

