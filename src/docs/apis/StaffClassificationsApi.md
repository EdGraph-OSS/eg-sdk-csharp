# EdGraph.Platform.Client.Api.StaffClassificationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateStaffClassification**](StaffClassificationsApi.md#createstaffclassification) | **POST** /tenants/{tenantId}/staffclassifications | Creates a StaffClassification. |
| [**DeleteStaffClassification**](StaffClassificationsApi.md#deletestaffclassification) | **DELETE** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Deletes a StaffClassification. |
| [**GetStaffClassificationById**](StaffClassificationsApi.md#getstaffclassificationbyid) | **GET** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Retrieves a StaffClassification by ID. |
| [**GetStaffClassifications**](StaffClassificationsApi.md#getstaffclassifications) | **GET** /tenants/{tenantId}/staffclassifications | Retrieves a list of StaffClassifications. |
| [**GetStaffClassificationsNamespaces**](StaffClassificationsApi.md#getstaffclassificationsnamespaces) | **GET** /tenants/{tenantId}/staffclassifications/namespaces | Retrieves a list of unique Staff Classification Namespaces. |
| [**UpdateStaffClassification**](StaffClassificationsApi.md#updatestaffclassification) | **PUT** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Updates a StaffClassification. |

<a id="createstaffclassification"></a>
# **CreateStaffClassification**
> IdentityApiStaffClassificationV1StaffClassificationCreatedResponse CreateStaffClassification (Guid tenantId, IdentityApiStaffClassificationV1CreateStaffClassificationRequest identityApiStaffClassificationV1CreateStaffClassificationRequest = null)

Creates a StaffClassification.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateStaffClassificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaffClassificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var identityApiStaffClassificationV1CreateStaffClassificationRequest = new IdentityApiStaffClassificationV1CreateStaffClassificationRequest(); // IdentityApiStaffClassificationV1CreateStaffClassificationRequest |  (optional) 

            try
            {
                // Creates a StaffClassification.
                IdentityApiStaffClassificationV1StaffClassificationCreatedResponse result = apiInstance.CreateStaffClassification(tenantId, identityApiStaffClassificationV1CreateStaffClassificationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaffClassificationsApi.CreateStaffClassification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStaffClassificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a StaffClassification.
    ApiResponse<IdentityApiStaffClassificationV1StaffClassificationCreatedResponse> response = apiInstance.CreateStaffClassificationWithHttpInfo(tenantId, identityApiStaffClassificationV1CreateStaffClassificationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaffClassificationsApi.CreateStaffClassificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **identityApiStaffClassificationV1CreateStaffClassificationRequest** | [**IdentityApiStaffClassificationV1CreateStaffClassificationRequest**](IdentityApiStaffClassificationV1CreateStaffClassificationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationCreatedResponse**](IdentityApiStaffClassificationV1StaffClassificationCreatedResponse.md)

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletestaffclassification"></a>
# **DeleteStaffClassification**
> IdentityApiStaffClassificationV1StaffClassificationDeletedResponse DeleteStaffClassification (Guid tenantId, Guid staffClassificationId)

Deletes a StaffClassification.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteStaffClassificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaffClassificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var staffClassificationId = "staffClassificationId_example";  // Guid | 

            try
            {
                // Deletes a StaffClassification.
                IdentityApiStaffClassificationV1StaffClassificationDeletedResponse result = apiInstance.DeleteStaffClassification(tenantId, staffClassificationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaffClassificationsApi.DeleteStaffClassification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteStaffClassificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a StaffClassification.
    ApiResponse<IdentityApiStaffClassificationV1StaffClassificationDeletedResponse> response = apiInstance.DeleteStaffClassificationWithHttpInfo(tenantId, staffClassificationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaffClassificationsApi.DeleteStaffClassificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **staffClassificationId** | **Guid** |  |  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationDeletedResponse**](IdentityApiStaffClassificationV1StaffClassificationDeletedResponse.md)

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

<a id="getstaffclassificationbyid"></a>
# **GetStaffClassificationById**
> IdentityApiStaffClassificationV1StaffClassificationResponse GetStaffClassificationById (Guid tenantId, Guid staffClassificationId)

Retrieves a StaffClassification by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStaffClassificationByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaffClassificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var staffClassificationId = "staffClassificationId_example";  // Guid | 

            try
            {
                // Retrieves a StaffClassification by ID.
                IdentityApiStaffClassificationV1StaffClassificationResponse result = apiInstance.GetStaffClassificationById(tenantId, staffClassificationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaffClassificationsApi.GetStaffClassificationById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStaffClassificationByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a StaffClassification by ID.
    ApiResponse<IdentityApiStaffClassificationV1StaffClassificationResponse> response = apiInstance.GetStaffClassificationByIdWithHttpInfo(tenantId, staffClassificationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaffClassificationsApi.GetStaffClassificationByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **staffClassificationId** | **Guid** |  |  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationResponse**](IdentityApiStaffClassificationV1StaffClassificationResponse.md)

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

<a id="getstaffclassifications"></a>
# **GetStaffClassifications**
> IdentityApiStaffClassificationV1GetStaffClassificationsResponse GetStaffClassifications (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of StaffClassifications.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStaffClassificationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaffClassificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of StaffClassifications.
                IdentityApiStaffClassificationV1GetStaffClassificationsResponse result = apiInstance.GetStaffClassifications(tenantId, pageIndex, pageSize, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaffClassificationsApi.GetStaffClassifications: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStaffClassificationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of StaffClassifications.
    ApiResponse<IdentityApiStaffClassificationV1GetStaffClassificationsResponse> response = apiInstance.GetStaffClassificationsWithHttpInfo(tenantId, pageIndex, pageSize, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaffClassificationsApi.GetStaffClassificationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiStaffClassificationV1GetStaffClassificationsResponse**](IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)

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

<a id="getstaffclassificationsnamespaces"></a>
# **GetStaffClassificationsNamespaces**
> IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse GetStaffClassificationsNamespaces (Guid tenantId, int pageIndex = null, int pageSize = null, string filter = null)

Retrieves a list of unique Staff Classification Namespaces.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStaffClassificationsNamespacesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaffClassificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of unique Staff Classification Namespaces.
                IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse result = apiInstance.GetStaffClassificationsNamespaces(tenantId, pageIndex, pageSize, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaffClassificationsApi.GetStaffClassificationsNamespaces: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStaffClassificationsNamespacesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of unique Staff Classification Namespaces.
    ApiResponse<IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse> response = apiInstance.GetStaffClassificationsNamespacesWithHttpInfo(tenantId, pageIndex, pageSize, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaffClassificationsApi.GetStaffClassificationsNamespacesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse**](IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse.md)

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

<a id="updatestaffclassification"></a>
# **UpdateStaffClassification**
> IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse UpdateStaffClassification (Guid tenantId, Guid staffClassificationId, IdentityApiStaffClassificationV1UpdateStaffClassificationRequest identityApiStaffClassificationV1UpdateStaffClassificationRequest = null)

Updates a StaffClassification.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateStaffClassificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StaffClassificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var staffClassificationId = "staffClassificationId_example";  // Guid | 
            var identityApiStaffClassificationV1UpdateStaffClassificationRequest = new IdentityApiStaffClassificationV1UpdateStaffClassificationRequest(); // IdentityApiStaffClassificationV1UpdateStaffClassificationRequest |  (optional) 

            try
            {
                // Updates a StaffClassification.
                IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse result = apiInstance.UpdateStaffClassification(tenantId, staffClassificationId, identityApiStaffClassificationV1UpdateStaffClassificationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StaffClassificationsApi.UpdateStaffClassification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStaffClassificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a StaffClassification.
    ApiResponse<IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse> response = apiInstance.UpdateStaffClassificationWithHttpInfo(tenantId, staffClassificationId, identityApiStaffClassificationV1UpdateStaffClassificationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StaffClassificationsApi.UpdateStaffClassificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **staffClassificationId** | **Guid** |  |  |
| **identityApiStaffClassificationV1UpdateStaffClassificationRequest** | [**IdentityApiStaffClassificationV1UpdateStaffClassificationRequest**](IdentityApiStaffClassificationV1UpdateStaffClassificationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse**](IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse.md)

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

