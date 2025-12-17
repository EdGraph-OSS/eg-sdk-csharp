# EdGraph.Platform.Client.Api.InstancesEducationOrganizationsEducationServiceCentersApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEducationServiceCenterAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#createeducationservicecenterasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters | Creates an EducationServiceCenter. |
| [**DeleteEducationServiceCenterAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#deleteeducationservicecenterasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Deletes an EducationServiceCenter. |
| [**GetEducationServiceCenterByIdAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#geteducationservicecenterbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Retrieves an EducationServiceCenter by ID. |
| [**UpdateEducationServiceCenterAsync**](InstancesEducationOrganizationsEducationServiceCentersApi.md#updateeducationservicecenterasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/educationservicecenters/{educationServiceCenterId} | Updates an EducationServiceCenter. |

<a id="createeducationservicecenterasync"></a>
# **CreateEducationServiceCenterAsync**
> EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse CreateEducationServiceCenterAsync (Guid tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest = null)

Creates an EducationServiceCenter.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateEducationServiceCenterAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsEducationServiceCentersApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest = new EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest(); // EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest |  (optional) 

            try
            {
                // Creates an EducationServiceCenter.
                EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse result = apiInstance.CreateEducationServiceCenterAsync(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.CreateEducationServiceCenterAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEducationServiceCenterAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an EducationServiceCenter.
    ApiResponse<EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse> response = apiInstance.CreateEducationServiceCenterAsyncWithHttpInfo(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.CreateEducationServiceCenterAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest** | [**EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest**](EdfiAdminApiEdfiAdminV1CreateEducationServiceCenterRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse**](EdfiAdminApiEdfiAdminV1EducationServiceCenterCreatedResponse.md)

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

<a id="deleteeducationservicecenterasync"></a>
# **DeleteEducationServiceCenterAsync**
> void DeleteEducationServiceCenterAsync (Guid tenantId, string instanceId, int year, Guid educationServiceCenterId)

Deletes an EducationServiceCenter.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteEducationServiceCenterAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsEducationServiceCentersApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var educationServiceCenterId = "educationServiceCenterId_example";  // Guid | 

            try
            {
                // Deletes an EducationServiceCenter.
                apiInstance.DeleteEducationServiceCenterAsync(tenantId, instanceId, year, educationServiceCenterId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.DeleteEducationServiceCenterAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteEducationServiceCenterAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an EducationServiceCenter.
    apiInstance.DeleteEducationServiceCenterAsyncWithHttpInfo(tenantId, instanceId, year, educationServiceCenterId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.DeleteEducationServiceCenterAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **educationServiceCenterId** | **Guid** |  |  |

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

<a id="geteducationservicecenterbyidasync"></a>
# **GetEducationServiceCenterByIdAsync**
> EdfiAdminApiEdfiAdminV1EducationServiceCenter GetEducationServiceCenterByIdAsync (Guid tenantId, string instanceId, int year, Guid educationServiceCenterId)

Retrieves an EducationServiceCenter by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEducationServiceCenterByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsEducationServiceCentersApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var educationServiceCenterId = "educationServiceCenterId_example";  // Guid | 

            try
            {
                // Retrieves an EducationServiceCenter by ID.
                EdfiAdminApiEdfiAdminV1EducationServiceCenter result = apiInstance.GetEducationServiceCenterByIdAsync(tenantId, instanceId, year, educationServiceCenterId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.GetEducationServiceCenterByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEducationServiceCenterByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an EducationServiceCenter by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1EducationServiceCenter> response = apiInstance.GetEducationServiceCenterByIdAsyncWithHttpInfo(tenantId, instanceId, year, educationServiceCenterId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.GetEducationServiceCenterByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **educationServiceCenterId** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1EducationServiceCenter**](EdfiAdminApiEdfiAdminV1EducationServiceCenter.md)

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

<a id="updateeducationservicecenterasync"></a>
# **UpdateEducationServiceCenterAsync**
> void UpdateEducationServiceCenterAsync (Guid tenantId, string instanceId, int year, Guid educationServiceCenterId, EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest = null)

Updates an EducationServiceCenter.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateEducationServiceCenterAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesEducationOrganizationsEducationServiceCentersApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var educationServiceCenterId = "educationServiceCenterId_example";  // Guid | 
            var edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest = new EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest(); // EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest |  (optional) 

            try
            {
                // Updates an EducationServiceCenter.
                apiInstance.UpdateEducationServiceCenterAsync(tenantId, instanceId, year, educationServiceCenterId, edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.UpdateEducationServiceCenterAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEducationServiceCenterAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an EducationServiceCenter.
    apiInstance.UpdateEducationServiceCenterAsyncWithHttpInfo(tenantId, instanceId, year, educationServiceCenterId, edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesEducationOrganizationsEducationServiceCentersApi.UpdateEducationServiceCenterAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **educationServiceCenterId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest** | [**EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest**](EdfiAdminApiEdfiAdminV1UpdateEducationServiceCenterRequest.md) |  | [optional]  |

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

