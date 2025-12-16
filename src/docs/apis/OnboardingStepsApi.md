# EdGraph.Platform.Client.Api.OnboardingStepsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOnboardingStep**](OnboardingStepsApi.md#createonboardingstep) | **POST** /tenants/{tenantId}/onboardingsteps | Creates an Onboarding Step. |
| [**GetOnboardingSteps**](OnboardingStepsApi.md#getonboardingsteps) | **GET** /tenants/{tenantId}/onboardingsteps | Gets a list of Onboarding Steps. |
| [**UpdateOnboardingStep**](OnboardingStepsApi.md#updateonboardingstep) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step. |

<a id="createonboardingstep"></a>
# **CreateOnboardingStep**
> TenantApiTenantV1TenantUpdatedResponse CreateOnboardingStep (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto = null)

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
    public class CreateOnboardingStepExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new OnboardingStepsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto |  (optional) 

            try
            {
                // Creates an Onboarding Step.
                TenantApiTenantV1TenantUpdatedResponse result = apiInstance.CreateOnboardingStep(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OnboardingStepsApi.CreateOnboardingStep: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateOnboardingStepWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates an Onboarding Step.
    ApiResponse<TenantApiTenantV1TenantUpdatedResponse> response = apiInstance.CreateOnboardingStepWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OnboardingStepsApi.CreateOnboardingStepWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1TenantUpdatedResponse**](TenantApiTenantV1TenantUpdatedResponse.md)

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

<a id="getonboardingsteps"></a>
# **GetOnboardingSteps**
> TenantApiTenantV1OnboardingStepsReponse GetOnboardingSteps (string tenantId)

Gets a list of Onboarding Steps.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetOnboardingStepsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new OnboardingStepsApi(config);
            var tenantId = "tenantId_example";  // string | 

            try
            {
                // Gets a list of Onboarding Steps.
                TenantApiTenantV1OnboardingStepsReponse result = apiInstance.GetOnboardingSteps(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OnboardingStepsApi.GetOnboardingSteps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetOnboardingStepsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets a list of Onboarding Steps.
    ApiResponse<TenantApiTenantV1OnboardingStepsReponse> response = apiInstance.GetOnboardingStepsWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OnboardingStepsApi.GetOnboardingStepsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**TenantApiTenantV1OnboardingStepsReponse**](TenantApiTenantV1OnboardingStepsReponse.md)

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

<a id="updateonboardingstep"></a>
# **UpdateOnboardingStep**
> TenantApiTenantV1TenantUpdatedResponse UpdateOnboardingStep (string tenantId, int stepNumber, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto = null)

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
    public class UpdateOnboardingStepExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new OnboardingStepsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var stepNumber = 56;  // int | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto |  (optional) 

            try
            {
                // Updates the status of an Onboarding Step.
                TenantApiTenantV1TenantUpdatedResponse result = apiInstance.UpdateOnboardingStep(tenantId, stepNumber, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling OnboardingStepsApi.UpdateOnboardingStep: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateOnboardingStepWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates the status of an Onboarding Step.
    ApiResponse<TenantApiTenantV1TenantUpdatedResponse> response = apiInstance.UpdateOnboardingStepWithHttpInfo(tenantId, stepNumber, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling OnboardingStepsApi.UpdateOnboardingStepWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1TenantUpdatedResponse**](TenantApiTenantV1TenantUpdatedResponse.md)

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

