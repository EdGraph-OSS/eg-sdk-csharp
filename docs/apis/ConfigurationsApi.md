# EdGraph.Platform.Client.Api.ConfigurationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAnalyticsConfigurationAsync**](ConfigurationsApi.md#createanalyticsconfigurationasync) | **POST** /tenants/{tenantId}/analytics/configurations | Creates a new configuration. |
| [**DeleteAnalyticsConfigurationAsync**](ConfigurationsApi.md#deleteanalyticsconfigurationasync) | **DELETE** /tenants/{tenantId}/analytics/configurations/{configurationId} | Deletes a configuration. |
| [**GetAllAnalyticsConfigurationsAsync**](ConfigurationsApi.md#getallanalyticsconfigurationsasync) | **GET** /tenants/{tenantId}/analytics/configurations | Retrieves all configurations. |
| [**GetAnalyticsConfigurationByIdAsync**](ConfigurationsApi.md#getanalyticsconfigurationbyidasync) | **GET** /tenants/{tenantId}/analytics/configurations/{configurationId} | Retrieves a configuration by ID. |
| [**GetAnalyticsConfigurationByTenantIdAsync**](ConfigurationsApi.md#getanalyticsconfigurationbytenantidasync) | **GET** /tenants/{tenantId}/analytics/configurations/default | Retrieves current default configuration. |
| [**HasValidAnalyticsConfigurationAsync**](ConfigurationsApi.md#hasvalidanalyticsconfigurationasync) | **GET** /tenants/{tenantId}/analytics/configurations/default/valid | Verifies if current default configuration has required values for correct functionality. |
| [**UpdateAnalyticsConfigurationAsync**](ConfigurationsApi.md#updateanalyticsconfigurationasync) | **PUT** /tenants/{tenantId}/analytics/configurations/{configurationId} | Updates a configuration. |
| [**ValidateAADTokenAsync**](ConfigurationsApi.md#validateaadtokenasync) | **POST** /tenants/{tenantId}/analytics/configurations/azure/testconnection | Verifies if AAD token generation is possible with user provided values. |

<a id="createanalyticsconfigurationasync"></a>
# **CreateAnalyticsConfigurationAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfiguration CreateAnalyticsConfigurationAsync (string tenantId, string workspaceName, AnalyticsApiConfigurationsV1CreateConfigurationRequest analyticsApiConfigurationsV1CreateConfigurationRequest = null)

Creates a new configuration.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateAnalyticsConfigurationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var workspaceName = "workspaceName_example";  // string | 
            var analyticsApiConfigurationsV1CreateConfigurationRequest = new AnalyticsApiConfigurationsV1CreateConfigurationRequest(); // AnalyticsApiConfigurationsV1CreateConfigurationRequest |  (optional) 

            try
            {
                // Creates a new configuration.
                AnalyticsApiConfigurationsV1AnalyticsConfiguration result = apiInstance.CreateAnalyticsConfigurationAsync(tenantId, workspaceName, analyticsApiConfigurationsV1CreateConfigurationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.CreateAnalyticsConfigurationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateAnalyticsConfigurationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new configuration.
    ApiResponse<AnalyticsApiConfigurationsV1AnalyticsConfiguration> response = apiInstance.CreateAnalyticsConfigurationAsyncWithHttpInfo(tenantId, workspaceName, analyticsApiConfigurationsV1CreateConfigurationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.CreateAnalyticsConfigurationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **workspaceName** | **string** |  |  |
| **analyticsApiConfigurationsV1CreateConfigurationRequest** | [**AnalyticsApiConfigurationsV1CreateConfigurationRequest**](AnalyticsApiConfigurationsV1CreateConfigurationRequest.md) |  | [optional]  |

### Return type

[**AnalyticsApiConfigurationsV1AnalyticsConfiguration**](AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteanalyticsconfigurationasync"></a>
# **DeleteAnalyticsConfigurationAsync**
> void DeleteAnalyticsConfigurationAsync (string tenantId, string configurationId)

Deletes a configuration.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteAnalyticsConfigurationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var configurationId = "configurationId_example";  // string | 

            try
            {
                // Deletes a configuration.
                apiInstance.DeleteAnalyticsConfigurationAsync(tenantId, configurationId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.DeleteAnalyticsConfigurationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteAnalyticsConfigurationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a configuration.
    apiInstance.DeleteAnalyticsConfigurationAsyncWithHttpInfo(tenantId, configurationId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.DeleteAnalyticsConfigurationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **configurationId** | **string** |  |  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getallanalyticsconfigurationsasync"></a>
# **GetAllAnalyticsConfigurationsAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel GetAllAnalyticsConfigurationsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves all configurations.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllAnalyticsConfigurationsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves all configurations.
                AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel result = apiInstance.GetAllAnalyticsConfigurationsAsync(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.GetAllAnalyticsConfigurationsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllAnalyticsConfigurationsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves all configurations.
    ApiResponse<AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel> response = apiInstance.GetAllAnalyticsConfigurationsAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.GetAllAnalyticsConfigurationsAsyncWithHttpInfo: " + e.Message);
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

[**AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel**](AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getanalyticsconfigurationbyidasync"></a>
# **GetAnalyticsConfigurationByIdAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfiguration GetAnalyticsConfigurationByIdAsync (string tenantId, string configurationId)

Retrieves a configuration by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAnalyticsConfigurationByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var configurationId = "configurationId_example";  // string | 

            try
            {
                // Retrieves a configuration by ID.
                AnalyticsApiConfigurationsV1AnalyticsConfiguration result = apiInstance.GetAnalyticsConfigurationByIdAsync(tenantId, configurationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.GetAnalyticsConfigurationByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAnalyticsConfigurationByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a configuration by ID.
    ApiResponse<AnalyticsApiConfigurationsV1AnalyticsConfiguration> response = apiInstance.GetAnalyticsConfigurationByIdAsyncWithHttpInfo(tenantId, configurationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.GetAnalyticsConfigurationByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **configurationId** | **string** |  |  |

### Return type

[**AnalyticsApiConfigurationsV1AnalyticsConfiguration**](AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getanalyticsconfigurationbytenantidasync"></a>
# **GetAnalyticsConfigurationByTenantIdAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfiguration GetAnalyticsConfigurationByTenantIdAsync (string tenantId)

Retrieves current default configuration.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAnalyticsConfigurationByTenantIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 

            try
            {
                // Retrieves current default configuration.
                AnalyticsApiConfigurationsV1AnalyticsConfiguration result = apiInstance.GetAnalyticsConfigurationByTenantIdAsync(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.GetAnalyticsConfigurationByTenantIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAnalyticsConfigurationByTenantIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves current default configuration.
    ApiResponse<AnalyticsApiConfigurationsV1AnalyticsConfiguration> response = apiInstance.GetAnalyticsConfigurationByTenantIdAsyncWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.GetAnalyticsConfigurationByTenantIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**AnalyticsApiConfigurationsV1AnalyticsConfiguration**](AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="hasvalidanalyticsconfigurationasync"></a>
# **HasValidAnalyticsConfigurationAsync**
> AnalyticsApiConfigurationsV1HasValidConfigurationResponse HasValidAnalyticsConfigurationAsync (string tenantId)

Verifies if current default configuration has required values for correct functionality.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class HasValidAnalyticsConfigurationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 

            try
            {
                // Verifies if current default configuration has required values for correct functionality.
                AnalyticsApiConfigurationsV1HasValidConfigurationResponse result = apiInstance.HasValidAnalyticsConfigurationAsync(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.HasValidAnalyticsConfigurationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the HasValidAnalyticsConfigurationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Verifies if current default configuration has required values for correct functionality.
    ApiResponse<AnalyticsApiConfigurationsV1HasValidConfigurationResponse> response = apiInstance.HasValidAnalyticsConfigurationAsyncWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.HasValidAnalyticsConfigurationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**AnalyticsApiConfigurationsV1HasValidConfigurationResponse**](AnalyticsApiConfigurationsV1HasValidConfigurationResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateanalyticsconfigurationasync"></a>
# **UpdateAnalyticsConfigurationAsync**
> AnalyticsApiConfigurationsV1ConfigurationResponse UpdateAnalyticsConfigurationAsync (string tenantId, string configurationId, AnalyticsApiConfigurationsV1UpdateConfigurationRequest analyticsApiConfigurationsV1UpdateConfigurationRequest = null)

Updates a configuration.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateAnalyticsConfigurationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var configurationId = "configurationId_example";  // string | 
            var analyticsApiConfigurationsV1UpdateConfigurationRequest = new AnalyticsApiConfigurationsV1UpdateConfigurationRequest(); // AnalyticsApiConfigurationsV1UpdateConfigurationRequest |  (optional) 

            try
            {
                // Updates a configuration.
                AnalyticsApiConfigurationsV1ConfigurationResponse result = apiInstance.UpdateAnalyticsConfigurationAsync(tenantId, configurationId, analyticsApiConfigurationsV1UpdateConfigurationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.UpdateAnalyticsConfigurationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateAnalyticsConfigurationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a configuration.
    ApiResponse<AnalyticsApiConfigurationsV1ConfigurationResponse> response = apiInstance.UpdateAnalyticsConfigurationAsyncWithHttpInfo(tenantId, configurationId, analyticsApiConfigurationsV1UpdateConfigurationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.UpdateAnalyticsConfigurationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **configurationId** | **string** |  |  |
| **analyticsApiConfigurationsV1UpdateConfigurationRequest** | [**AnalyticsApiConfigurationsV1UpdateConfigurationRequest**](AnalyticsApiConfigurationsV1UpdateConfigurationRequest.md) |  | [optional]  |

### Return type

[**AnalyticsApiConfigurationsV1ConfigurationResponse**](AnalyticsApiConfigurationsV1ConfigurationResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="validateaadtokenasync"></a>
# **ValidateAADTokenAsync**
> AnalyticsApiConfigurationsV1TestConnectionResponse ValidateAADTokenAsync (string tenantId, AnalyticsApiConfigurationsV1AnalyticsAzureAd analyticsApiConfigurationsV1AnalyticsAzureAd = null)

Verifies if AAD token generation is possible with user provided values.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ValidateAADTokenAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConfigurationsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var analyticsApiConfigurationsV1AnalyticsAzureAd = new AnalyticsApiConfigurationsV1AnalyticsAzureAd(); // AnalyticsApiConfigurationsV1AnalyticsAzureAd |  (optional) 

            try
            {
                // Verifies if AAD token generation is possible with user provided values.
                AnalyticsApiConfigurationsV1TestConnectionResponse result = apiInstance.ValidateAADTokenAsync(tenantId, analyticsApiConfigurationsV1AnalyticsAzureAd);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConfigurationsApi.ValidateAADTokenAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ValidateAADTokenAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Verifies if AAD token generation is possible with user provided values.
    ApiResponse<AnalyticsApiConfigurationsV1TestConnectionResponse> response = apiInstance.ValidateAADTokenAsyncWithHttpInfo(tenantId, analyticsApiConfigurationsV1AnalyticsAzureAd);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConfigurationsApi.ValidateAADTokenAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiConfigurationsV1AnalyticsAzureAd** | [**AnalyticsApiConfigurationsV1AnalyticsAzureAd**](AnalyticsApiConfigurationsV1AnalyticsAzureAd.md) |  | [optional]  |

### Return type

[**AnalyticsApiConfigurationsV1TestConnectionResponse**](AnalyticsApiConfigurationsV1TestConnectionResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

