# EdGraph.Platform.Client.Api.OnboardingStepsConnectionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOnboardingStepConnection**](OnboardingStepsConnectionsApi.md#createonboardingstepconnection) | **POST** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections | Creates an Onboarding Step connection. |
| [**GetOnboardingStepConnectionById**](OnboardingStepsConnectionsApi.md#getonboardingstepconnectionbyid) | **GET** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Get an Onboarding Step connection by Id |
| [**UpdateOnboardingStepConnection**](OnboardingStepsConnectionsApi.md#updateonboardingstepconnection) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Update an Onboarding Step connection by Id |

<a id="createonboardingstepconnection"></a>
# **CreateOnboardingStepConnection**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse CreateOnboardingStepConnection (string tenantId, int stepNumber, Object body = null)

Creates an Onboarding Step connection.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateOnboardingStepConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new OnboardingStepsConnectionsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var stepNumber = 56;  // int | 
            var body = null;  // Object |  (optional) 

            try
            {
                // Creates an Onboarding Step connection.
                EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse result = apiInstance.CreateOnboardingStepConnection(tenantId, stepNumber, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OnboardingStepsConnectionsApi.CreateOnboardingStepConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateOnboardingStepConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Onboarding Step connection.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse> response = apiInstance.CreateOnboardingStepConnectionWithHttpInfo(tenantId, stepNumber, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OnboardingStepsConnectionsApi.CreateOnboardingStepConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse.md)

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

<a id="getonboardingstepconnectionbyid"></a>
# **GetOnboardingStepConnectionById**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse GetOnboardingStepConnectionById (string tenantId, int stepNumber, string connectionId)

Get an Onboarding Step connection by Id

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetOnboardingStepConnectionByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new OnboardingStepsConnectionsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var stepNumber = 56;  // int | 
            var connectionId = "connectionId_example";  // string | 

            try
            {
                // Get an Onboarding Step connection by Id
                EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse result = apiInstance.GetOnboardingStepConnectionById(tenantId, stepNumber, connectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OnboardingStepsConnectionsApi.GetOnboardingStepConnectionById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetOnboardingStepConnectionByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an Onboarding Step connection by Id
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse> response = apiInstance.GetOnboardingStepConnectionByIdWithHttpInfo(tenantId, stepNumber, connectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OnboardingStepsConnectionsApi.GetOnboardingStepConnectionByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse.md)

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

<a id="updateonboardingstepconnection"></a>
# **UpdateOnboardingStepConnection**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse UpdateOnboardingStepConnection (string tenantId, int stepNumber, string connectionId, Object body = null)

Update an Onboarding Step connection by Id

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateOnboardingStepConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new OnboardingStepsConnectionsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var stepNumber = 56;  // int | 
            var connectionId = "connectionId_example";  // string | 
            var body = null;  // Object |  (optional) 

            try
            {
                // Update an Onboarding Step connection by Id
                EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse result = apiInstance.UpdateOnboardingStepConnection(tenantId, stepNumber, connectionId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OnboardingStepsConnectionsApi.UpdateOnboardingStepConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateOnboardingStepConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update an Onboarding Step connection by Id
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse> response = apiInstance.UpdateOnboardingStepConnectionWithHttpInfo(tenantId, stepNumber, connectionId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OnboardingStepsConnectionsApi.UpdateOnboardingStepConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **connectionId** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse.md)

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

