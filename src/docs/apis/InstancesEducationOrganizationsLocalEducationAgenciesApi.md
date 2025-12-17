# EdGraph.Platform.Client.Api.InstancesEducationOrganizationsLocalEducationAgenciesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#createlocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Creates a LocalEducationAgency. |
| [**DeleteLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#deletelocaleducationagencyasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Deletes a LocalEducationAgency. |
| [**GetLocalEducationAgencyByIdAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getlocaleducationagencybyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Retrieves a LocalEducationAgency by ID. |
| [**GetlLocalEducationAgenciesAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#getllocaleducationagenciesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies | Retrieves a list of LocalEducationAgencies. |
| [**SyncLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#synclocaleducationagencyasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId}/sync | Copies a LocalEducationAgency from one instance to another/other instance(s). |
| [**UpdateLocalEducationAgencyAsync**](InstancesEducationOrganizationsLocalEducationAgenciesApi.md#updatelocaleducationagencyasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/localeducationagencies/{localEducationAgencyId} | Updates a LocalEducationAgency. |

<a id="createlocaleducationagencyasync"></a>
# **CreateLocalEducationAgencyAsync**
> EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse CreateLocalEducationAgencyAsync (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest = null)

Creates a LocalEducationAgency.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateLocalEducationAgencyAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsLocalEducationAgenciesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest = new EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest(); // EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest |  (optional) 

            try
            {
                // Creates a LocalEducationAgency.
                EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse result = apiInstance.CreateLocalEducationAgencyAsync(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.CreateLocalEducationAgencyAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateLocalEducationAgencyAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a LocalEducationAgency.
    ApiResponse<EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse> response = apiInstance.CreateLocalEducationAgencyAsyncWithHttpInfo(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.CreateLocalEducationAgencyAsyncWithHttpInfo: " + e.Message);
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
| **edfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1CreateLocalEducationAgencyRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse**](EdfiAdminApiEdfiAdminV1LocalEducationAgencyCreatedResponse.md)

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

<a id="deletelocaleducationagencyasync"></a>
# **DeleteLocalEducationAgencyAsync**
> void DeleteLocalEducationAgencyAsync (string tenantId, string instanceId, int year, string localEducationAgencyId)

Deletes a LocalEducationAgency.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteLocalEducationAgencyAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsLocalEducationAgenciesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var localEducationAgencyId = "localEducationAgencyId_example";  // string | 

            try
            {
                // Deletes a LocalEducationAgency.
                apiInstance.DeleteLocalEducationAgencyAsync(tenantId, instanceId, year, localEducationAgencyId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.DeleteLocalEducationAgencyAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteLocalEducationAgencyAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a LocalEducationAgency.
    apiInstance.DeleteLocalEducationAgencyAsyncWithHttpInfo(tenantId, instanceId, year, localEducationAgencyId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.DeleteLocalEducationAgencyAsyncWithHttpInfo: " + e.Message);
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
| **localEducationAgencyId** | **string** |  |  |

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

<a id="getlocaleducationagencybyidasync"></a>
# **GetLocalEducationAgencyByIdAsync**
> EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse GetLocalEducationAgencyByIdAsync (string tenantId, string instanceId, int year, string localEducationAgencyId)

Retrieves a LocalEducationAgency by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetLocalEducationAgencyByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsLocalEducationAgenciesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var localEducationAgencyId = "localEducationAgencyId_example";  // string | 

            try
            {
                // Retrieves a LocalEducationAgency by ID.
                EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse result = apiInstance.GetLocalEducationAgencyByIdAsync(tenantId, instanceId, year, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.GetLocalEducationAgencyByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetLocalEducationAgencyByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a LocalEducationAgency by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse> response = apiInstance.GetLocalEducationAgencyByIdAsyncWithHttpInfo(tenantId, instanceId, year, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.GetLocalEducationAgencyByIdAsyncWithHttpInfo: " + e.Message);
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
| **localEducationAgencyId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse**](EdfiAdminApiEdfiAdminV1GetLocalEducationAgencyProfileResponse.md)

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

<a id="getllocaleducationagenciesasync"></a>
# **GetlLocalEducationAgenciesAsync**
> EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel GetlLocalEducationAgenciesAsync (string tenantId, string instanceId, int year, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of LocalEducationAgencies.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetlLocalEducationAgenciesAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsLocalEducationAgenciesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of LocalEducationAgencies.
                EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel result = apiInstance.GetlLocalEducationAgenciesAsync(tenantId, instanceId, year, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.GetlLocalEducationAgenciesAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetlLocalEducationAgenciesAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of LocalEducationAgencies.
    ApiResponse<EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel> response = apiInstance.GetlLocalEducationAgenciesAsyncWithHttpInfo(tenantId, instanceId, year, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.GetlLocalEducationAgenciesAsyncWithHttpInfo: " + e.Message);
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
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1LocalEducationAgencyTableViewResponsePaginatedItemsViewModel.md)

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

<a id="synclocaleducationagencyasync"></a>
# **SyncLocalEducationAgencyAsync**
> EdfiAdminApiEdfiAdminV1SyncResponse SyncLocalEducationAgencyAsync (string tenantId, string instanceId, int year, int localEducationAgencyId, EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest = null)

Copies a LocalEducationAgency from one instance to another/other instance(s).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SyncLocalEducationAgencyAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsLocalEducationAgenciesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var localEducationAgencyId = 56;  // int | 
            var edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest = new EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest(); // EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest |  (optional) 

            try
            {
                // Copies a LocalEducationAgency from one instance to another/other instance(s).
                EdfiAdminApiEdfiAdminV1SyncResponse result = apiInstance.SyncLocalEducationAgencyAsync(tenantId, instanceId, year, localEducationAgencyId, edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.SyncLocalEducationAgencyAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SyncLocalEducationAgencyAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Copies a LocalEducationAgency from one instance to another/other instance(s).
    ApiResponse<EdfiAdminApiEdfiAdminV1SyncResponse> response = apiInstance.SyncLocalEducationAgencyAsyncWithHttpInfo(tenantId, instanceId, year, localEducationAgencyId, edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.SyncLocalEducationAgencyAsyncWithHttpInfo: " + e.Message);
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
| **localEducationAgencyId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1SyncLocalEducationAgencyRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SyncResponse**](EdfiAdminApiEdfiAdminV1SyncResponse.md)

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

<a id="updatelocaleducationagencyasync"></a>
# **UpdateLocalEducationAgencyAsync**
> void UpdateLocalEducationAgencyAsync (string tenantId, string instanceId, int year, string localEducationAgencyId, EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest = null)

Updates a LocalEducationAgency.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateLocalEducationAgencyAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsLocalEducationAgenciesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var localEducationAgencyId = "localEducationAgencyId_example";  // string | 
            var edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest = new EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest(); // EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest |  (optional) 

            try
            {
                // Updates a LocalEducationAgency.
                apiInstance.UpdateLocalEducationAgencyAsync(tenantId, instanceId, year, localEducationAgencyId, edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.UpdateLocalEducationAgencyAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateLocalEducationAgencyAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a LocalEducationAgency.
    apiInstance.UpdateLocalEducationAgencyAsyncWithHttpInfo(tenantId, instanceId, year, localEducationAgencyId, edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsLocalEducationAgenciesApi.UpdateLocalEducationAgencyAsyncWithHttpInfo: " + e.Message);
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
| **localEducationAgencyId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest** | [**EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest**](EdfiAdminApiEdfiAdminV1UpdateLocalEducationAgencyRequest.md) |  | [optional]  |

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

