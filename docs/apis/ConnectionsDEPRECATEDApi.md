# EdGraph.Platform.Client.Api.ConnectionsDEPRECATEDApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#createstatereportingconnectionv1) | **POST** /tenants/{tenantId}/statereporting/connections | Creates a new Connection. |
| [**DeleteStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#deletestatereportingconnectionv1) | **DELETE** /tenants/{tenantId}/statereporting/connections/{connectionId} | Deletes a Connection. |
| [**FindStateReportingConnectionsV1**](ConnectionsDEPRECATEDApi.md#findstatereportingconnectionsv1) | **GET** /tenants/{tenantId}/statereporting/connections | Retrieves a list of Connections. |
| [**GetStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#getstatereportingconnectionv1) | **GET** /tenants/{tenantId}/statereporting/connections/{connectionId} | Retrieves a Connection by ID. |
| [**TestStateReportingConnectionByIdV1**](ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbyidv1) | **POST** /tenants/{tenantId}/statereporting/connections/{connectionId}/testconnection | Tests a Connection by ID. |
| [**TestStateReportingConnectionByTypeV1**](ConnectionsDEPRECATEDApi.md#teststatereportingconnectionbytypev1) | **POST** /tenants/{tenantId}/statereporting/connections/testconnection | Tests a Connection by Type. |
| [**UpdateStateReportingConnectionV1**](ConnectionsDEPRECATEDApi.md#updatestatereportingconnectionv1) | **PUT** /tenants/{tenantId}/statereporting/connections/{connectionId} | Updates a Connection. |

<a id="createstatereportingconnectionv1"></a>
# **CreateStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse CreateStateReportingConnectionV1 (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = null)

Creates a new Connection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateStateReportingConnectionV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = new EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest(); // EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest |  (optional) 

            try
            {
                // Creates a new Connection.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse result = apiInstance.CreateStateReportingConnectionV1(tenantId, edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.CreateStateReportingConnectionV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStateReportingConnectionV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Connection.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse> response = apiInstance.CreateStateReportingConnectionV1WithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.CreateStateReportingConnectionV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest** | [**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse.md)

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

<a id="deletestatereportingconnectionv1"></a>
# **DeleteStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse DeleteStateReportingConnectionV1 (Guid tenantId, Guid connectionId)

Deletes a Connection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteStateReportingConnectionV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var connectionId = "connectionId_example";  // Guid | 

            try
            {
                // Deletes a Connection.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse result = apiInstance.DeleteStateReportingConnectionV1(tenantId, connectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.DeleteStateReportingConnectionV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteStateReportingConnectionV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Connection.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse> response = apiInstance.DeleteStateReportingConnectionV1WithHttpInfo(tenantId, connectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.DeleteStateReportingConnectionV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="findstatereportingconnectionsv1"></a>
# **FindStateReportingConnectionsV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse FindStateReportingConnectionsV1 (string tenantId, string instanceType = null, string connectionType = null)

Retrieves a list of Connections.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class FindStateReportingConnectionsV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceType = "instanceType_example";  // string |  (optional) 
            var connectionType = "connectionType_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Connections.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse result = apiInstance.FindStateReportingConnectionsV1(tenantId, instanceType, connectionType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.FindStateReportingConnectionsV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the FindStateReportingConnectionsV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Connections.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse> response = apiInstance.FindStateReportingConnectionsV1WithHttpInfo(tenantId, instanceType, connectionType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.FindStateReportingConnectionsV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceType** | **string** |  | [optional]  |
| **connectionType** | **string** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1PagedConnectionsResponse.md)

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

<a id="getstatereportingconnectionv1"></a>
# **GetStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse GetStateReportingConnectionV1 (Guid tenantId, Guid connectionId)

Retrieves a Connection by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStateReportingConnectionV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var connectionId = "connectionId_example";  // Guid | 

            try
            {
                // Retrieves a Connection by ID.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse result = apiInstance.GetStateReportingConnectionV1(tenantId, connectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.GetStateReportingConnectionV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStateReportingConnectionV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Connection by ID.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse> response = apiInstance.GetStateReportingConnectionV1WithHttpInfo(tenantId, connectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.GetStateReportingConnectionV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse.md)

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

<a id="teststatereportingconnectionbyidv1"></a>
# **TestStateReportingConnectionByIdV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse TestStateReportingConnectionByIdV1 (Guid tenantId, Guid connectionId)

Tests a Connection by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestStateReportingConnectionByIdV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var connectionId = "connectionId_example";  // Guid | 

            try
            {
                // Tests a Connection by ID.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse result = apiInstance.TestStateReportingConnectionByIdV1(tenantId, connectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.TestStateReportingConnectionByIdV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestStateReportingConnectionByIdV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests a Connection by ID.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse> response = apiInstance.TestStateReportingConnectionByIdV1WithHttpInfo(tenantId, connectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.TestStateReportingConnectionByIdV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="teststatereportingconnectionbytypev1"></a>
# **TestStateReportingConnectionByTypeV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse TestStateReportingConnectionByTypeV1 (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest = null)

Tests a Connection by Type.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestStateReportingConnectionByTypeV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest = new EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest(); // EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest |  (optional) 

            try
            {
                // Tests a Connection by Type.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse result = apiInstance.TestStateReportingConnectionByTypeV1(tenantId, edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.TestStateReportingConnectionByTypeV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestStateReportingConnectionByTypeV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests a Connection by Type.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse> response = apiInstance.TestStateReportingConnectionByTypeV1WithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.TestStateReportingConnectionByTypeV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest** | [**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionByTypeRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1TestConnectionResponse.md)

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

<a id="updatestatereportingconnectionv1"></a>
# **UpdateStateReportingConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse UpdateStateReportingConnectionV1 (Guid tenantId, Guid connectionId, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest = null)

Updates a Connection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateStateReportingConnectionV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var connectionId = "connectionId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest = new EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest(); // EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest |  (optional) 

            try
            {
                // Updates a Connection.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse result = apiInstance.UpdateStateReportingConnectionV1(tenantId, connectionId, edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.UpdateStateReportingConnectionV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStateReportingConnectionV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Connection.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse> response = apiInstance.UpdateStateReportingConnectionV1WithHttpInfo(tenantId, connectionId, edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsDEPRECATEDApi.UpdateStateReportingConnectionV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest** | [**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1UpdateConnectionRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse**](EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionUpdatedResponse.md)

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

