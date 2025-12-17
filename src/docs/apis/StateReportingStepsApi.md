# EdGraph.Platform.Client.Api.StateReportingStepsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetSteps**](StateReportingStepsApi.md#getsteps) | **GET** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Get Steps Status for the tenant. |
| [**UpdateStep**](StateReportingStepsApi.md#updatestep) | **POST** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Update Steps Status for the tenant. |

<a id="getsteps"></a>
# **GetSteps**
> ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse GetSteps (Guid tenantId, int schoolYear)

Get Steps Status for the tenant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStepsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StateReportingStepsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var schoolYear = 56;  // int | 

            try
            {
                // Get Steps Status for the tenant.
                ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse result = apiInstance.GetSteps(tenantId, schoolYear);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StateReportingStepsApi.GetSteps: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStepsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Steps Status for the tenant.
    ApiResponse<ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse> response = apiInstance.GetStepsWithHttpInfo(tenantId, schoolYear);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StateReportingStepsApi.GetStepsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **schoolYear** | **int** |  |  |

### Return type

[**ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse**](ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)

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

<a id="updatestep"></a>
# **UpdateStep**
> ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse UpdateStep (Guid tenantId, int schoolYear, ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest validationsApiStateReportingStepsV1UpdateStateReportingStepRequest = null)

Update Steps Status for the tenant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateStepExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new StateReportingStepsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var schoolYear = 56;  // int | 
            var validationsApiStateReportingStepsV1UpdateStateReportingStepRequest = new ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest(); // ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest |  (optional) 

            try
            {
                // Update Steps Status for the tenant.
                ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse result = apiInstance.UpdateStep(tenantId, schoolYear, validationsApiStateReportingStepsV1UpdateStateReportingStepRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling StateReportingStepsApi.UpdateStep: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStepWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Update Steps Status for the tenant.
    ApiResponse<ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse> response = apiInstance.UpdateStepWithHttpInfo(tenantId, schoolYear, validationsApiStateReportingStepsV1UpdateStateReportingStepRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling StateReportingStepsApi.UpdateStepWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **schoolYear** | **int** |  |  |
| **validationsApiStateReportingStepsV1UpdateStateReportingStepRequest** | [**ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest**](ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse**](ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)

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

