# EdGraph.Platform.Client.Api.ConnectionsByTypeDEPRECATEDApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOrUpdateStateReportingConnectionByTypeV1**](ConnectionsByTypeDEPRECATEDApi.md#createorupdatestatereportingconnectionbytypev1) | **PUT** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Creates or Update a Connection by ConnectionType. |
| [**DeleteStateReportingByTypeConnectionV1**](ConnectionsByTypeDEPRECATEDApi.md#deletestatereportingbytypeconnectionv1) | **DELETE** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Deletes a Connection by Type |
| [**GetStateReportingConnectionByTypeV1**](ConnectionsByTypeDEPRECATEDApi.md#getstatereportingconnectionbytypev1) | **GET** /tenants/{tenantId}/statereporting/connectionsByType/{connectionType} | Retrieves a Connection by Type. |

<a id="createorupdatestatereportingconnectionbytypev1"></a>
# **CreateOrUpdateStateReportingConnectionByTypeV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse CreateOrUpdateStateReportingConnectionByTypeV1 (Guid tenantId, string connectionType, EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = null)

Creates or Update a Connection by ConnectionType.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateOrUpdateStateReportingConnectionByTypeV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsByTypeDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var connectionType = "connectionType_example";  // string | 
            var edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest = new EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest(); // EdGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest |  (optional) 

            try
            {
                // Creates or Update a Connection by ConnectionType.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse result = apiInstance.CreateOrUpdateStateReportingConnectionByTypeV1(tenantId, connectionType, edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsByTypeDEPRECATEDApi.CreateOrUpdateStateReportingConnectionByTypeV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateOrUpdateStateReportingConnectionByTypeV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates or Update a Connection by ConnectionType.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionCreatedResponse> response = apiInstance.CreateOrUpdateStateReportingConnectionByTypeV1WithHttpInfo(tenantId, connectionType, edGraphHttpAggregatorsTenantApiServicesStateReportingV1CreateConnectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsByTypeDEPRECATEDApi.CreateOrUpdateStateReportingConnectionByTypeV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionType** | **string** |  |  |
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

<a id="deletestatereportingbytypeconnectionv1"></a>
# **DeleteStateReportingByTypeConnectionV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse DeleteStateReportingByTypeConnectionV1 (Guid tenantId, string connectionType)

Deletes a Connection by Type

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteStateReportingByTypeConnectionV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsByTypeDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var connectionType = "connectionType_example";  // string | 

            try
            {
                // Deletes a Connection by Type
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse result = apiInstance.DeleteStateReportingByTypeConnectionV1(tenantId, connectionType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsByTypeDEPRECATEDApi.DeleteStateReportingByTypeConnectionV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteStateReportingByTypeConnectionV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Connection by Type
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionDeletedResponse> response = apiInstance.DeleteStateReportingByTypeConnectionV1WithHttpInfo(tenantId, connectionType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsByTypeDEPRECATEDApi.DeleteStateReportingByTypeConnectionV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionType** | **string** |  |  |

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

<a id="getstatereportingconnectionbytypev1"></a>
# **GetStateReportingConnectionByTypeV1**
> EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse GetStateReportingConnectionByTypeV1 (Guid tenantId, string connectionType)

Retrieves a Connection by Type.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStateReportingConnectionByTypeV1Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ConnectionsByTypeDEPRECATEDApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var connectionType = "connectionType_example";  // string | 

            try
            {
                // Retrieves a Connection by Type.
                EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse result = apiInstance.GetStateReportingConnectionByTypeV1(tenantId, connectionType);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ConnectionsByTypeDEPRECATEDApi.GetStateReportingConnectionByTypeV1: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStateReportingConnectionByTypeV1WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Connection by Type.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesStateReportingV1ConnectionProfileResponse> response = apiInstance.GetStateReportingConnectionByTypeV1WithHttpInfo(tenantId, connectionType);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ConnectionsByTypeDEPRECATEDApi.GetStateReportingConnectionByTypeV1WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **connectionType** | **string** |  |  |

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

