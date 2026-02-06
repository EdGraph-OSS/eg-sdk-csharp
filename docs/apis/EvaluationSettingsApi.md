# EdGraph.Platform.Client.Api.EvaluationSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetEvaluationSetting**](EvaluationSettingsApi.md#getevaluationsetting) | **GET** /tenants/{tenantId}/evaluations/configuration | Gets the Evaluation Settings for a given tenant |
| [**SetEvaluationSettingApplicationSetting**](EvaluationSettingsApi.md#setevaluationsettingapplicationsetting) | **POST** /tenants/{tenantId}/evaluations/configuration/application | Sets the Application Settings of an Evaluation for a given Tenant |
| [**SetEvaluationSettingUserSetting**](EvaluationSettingsApi.md#setevaluationsettingusersetting) | **POST** /tenants/{tenantId}/evaluations/configuration/users | Sets the User Settings of an Evaluation for a given Tenant |

<a id="getevaluationsetting"></a>
# **GetEvaluationSetting**
> EvaluationApiEvaluationSettingsV1EvaluationSettingResponse GetEvaluationSetting (Guid tenantId)

Gets the Evaluation Settings for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEvaluationSettingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Gets the Evaluation Settings for a given tenant
                EvaluationApiEvaluationSettingsV1EvaluationSettingResponse result = apiInstance.GetEvaluationSetting(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationSettingsApi.GetEvaluationSetting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEvaluationSettingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets the Evaluation Settings for a given tenant
    ApiResponse<EvaluationApiEvaluationSettingsV1EvaluationSettingResponse> response = apiInstance.GetEvaluationSettingWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationSettingsApi.GetEvaluationSettingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EvaluationApiEvaluationSettingsV1EvaluationSettingResponse**](EvaluationApiEvaluationSettingsV1EvaluationSettingResponse.md)

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

<a id="setevaluationsettingapplicationsetting"></a>
# **SetEvaluationSettingApplicationSetting**
> EvaluationApiEvaluationSettingsV1ApplicationSetResponse SetEvaluationSettingApplicationSetting (Guid tenantId, EvaluationApiEvaluationSettingsV1SetApplicationRequest evaluationApiEvaluationSettingsV1SetApplicationRequest = null)

Sets the Application Settings of an Evaluation for a given Tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetEvaluationSettingApplicationSettingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var evaluationApiEvaluationSettingsV1SetApplicationRequest = new EvaluationApiEvaluationSettingsV1SetApplicationRequest(); // EvaluationApiEvaluationSettingsV1SetApplicationRequest |  (optional) 

            try
            {
                // Sets the Application Settings of an Evaluation for a given Tenant
                EvaluationApiEvaluationSettingsV1ApplicationSetResponse result = apiInstance.SetEvaluationSettingApplicationSetting(tenantId, evaluationApiEvaluationSettingsV1SetApplicationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationSettingsApi.SetEvaluationSettingApplicationSetting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetEvaluationSettingApplicationSettingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the Application Settings of an Evaluation for a given Tenant
    ApiResponse<EvaluationApiEvaluationSettingsV1ApplicationSetResponse> response = apiInstance.SetEvaluationSettingApplicationSettingWithHttpInfo(tenantId, evaluationApiEvaluationSettingsV1SetApplicationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationSettingsApi.SetEvaluationSettingApplicationSettingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationApiEvaluationSettingsV1SetApplicationRequest** | [**EvaluationApiEvaluationSettingsV1SetApplicationRequest**](EvaluationApiEvaluationSettingsV1SetApplicationRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationSettingsV1ApplicationSetResponse**](EvaluationApiEvaluationSettingsV1ApplicationSetResponse.md)

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

<a id="setevaluationsettingusersetting"></a>
# **SetEvaluationSettingUserSetting**
> EvaluationApiEvaluationSettingsV1UsersSetResponse SetEvaluationSettingUserSetting (Guid tenantId, EvaluationApiEvaluationSettingsV1SetUsersRequest evaluationApiEvaluationSettingsV1SetUsersRequest = null)

Sets the User Settings of an Evaluation for a given Tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetEvaluationSettingUserSettingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var evaluationApiEvaluationSettingsV1SetUsersRequest = new EvaluationApiEvaluationSettingsV1SetUsersRequest(); // EvaluationApiEvaluationSettingsV1SetUsersRequest |  (optional) 

            try
            {
                // Sets the User Settings of an Evaluation for a given Tenant
                EvaluationApiEvaluationSettingsV1UsersSetResponse result = apiInstance.SetEvaluationSettingUserSetting(tenantId, evaluationApiEvaluationSettingsV1SetUsersRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationSettingsApi.SetEvaluationSettingUserSetting: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetEvaluationSettingUserSettingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the User Settings of an Evaluation for a given Tenant
    ApiResponse<EvaluationApiEvaluationSettingsV1UsersSetResponse> response = apiInstance.SetEvaluationSettingUserSettingWithHttpInfo(tenantId, evaluationApiEvaluationSettingsV1SetUsersRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationSettingsApi.SetEvaluationSettingUserSettingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationApiEvaluationSettingsV1SetUsersRequest** | [**EvaluationApiEvaluationSettingsV1SetUsersRequest**](EvaluationApiEvaluationSettingsV1SetUsersRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationSettingsV1UsersSetResponse**](EvaluationApiEvaluationSettingsV1UsersSetResponse.md)

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

