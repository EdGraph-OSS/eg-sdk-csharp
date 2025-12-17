# EdGraph.Platform.Client.Api.InstancesInstanceApplicationsAPIClientsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateInstanceApiClient**](InstancesInstanceApplicationsAPIClientsApi.md#createinstanceapiclient) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Creates an Instance ApiClient |
| [**DeleteInstanceApiClient**](InstancesInstanceApplicationsAPIClientsApi.md#deleteinstanceapiclient) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Deletes an Instance ApiClient |
| [**GetInstanceApiClientById**](InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclientbyid) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Retrieves an Instance ApiClient by ID. |
| [**GetInstanceApiClients**](InstancesInstanceApplicationsAPIClientsApi.md#getinstanceapiclients) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients | Retrieves a paginated list of Instance ApiClients |
| [**UpdateInstanceApiClient**](InstancesInstanceApplicationsAPIClientsApi.md#updateinstanceapiclient) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/instanceapplications/{applicationId}/apiclients/{apiClientId} | Updates an Instance Application ApiClient |

<a id="createinstanceapiclient"></a>
# **CreateInstanceApiClient**
> EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse CreateInstanceApiClient (string tenantId, string instanceId, string applicationId, EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest = null)

Creates an Instance ApiClient

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateInstanceApiClientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesInstanceApplicationsAPIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest = new EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest(); // EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest |  (optional) 

            try
            {
                // Creates an Instance ApiClient
                EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse result = apiInstance.CreateInstanceApiClient(tenantId, instanceId, applicationId, edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.CreateInstanceApiClient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInstanceApiClientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Instance ApiClient
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse> response = apiInstance.CreateInstanceApiClientWithHttpInfo(tenantId, instanceId, applicationId, edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.CreateInstanceApiClientWithHttpInfo: " + e.Message);
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
| **edfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest** | [**EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest**](EdfiAdminApiEdfiAdminV1CreateInstanceApiClientRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse**](EdfiAdminApiEdfiAdminV1InstanceApiClientCreatedResponse.md)

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

<a id="deleteinstanceapiclient"></a>
# **DeleteInstanceApiClient**
> void DeleteInstanceApiClient (string tenantId, string instanceId, string applicationId, string apiClientId)

Deletes an Instance ApiClient

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteInstanceApiClientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesInstanceApplicationsAPIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = "apiClientId_example";  // string | 

            try
            {
                // Deletes an Instance ApiClient
                apiInstance.DeleteInstanceApiClient(tenantId, instanceId, applicationId, apiClientId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.DeleteInstanceApiClient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInstanceApiClientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an Instance ApiClient
    apiInstance.DeleteInstanceApiClientWithHttpInfo(tenantId, instanceId, applicationId, apiClientId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.DeleteInstanceApiClientWithHttpInfo: " + e.Message);
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

<a id="getinstanceapiclientbyid"></a>
# **GetInstanceApiClientById**
> EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse GetInstanceApiClientById (string tenantId, string instanceId, string applicationId, string apiClientId)

Retrieves an Instance ApiClient by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstanceApiClientByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesInstanceApplicationsAPIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = "apiClientId_example";  // string | 

            try
            {
                // Retrieves an Instance ApiClient by ID.
                EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse result = apiInstance.GetInstanceApiClientById(tenantId, instanceId, applicationId, apiClientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.GetInstanceApiClientById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstanceApiClientByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an Instance ApiClient by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse> response = apiInstance.GetInstanceApiClientByIdWithHttpInfo(tenantId, instanceId, applicationId, apiClientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.GetInstanceApiClientByIdWithHttpInfo: " + e.Message);
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

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse**](EdfiAdminApiEdfiAdminV1InstanceApiClientProfileResponse.md)

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

<a id="getinstanceapiclients"></a>
# **GetInstanceApiClients**
> EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel GetInstanceApiClients (string tenantId, string instanceId, string applicationId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a paginated list of Instance ApiClients

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstanceApiClientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesInstanceApplicationsAPIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a paginated list of Instance ApiClients
                EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel result = apiInstance.GetInstanceApiClients(tenantId, instanceId, applicationId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.GetInstanceApiClients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstanceApiClientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a paginated list of Instance ApiClients
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel> response = apiInstance.GetInstanceApiClientsWithHttpInfo(tenantId, instanceId, applicationId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.GetInstanceApiClientsWithHttpInfo: " + e.Message);
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
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1InstanceApiClientListResponsePaginatedItemsViewModel.md)

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

<a id="updateinstanceapiclient"></a>
# **UpdateInstanceApiClient**
> EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse UpdateInstanceApiClient (string tenantId, string instanceId, string applicationId, string apiClientId, EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest = null)

Updates an Instance Application ApiClient

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateInstanceApiClientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesInstanceApplicationsAPIClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var applicationId = "applicationId_example";  // string | 
            var apiClientId = "apiClientId_example";  // string | 
            var edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest = new EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest(); // EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest |  (optional) 

            try
            {
                // Updates an Instance Application ApiClient
                EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse result = apiInstance.UpdateInstanceApiClient(tenantId, instanceId, applicationId, apiClientId, edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.UpdateInstanceApiClient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateInstanceApiClientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Instance Application ApiClient
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse> response = apiInstance.UpdateInstanceApiClientWithHttpInfo(tenantId, instanceId, applicationId, apiClientId, edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesInstanceApplicationsAPIClientsApi.UpdateInstanceApiClientWithHttpInfo: " + e.Message);
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
| **edfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest** | [**EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest**](EdfiAdminApiEdfiAdminV1UpdateInstanceApiClientRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse**](EdfiAdminApiEdfiAdminV1InstanceApiClientUpdatedResponse.md)

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

