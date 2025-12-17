# EdGraph.Platform.Client.Api.CapacitiesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AssignMyGroupToCapacity**](CapacitiesApi.md#assignmygrouptocapacity) | **POST** /tenants/{tenantId}/analytics/capacities | Assigns the specified group to the specified capacity. |
| [**GetAllAnalyticsPowerBiCapacities**](CapacitiesApi.md#getallanalyticspowerbicapacities) | **GET** /tenants/{tenantId}/analytics/capacities | Retrieves a list of capacities in Power Bi that the user has access to. |
| [**ResumeCapacityAsync**](CapacitiesApi.md#resumecapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/resume | Resumes currently suspended capacity |
| [**SuspendCapacityAsync**](CapacitiesApi.md#suspendcapacityasync) | **POST** /tenants/{tenantId}/analytics/capacities/suspend | Suspends currently active capacity |

<a id="assignmygrouptocapacity"></a>
# **AssignMyGroupToCapacity**
> void AssignMyGroupToCapacity (string tenantId, AnalyticsApiCapacitiesV1AssignCapacityRequest analyticsApiCapacitiesV1AssignCapacityRequest = null)

Assigns the specified group to the specified capacity.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AssignMyGroupToCapacityExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CapacitiesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var analyticsApiCapacitiesV1AssignCapacityRequest = new AnalyticsApiCapacitiesV1AssignCapacityRequest(); // AnalyticsApiCapacitiesV1AssignCapacityRequest |  (optional) 

            try
            {
                // Assigns the specified group to the specified capacity.
                apiInstance.AssignMyGroupToCapacity(tenantId, analyticsApiCapacitiesV1AssignCapacityRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CapacitiesApi.AssignMyGroupToCapacity: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AssignMyGroupToCapacityWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Assigns the specified group to the specified capacity.
    apiInstance.AssignMyGroupToCapacityWithHttpInfo(tenantId, analyticsApiCapacitiesV1AssignCapacityRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CapacitiesApi.AssignMyGroupToCapacityWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiCapacitiesV1AssignCapacityRequest** | [**AnalyticsApiCapacitiesV1AssignCapacityRequest**](AnalyticsApiCapacitiesV1AssignCapacityRequest.md) |  | [optional]  |

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getallanalyticspowerbicapacities"></a>
# **GetAllAnalyticsPowerBiCapacities**
> AnalyticsApiCapacitiesV1CapacityResponse GetAllAnalyticsPowerBiCapacities (string tenantId)

Retrieves a list of capacities in Power Bi that the user has access to.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllAnalyticsPowerBiCapacitiesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CapacitiesApi(config);
            var tenantId = "tenantId_example";  // string | 

            try
            {
                // Retrieves a list of capacities in Power Bi that the user has access to.
                AnalyticsApiCapacitiesV1CapacityResponse result = apiInstance.GetAllAnalyticsPowerBiCapacities(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CapacitiesApi.GetAllAnalyticsPowerBiCapacities: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllAnalyticsPowerBiCapacitiesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of capacities in Power Bi that the user has access to.
    ApiResponse<AnalyticsApiCapacitiesV1CapacityResponse> response = apiInstance.GetAllAnalyticsPowerBiCapacitiesWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CapacitiesApi.GetAllAnalyticsPowerBiCapacitiesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**AnalyticsApiCapacitiesV1CapacityResponse**](AnalyticsApiCapacitiesV1CapacityResponse.md)

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

<a id="resumecapacityasync"></a>
# **ResumeCapacityAsync**
> void ResumeCapacityAsync (string tenantId, AnalyticsApiCapacitiesV1ResumeCapacityRequest analyticsApiCapacitiesV1ResumeCapacityRequest = null)

Resumes currently suspended capacity

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ResumeCapacityAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CapacitiesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var analyticsApiCapacitiesV1ResumeCapacityRequest = new AnalyticsApiCapacitiesV1ResumeCapacityRequest(); // AnalyticsApiCapacitiesV1ResumeCapacityRequest |  (optional) 

            try
            {
                // Resumes currently suspended capacity
                apiInstance.ResumeCapacityAsync(tenantId, analyticsApiCapacitiesV1ResumeCapacityRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CapacitiesApi.ResumeCapacityAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResumeCapacityAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resumes currently suspended capacity
    apiInstance.ResumeCapacityAsyncWithHttpInfo(tenantId, analyticsApiCapacitiesV1ResumeCapacityRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CapacitiesApi.ResumeCapacityAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiCapacitiesV1ResumeCapacityRequest** | [**AnalyticsApiCapacitiesV1ResumeCapacityRequest**](AnalyticsApiCapacitiesV1ResumeCapacityRequest.md) |  | [optional]  |

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="suspendcapacityasync"></a>
# **SuspendCapacityAsync**
> void SuspendCapacityAsync (string tenantId, AnalyticsApiCapacitiesV1SuspendCapacityRequest analyticsApiCapacitiesV1SuspendCapacityRequest = null)

Suspends currently active capacity

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SuspendCapacityAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CapacitiesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var analyticsApiCapacitiesV1SuspendCapacityRequest = new AnalyticsApiCapacitiesV1SuspendCapacityRequest(); // AnalyticsApiCapacitiesV1SuspendCapacityRequest |  (optional) 

            try
            {
                // Suspends currently active capacity
                apiInstance.SuspendCapacityAsync(tenantId, analyticsApiCapacitiesV1SuspendCapacityRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CapacitiesApi.SuspendCapacityAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SuspendCapacityAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Suspends currently active capacity
    apiInstance.SuspendCapacityAsyncWithHttpInfo(tenantId, analyticsApiCapacitiesV1SuspendCapacityRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CapacitiesApi.SuspendCapacityAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiCapacitiesV1SuspendCapacityRequest** | [**AnalyticsApiCapacitiesV1SuspendCapacityRequest**](AnalyticsApiCapacitiesV1SuspendCapacityRequest.md) |  | [optional]  |

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

