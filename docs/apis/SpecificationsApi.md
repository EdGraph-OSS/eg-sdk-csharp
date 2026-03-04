# EdGraph.Platform.Client.Api.SpecificationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSpecification**](SpecificationsApi.md#createspecification) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications | Create a Specification resource |
| [**DeleteSpecification**](SpecificationsApi.md#deletespecification) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{id} | Delete of Specification resource |
| [**ExportSpecifications**](SpecificationsApi.md#exportspecifications) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/export | Export all Specifications resources given a Tenant |
| [**GetSpecification**](SpecificationsApi.md#getspecification) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{id} | Get Specification resource |
| [**PurgeSpecification**](SpecificationsApi.md#purgespecification) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{specificationId}/purge | Purge a deleted Specification resource |
| [**RecoverSpecification**](SpecificationsApi.md#recoverspecification) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{specificationId}/recover | Recover deleted Specification resource |
| [**SearchSpecifications**](SpecificationsApi.md#searchspecifications) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/search | Seaarch specifications |
| [**UpdateSpecification**](SpecificationsApi.md#updatespecification) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/specifications/{id} | Update specification |

<a id="createspecification"></a>
# **CreateSpecification**
> void CreateSpecification (Guid tenantId, Guid instanceId, EdfiAdminApiEdfiAdminV1CreateSpecificationRequest edfiAdminApiEdfiAdminV1CreateSpecificationRequest = null)

Create a Specification resource

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateSpecificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var edfiAdminApiEdfiAdminV1CreateSpecificationRequest = new EdfiAdminApiEdfiAdminV1CreateSpecificationRequest(); // EdfiAdminApiEdfiAdminV1CreateSpecificationRequest |  (optional) 

            try
            {
                // Create a Specification resource
                apiInstance.CreateSpecification(tenantId, instanceId, edfiAdminApiEdfiAdminV1CreateSpecificationRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.CreateSpecification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSpecificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Create a Specification resource
    apiInstance.CreateSpecificationWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1CreateSpecificationRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.CreateSpecificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1CreateSpecificationRequest** | [**EdfiAdminApiEdfiAdminV1CreateSpecificationRequest**](EdfiAdminApiEdfiAdminV1CreateSpecificationRequest.md) |  | [optional]  |

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
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletespecification"></a>
# **DeleteSpecification**
> EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse DeleteSpecification (Guid tenantId, Guid instanceId, Guid id)

Delete of Specification resource

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteSpecificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var id = "id_example";  // Guid | 

            try
            {
                // Delete of Specification resource
                EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse result = apiInstance.DeleteSpecification(tenantId, instanceId, id);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.DeleteSpecification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteSpecificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete of Specification resource
    ApiResponse<EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse> response = apiInstance.DeleteSpecificationWithHttpInfo(tenantId, instanceId, id);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.DeleteSpecificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse**](EdfiAdminApiEdfiAdminV1SpecificationDeletedResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="exportspecifications"></a>
# **ExportSpecifications**
> EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse ExportSpecifications (Guid tenantId, Guid instanceId, EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest edfiAdminApiEdfiAdminV1ExportSpecificationsRequest = null)

Export all Specifications resources given a Tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ExportSpecificationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var edfiAdminApiEdfiAdminV1ExportSpecificationsRequest = new EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest(); // EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest |  (optional) 

            try
            {
                // Export all Specifications resources given a Tenant
                EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse result = apiInstance.ExportSpecifications(tenantId, instanceId, edfiAdminApiEdfiAdminV1ExportSpecificationsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.ExportSpecifications: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportSpecificationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Export all Specifications resources given a Tenant
    ApiResponse<EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse> response = apiInstance.ExportSpecificationsWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1ExportSpecificationsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.ExportSpecificationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1ExportSpecificationsRequest** | [**EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest**](EdfiAdminApiEdfiAdminV1ExportSpecificationsRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse**](EdfiAdminApiEdfiAdminV1SpecificationsExportedResponse.md)

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
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getspecification"></a>
# **GetSpecification**
> EdfiAdminApiEdfiAdminV1SpecificationResponse GetSpecification (Guid id, Guid tenantId, Guid instanceId)

Get Specification resource

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetSpecificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var id = "id_example";  // Guid | 
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 

            try
            {
                // Get Specification resource
                EdfiAdminApiEdfiAdminV1SpecificationResponse result = apiInstance.GetSpecification(id, tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.GetSpecification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSpecificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Specification resource
    ApiResponse<EdfiAdminApiEdfiAdminV1SpecificationResponse> response = apiInstance.GetSpecificationWithHttpInfo(id, tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.GetSpecificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **id** | **Guid** |  |  |
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1SpecificationResponse**](EdfiAdminApiEdfiAdminV1SpecificationResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="purgespecification"></a>
# **PurgeSpecification**
> EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse PurgeSpecification (Guid tenantId, Guid instanceId, Guid specificationId)

Purge a deleted Specification resource

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class PurgeSpecificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var specificationId = "specificationId_example";  // Guid | 

            try
            {
                // Purge a deleted Specification resource
                EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse result = apiInstance.PurgeSpecification(tenantId, instanceId, specificationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.PurgeSpecification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PurgeSpecificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Purge a deleted Specification resource
    ApiResponse<EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse> response = apiInstance.PurgeSpecificationWithHttpInfo(tenantId, instanceId, specificationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.PurgeSpecificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **specificationId** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse**](EdfiAdminApiEdfiAdminV1SpecificationPurgedResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="recoverspecification"></a>
# **RecoverSpecification**
> EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse RecoverSpecification (Guid tenantId, Guid instanceId, Guid specificationId)

Recover deleted Specification resource

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RecoverSpecificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var specificationId = "specificationId_example";  // Guid | 

            try
            {
                // Recover deleted Specification resource
                EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse result = apiInstance.RecoverSpecification(tenantId, instanceId, specificationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.RecoverSpecification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RecoverSpecificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Recover deleted Specification resource
    ApiResponse<EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse> response = apiInstance.RecoverSpecificationWithHttpInfo(tenantId, instanceId, specificationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.RecoverSpecificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **specificationId** | **Guid** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse**](EdfiAdminApiEdfiAdminV1SpecificationRecoveredResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchspecifications"></a>
# **SearchSpecifications**
> EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse SearchSpecifications (Guid tenantId, Guid instanceId, EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest edfiAdminApiEdfiAdminV1SearchSpecificationsRequest = null)

Seaarch specifications

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchSpecificationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var edfiAdminApiEdfiAdminV1SearchSpecificationsRequest = new EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest(); // EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest |  (optional) 

            try
            {
                // Seaarch specifications
                EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse result = apiInstance.SearchSpecifications(tenantId, instanceId, edfiAdminApiEdfiAdminV1SearchSpecificationsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.SearchSpecifications: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchSpecificationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Seaarch specifications
    ApiResponse<EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse> response = apiInstance.SearchSpecificationsWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1SearchSpecificationsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.SearchSpecificationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1SearchSpecificationsRequest** | [**EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest**](EdfiAdminApiEdfiAdminV1SearchSpecificationsRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse**](EdfiAdminApiEdfiAdminV1SpecificationsSearchResponse.md)

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
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatespecification"></a>
# **UpdateSpecification**
> EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse UpdateSpecification (Guid tenantId, Guid instanceId, Guid id, EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest edfiAdminApiEdfiAdminV1UpdateSpecificationRequest = null)

Update specification

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateSpecificationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SpecificationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var id = "id_example";  // Guid | 
            var edfiAdminApiEdfiAdminV1UpdateSpecificationRequest = new EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest(); // EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest |  (optional) 

            try
            {
                // Update specification
                EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse result = apiInstance.UpdateSpecification(tenantId, instanceId, id, edfiAdminApiEdfiAdminV1UpdateSpecificationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SpecificationsApi.UpdateSpecification: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSpecificationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update specification
    ApiResponse<EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse> response = apiInstance.UpdateSpecificationWithHttpInfo(tenantId, instanceId, id, edfiAdminApiEdfiAdminV1UpdateSpecificationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SpecificationsApi.UpdateSpecificationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **id** | **Guid** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateSpecificationRequest** | [**EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest**](EdfiAdminApiEdfiAdminV1UpdateSpecificationRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse**](EdfiAdminApiEdfiAdminV1SpecificationUpdatedResponse.md)

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
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

