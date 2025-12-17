# EdGraph.Platform.Client.Api.InstanceOnboardingStepsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateInstanceOnboardingStepAsync**](InstanceOnboardingStepsApi.md#createinstanceonboardingstepasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps | Creates an Onboarding Step. |
| [**UpdateInstanceOnboardingStepAsync**](InstanceOnboardingStepsApi.md#updateinstanceonboardingstepasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step. |

<a id="createinstanceonboardingstepasync"></a>
# **CreateInstanceOnboardingStepAsync**
> EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse CreateInstanceOnboardingStepAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest = null)

Creates an Onboarding Step.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateInstanceOnboardingStepAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstanceOnboardingStepsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest = new EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest(); // EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest |  (optional) 

            try
            {
                // Creates an Onboarding Step.
                EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse result = apiInstance.CreateInstanceOnboardingStepAsync(tenantId, instanceId, edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstanceOnboardingStepsApi.CreateInstanceOnboardingStepAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInstanceOnboardingStepAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Onboarding Step.
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse> response = apiInstance.CreateInstanceOnboardingStepAsyncWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstanceOnboardingStepsApi.CreateInstanceOnboardingStepAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest** | [**EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest**](EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse**](EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)

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

<a id="updateinstanceonboardingstepasync"></a>
# **UpdateInstanceOnboardingStepAsync**
> EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse UpdateInstanceOnboardingStepAsync (string tenantId, string instanceId, int stepNumber, EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest = null)

Updates the status of an Onboarding Step.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateInstanceOnboardingStepAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstanceOnboardingStepsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var stepNumber = 56;  // int | 
            var edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest = new EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest(); // EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest |  (optional) 

            try
            {
                // Updates the status of an Onboarding Step.
                EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse result = apiInstance.UpdateInstanceOnboardingStepAsync(tenantId, instanceId, stepNumber, edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstanceOnboardingStepsApi.UpdateInstanceOnboardingStepAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateInstanceOnboardingStepAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates the status of an Onboarding Step.
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse> response = apiInstance.UpdateInstanceOnboardingStepAsyncWithHttpInfo(tenantId, instanceId, stepNumber, edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstanceOnboardingStepsApi.UpdateInstanceOnboardingStepAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest** | [**EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest**](EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse**](EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)

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

