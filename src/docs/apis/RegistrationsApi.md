# EdGraph.Platform.Client.Api.RegistrationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetOnboardingApplicationsAsync**](RegistrationsApi.md#getonboardingapplicationsasync) | **GET** /public/applications | Gets a list of applications available for registration/onboarding |
| [**GetRegistrationApprovalStatusAsync**](RegistrationsApi.md#getregistrationapprovalstatusasync) | **GET** /registrations/{registrationId} | Gets the approval status of a registration |
| [**SubmitTenantRegistrationAsync**](RegistrationsApi.md#submittenantregistrationasync) | **POST** /registrations | Submits a tenant&#39;s registration request |

<a id="getonboardingapplicationsasync"></a>
# **GetOnboardingApplicationsAsync**
> ApplicationApiApplicationV1PaginatedItemsResponse GetOnboardingApplicationsAsync (int pageSize = null, int pageIndex = null, string orderBy = null)

Gets a list of applications available for registration/onboarding

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetOnboardingApplicationsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new RegistrationsApi(config);
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Gets a list of applications available for registration/onboarding
                ApplicationApiApplicationV1PaginatedItemsResponse result = apiInstance.GetOnboardingApplicationsAsync(pageSize, pageIndex, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RegistrationsApi.GetOnboardingApplicationsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetOnboardingApplicationsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets a list of applications available for registration/onboarding
    ApiResponse<ApplicationApiApplicationV1PaginatedItemsResponse> response = apiInstance.GetOnboardingApplicationsAsyncWithHttpInfo(pageSize, pageIndex, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RegistrationsApi.GetOnboardingApplicationsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**ApplicationApiApplicationV1PaginatedItemsResponse**](ApplicationApiApplicationV1PaginatedItemsResponse.md)

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

<a id="getregistrationapprovalstatusasync"></a>
# **GetRegistrationApprovalStatusAsync**
> RegistrationApiRegistrationV2ApprovalStatus GetRegistrationApprovalStatusAsync (string registrationId)

Gets the approval status of a registration

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetRegistrationApprovalStatusAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new RegistrationsApi(config);
            var registrationId = "registrationId_example";  // string | 

            try
            {
                // Gets the approval status of a registration
                RegistrationApiRegistrationV2ApprovalStatus result = apiInstance.GetRegistrationApprovalStatusAsync(registrationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RegistrationsApi.GetRegistrationApprovalStatusAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetRegistrationApprovalStatusAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets the approval status of a registration
    ApiResponse<RegistrationApiRegistrationV2ApprovalStatus> response = apiInstance.GetRegistrationApprovalStatusAsyncWithHttpInfo(registrationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RegistrationsApi.GetRegistrationApprovalStatusAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **registrationId** | **string** |  |  |

### Return type

[**RegistrationApiRegistrationV2ApprovalStatus**](RegistrationApiRegistrationV2ApprovalStatus.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="submittenantregistrationasync"></a>
# **SubmitTenantRegistrationAsync**
> string SubmitTenantRegistrationAsync (RegistrationApiRegistrationV2SubmitTenantRegistrationRequest registrationApiRegistrationV2SubmitTenantRegistrationRequest = null)

Submits a tenant's registration request

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SubmitTenantRegistrationAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new RegistrationsApi(config);
            var registrationApiRegistrationV2SubmitTenantRegistrationRequest = new RegistrationApiRegistrationV2SubmitTenantRegistrationRequest(); // RegistrationApiRegistrationV2SubmitTenantRegistrationRequest |  (optional) 

            try
            {
                // Submits a tenant's registration request
                string result = apiInstance.SubmitTenantRegistrationAsync(registrationApiRegistrationV2SubmitTenantRegistrationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling RegistrationsApi.SubmitTenantRegistrationAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SubmitTenantRegistrationAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Submits a tenant's registration request
    ApiResponse<string> response = apiInstance.SubmitTenantRegistrationAsyncWithHttpInfo(registrationApiRegistrationV2SubmitTenantRegistrationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling RegistrationsApi.SubmitTenantRegistrationAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **registrationApiRegistrationV2SubmitTenantRegistrationRequest** | [**RegistrationApiRegistrationV2SubmitTenantRegistrationRequest**](RegistrationApiRegistrationV2SubmitTenantRegistrationRequest.md) |  | [optional]  |

### Return type

**string**

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

