# EdGraph.Platform.Client.Api.DomainsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTenantDomainAsync**](DomainsApi.md#createtenantdomainasync) | **POST** /tenants/{tenantId}/domains | Creates a new domain |
| [**DeleteTenantDomainAsync**](DomainsApi.md#deletetenantdomainasync) | **DELETE** /tenants/{tenantId}/domains/{domainName} | Deletes a user |
| [**GetAllTenantDomainsAsync**](DomainsApi.md#getalltenantdomainsasync) | **GET** /tenants/{tenantId}/domains | Retrieves a list of domains associated to this tenant |
| [**GetTenantDomainProfileByNameAsync**](DomainsApi.md#gettenantdomainprofilebynameasync) | **GET** /tenants/{tenantId}/domains/{domainName} | Retrieves a domain |
| [**UpdateTenantDomainAsync**](DomainsApi.md#updatetenantdomainasync) | **PUT** /tenants/{tenantId}/domains/{domainName} | Updates a domain |
| [**VerifyTenantDomainAsync**](DomainsApi.md#verifytenantdomainasync) | **PUT** /tenants/{tenantId}/domains/{domainName}/verify | Verify a  tenant&#39;s domain |

<a id="createtenantdomainasync"></a>
# **CreateTenantDomainAsync**
> TenantApiTenantV1DomainCreatedResponse CreateTenantDomainAsync (string tenantId, TenantApiTenantV1CreateDomainRequest tenantApiTenantV1CreateDomainRequest = null)

Creates a new domain

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateTenantDomainAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new DomainsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var tenantApiTenantV1CreateDomainRequest = new TenantApiTenantV1CreateDomainRequest(); // TenantApiTenantV1CreateDomainRequest |  (optional) 

            try
            {
                // Creates a new domain
                TenantApiTenantV1DomainCreatedResponse result = apiInstance.CreateTenantDomainAsync(tenantId, tenantApiTenantV1CreateDomainRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DomainsApi.CreateTenantDomainAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateTenantDomainAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new domain
    ApiResponse<TenantApiTenantV1DomainCreatedResponse> response = apiInstance.CreateTenantDomainAsyncWithHttpInfo(tenantId, tenantApiTenantV1CreateDomainRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DomainsApi.CreateTenantDomainAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **tenantApiTenantV1CreateDomainRequest** | [**TenantApiTenantV1CreateDomainRequest**](TenantApiTenantV1CreateDomainRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1DomainCreatedResponse**](TenantApiTenantV1DomainCreatedResponse.md)

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

<a id="deletetenantdomainasync"></a>
# **DeleteTenantDomainAsync**
> void DeleteTenantDomainAsync (string tenantId, string domainName)

Deletes a user

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteTenantDomainAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new DomainsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var domainName = "domainName_example";  // string | 

            try
            {
                // Deletes a user
                apiInstance.DeleteTenantDomainAsync(tenantId, domainName);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DomainsApi.DeleteTenantDomainAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteTenantDomainAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a user
    apiInstance.DeleteTenantDomainAsyncWithHttpInfo(tenantId, domainName);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DomainsApi.DeleteTenantDomainAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **domainName** | **string** |  |  |

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

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getalltenantdomainsasync"></a>
# **GetAllTenantDomainsAsync**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel GetAllTenantDomainsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of domains associated to this tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllTenantDomainsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new DomainsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of domains associated to this tenant
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel result = apiInstance.GetAllTenantDomainsAsync(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DomainsApi.GetAllTenantDomainsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantDomainsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of domains associated to this tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel> response = apiInstance.GetAllTenantDomainsAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DomainsApi.GetAllTenantDomainsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesDomainListResponseDtoPaginatedItemsViewModel.md)

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

<a id="gettenantdomainprofilebynameasync"></a>
# **GetTenantDomainProfileByNameAsync**
> TenantApiTenantV1DomainProfileResponse GetTenantDomainProfileByNameAsync (string tenantId, string domainName)

Retrieves a domain

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantDomainProfileByNameAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new DomainsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var domainName = "domainName_example";  // string | 

            try
            {
                // Retrieves a domain
                TenantApiTenantV1DomainProfileResponse result = apiInstance.GetTenantDomainProfileByNameAsync(tenantId, domainName);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DomainsApi.GetTenantDomainProfileByNameAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantDomainProfileByNameAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a domain
    ApiResponse<TenantApiTenantV1DomainProfileResponse> response = apiInstance.GetTenantDomainProfileByNameAsyncWithHttpInfo(tenantId, domainName);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DomainsApi.GetTenantDomainProfileByNameAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **domainName** | **string** |  |  |

### Return type

[**TenantApiTenantV1DomainProfileResponse**](TenantApiTenantV1DomainProfileResponse.md)

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

<a id="updatetenantdomainasync"></a>
# **UpdateTenantDomainAsync**
> TenantApiTenantV1DomainUpdatedResponse UpdateTenantDomainAsync (string tenantId, string domainName, TenantApiTenantV1UpdateDomainRequest tenantApiTenantV1UpdateDomainRequest = null)

Updates a domain

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateTenantDomainAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new DomainsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var domainName = "domainName_example";  // string | 
            var tenantApiTenantV1UpdateDomainRequest = new TenantApiTenantV1UpdateDomainRequest(); // TenantApiTenantV1UpdateDomainRequest |  (optional) 

            try
            {
                // Updates a domain
                TenantApiTenantV1DomainUpdatedResponse result = apiInstance.UpdateTenantDomainAsync(tenantId, domainName, tenantApiTenantV1UpdateDomainRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DomainsApi.UpdateTenantDomainAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTenantDomainAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a domain
    ApiResponse<TenantApiTenantV1DomainUpdatedResponse> response = apiInstance.UpdateTenantDomainAsyncWithHttpInfo(tenantId, domainName, tenantApiTenantV1UpdateDomainRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DomainsApi.UpdateTenantDomainAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **domainName** | **string** |  |  |
| **tenantApiTenantV1UpdateDomainRequest** | [**TenantApiTenantV1UpdateDomainRequest**](TenantApiTenantV1UpdateDomainRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1DomainUpdatedResponse**](TenantApiTenantV1DomainUpdatedResponse.md)

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

<a id="verifytenantdomainasync"></a>
# **VerifyTenantDomainAsync**
> TenantApiTenantV1DomainVerifiedResponse VerifyTenantDomainAsync (string tenantId, string domainName, TenantApiTenantV1VerifyDomainRequest tenantApiTenantV1VerifyDomainRequest = null)

Verify a  tenant's domain

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class VerifyTenantDomainAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new DomainsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var domainName = "domainName_example";  // string | 
            var tenantApiTenantV1VerifyDomainRequest = new TenantApiTenantV1VerifyDomainRequest(); // TenantApiTenantV1VerifyDomainRequest |  (optional) 

            try
            {
                // Verify a  tenant's domain
                TenantApiTenantV1DomainVerifiedResponse result = apiInstance.VerifyTenantDomainAsync(tenantId, domainName, tenantApiTenantV1VerifyDomainRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling DomainsApi.VerifyTenantDomainAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VerifyTenantDomainAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Verify a  tenant's domain
    ApiResponse<TenantApiTenantV1DomainVerifiedResponse> response = apiInstance.VerifyTenantDomainAsyncWithHttpInfo(tenantId, domainName, tenantApiTenantV1VerifyDomainRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling DomainsApi.VerifyTenantDomainAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **domainName** | **string** |  |  |
| **tenantApiTenantV1VerifyDomainRequest** | [**TenantApiTenantV1VerifyDomainRequest**](TenantApiTenantV1VerifyDomainRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1DomainVerifiedResponse**](TenantApiTenantV1DomainVerifiedResponse.md)

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

