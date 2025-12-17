# EdGraph.Platform.Client.Api.InstancesClientsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateClient**](InstancesClientsApi.md#createclient) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Creates a new client |
| [**DeleteClient**](InstancesClientsApi.md#deleteclient) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Deletes a client by Id |
| [**GetClientById**](InstancesClientsApi.md#getclientbyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Retrieves a client by Id |
| [**GetPagedClients**](InstancesClientsApi.md#getpagedclients) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients | Retrieves a list of clients for a given instance |
| [**UpdateClient**](InstancesClientsApi.md#updateclient) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId} | Updates a client by Id |

<a id="createclient"></a>
# **CreateClient**
> IMSAdminApiV1ClientsClientCreatedResponse CreateClient (string tenantId, string instanceId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto = null)

Creates a new client

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateClientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto |  (optional) 

            try
            {
                // Creates a new client
                IMSAdminApiV1ClientsClientCreatedResponse result = apiInstance.CreateClient(tenantId, instanceId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClientsApi.CreateClient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateClientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new client
    ApiResponse<IMSAdminApiV1ClientsClientCreatedResponse> response = apiInstance.CreateClientWithHttpInfo(tenantId, instanceId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClientsApi.CreateClientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsOneRosterCreateClientRequestDto.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientCreatedResponse**](IMSAdminApiV1ClientsClientCreatedResponse.md)

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

<a id="deleteclient"></a>
# **DeleteClient**
> IMSAdminApiV1ClientsClientDeletedResponse DeleteClient (string tenantId, string instanceId, string clientId)

Deletes a client by Id

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteClientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var clientId = "clientId_example";  // string | 

            try
            {
                // Deletes a client by Id
                IMSAdminApiV1ClientsClientDeletedResponse result = apiInstance.DeleteClient(tenantId, instanceId, clientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClientsApi.DeleteClient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteClientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a client by Id
    ApiResponse<IMSAdminApiV1ClientsClientDeletedResponse> response = apiInstance.DeleteClientWithHttpInfo(tenantId, instanceId, clientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClientsApi.DeleteClientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |

### Return type

[**IMSAdminApiV1ClientsClientDeletedResponse**](IMSAdminApiV1ClientsClientDeletedResponse.md)

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

<a id="getclientbyid"></a>
# **GetClientById**
> IMSAdminApiV1ClientsClientProfileResponse GetClientById (string tenantId, string instanceId, string clientId)

Retrieves a client by Id

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetClientByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var clientId = "clientId_example";  // string | 

            try
            {
                // Retrieves a client by Id
                IMSAdminApiV1ClientsClientProfileResponse result = apiInstance.GetClientById(tenantId, instanceId, clientId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClientsApi.GetClientById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetClientByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a client by Id
    ApiResponse<IMSAdminApiV1ClientsClientProfileResponse> response = apiInstance.GetClientByIdWithHttpInfo(tenantId, instanceId, clientId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClientsApi.GetClientByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |

### Return type

[**IMSAdminApiV1ClientsClientProfileResponse**](IMSAdminApiV1ClientsClientProfileResponse.md)

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

<a id="getpagedclients"></a>
# **GetPagedClients**
> IMSAdminApiV1ClientsPaginatedItemsResponse GetPagedClients (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of clients for a given instance

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPagedClientsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of clients for a given instance
                IMSAdminApiV1ClientsPaginatedItemsResponse result = apiInstance.GetPagedClients(tenantId, instanceId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClientsApi.GetPagedClients: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPagedClientsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of clients for a given instance
    ApiResponse<IMSAdminApiV1ClientsPaginatedItemsResponse> response = apiInstance.GetPagedClientsWithHttpInfo(tenantId, instanceId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClientsApi.GetPagedClientsWithHttpInfo: " + e.Message);
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

[**IMSAdminApiV1ClientsPaginatedItemsResponse**](IMSAdminApiV1ClientsPaginatedItemsResponse.md)

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

<a id="updateclient"></a>
# **UpdateClient**
> IMSAdminApiV1ClientsClientUpdatedResponse UpdateClient (string tenantId, string instanceId, string clientId, IMSAdminApiV1ClientsUpdateClientRequest iMSAdminApiV1ClientsUpdateClientRequest = null)

Updates a client by Id

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateClientExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesClientsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var clientId = "clientId_example";  // string | 
            var iMSAdminApiV1ClientsUpdateClientRequest = new IMSAdminApiV1ClientsUpdateClientRequest(); // IMSAdminApiV1ClientsUpdateClientRequest |  (optional) 

            try
            {
                // Updates a client by Id
                IMSAdminApiV1ClientsClientUpdatedResponse result = apiInstance.UpdateClient(tenantId, instanceId, clientId, iMSAdminApiV1ClientsUpdateClientRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesClientsApi.UpdateClient: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateClientWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a client by Id
    ApiResponse<IMSAdminApiV1ClientsClientUpdatedResponse> response = apiInstance.UpdateClientWithHttpInfo(tenantId, instanceId, clientId, iMSAdminApiV1ClientsUpdateClientRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesClientsApi.UpdateClientWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **iMSAdminApiV1ClientsUpdateClientRequest** | [**IMSAdminApiV1ClientsUpdateClientRequest**](IMSAdminApiV1ClientsUpdateClientRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientUpdatedResponse**](IMSAdminApiV1ClientsClientUpdatedResponse.md)

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

