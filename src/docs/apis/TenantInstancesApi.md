# EdGraph.Platform.Client.Api.TenantInstancesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**LoadOnboardingStepEdFiApiMetadata**](TenantInstancesApi.md#loadonboardingstepedfiapimetadata) | **POST** /tenants/{tenantId}/onboardingsteps/edfi-api-metadata | Loads connection metadata. |
| [**TestOnboardingStepConnection**](TenantInstancesApi.md#testonboardingstepconnection) | **POST** /tenants/{tenantId}/onboardingsteps/testconnection | Tests availability of provided connection metadata. |

<a id="loadonboardingstepedfiapimetadata"></a>
# **LoadOnboardingStepEdFiApiMetadata**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult LoadOnboardingStepEdFiApiMetadata (string tenantId, EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest = null)

Loads connection metadata.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class LoadOnboardingStepEdFiApiMetadataExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantInstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest = new EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest(); // EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest |  (optional) 

            try
            {
                // Loads connection metadata.
                EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult result = apiInstance.LoadOnboardingStepEdFiApiMetadata(tenantId, edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantInstancesApi.LoadOnboardingStepEdFiApiMetadata: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoadOnboardingStepEdFiApiMetadataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Loads connection metadata.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult> response = apiInstance.LoadOnboardingStepEdFiApiMetadataWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantInstancesApi.LoadOnboardingStepEdFiApiMetadataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest** | [**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult.md)

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

<a id="testonboardingstepconnection"></a>
# **TestOnboardingStepConnection**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse TestOnboardingStepConnection (string tenantId, Object body = null)

Tests availability of provided connection metadata.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestOnboardingStepConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantInstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var body = null;  // Object |  (optional) 

            try
            {
                // Tests availability of provided connection metadata.
                EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse result = apiInstance.TestOnboardingStepConnection(tenantId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantInstancesApi.TestOnboardingStepConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestOnboardingStepConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests availability of provided connection metadata.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse> response = apiInstance.TestOnboardingStepConnectionWithHttpInfo(tenantId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantInstancesApi.TestOnboardingStepConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse.md)

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

