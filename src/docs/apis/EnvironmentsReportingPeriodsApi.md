# EdGraph.Platform.Client.Api.EnvironmentsReportingPeriodsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CancelStateReportingPeriodRun**](EnvironmentsReportingPeriodsApi.md#cancelstatereportingperiodrun) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Cancel the Validation Run of a Reporting Period. |
| [**CloseStateReportingPeriod**](EnvironmentsReportingPeriodsApi.md#closestatereportingperiod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/close | Closes a Reporting Period. |
| [**CreateStateReportingPeriod**](EnvironmentsReportingPeriodsApi.md#createstatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Creates a new Reporting Period. |
| [**DeleteStateReportingPeriod**](EnvironmentsReportingPeriodsApi.md#deletestatereportingperiod) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Deletes a Reporting Period. |
| [**GetStateReportingPeriod**](EnvironmentsReportingPeriodsApi.md#getstatereportingperiod) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Retrieves a Reporting Period by ID. |
| [**GetStateReportingPeriodCertificationStatus**](EnvironmentsReportingPeriodsApi.md#getstatereportingperiodcertificationstatus) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of Reporting Period. |
| [**GetStateReportingPeriodValidationSummary**](EnvironmentsReportingPeriodsApi.md#getstatereportingperiodvalidationsummary) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of Reporting Period. |
| [**GetStateReportingPeriodValidationSummaryByCategory**](EnvironmentsReportingPeriodsApi.md#getstatereportingperiodvalidationsummarybycategory) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of Reporting Period by Category. |
| [**PostStateReportingPeriod**](EnvironmentsReportingPeriodsApi.md#poststatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/post | Posts a Reporting Period. |
| [**RunStateReportingPeriod**](EnvironmentsReportingPeriodsApi.md#runstatereportingperiod) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/run | Run a Reporting Period. |
| [**SearchStateReportingPeriods**](EnvironmentsReportingPeriodsApi.md#searchstatereportingperiods) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Retrieves a list of Reporting Periods. |
| [**SetStateReportingPeriodCurrentStep**](EnvironmentsReportingPeriodsApi.md#setstatereportingperiodcurrentstep) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/current | Sets the current step of a Reporting Period. |
| [**SetStateReportingPeriodStepStatus**](EnvironmentsReportingPeriodsApi.md#setstatereportingperiodstepstatus) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/steps/{stepNumber} | Sets the status of a Reporting Period step. |
| [**ToggleStateReportingPeriodSelected**](EnvironmentsReportingPeriodsApi.md#togglestatereportingperiodselected) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period. |
| [**UpdateStateReportingPeriod**](EnvironmentsReportingPeriodsApi.md#updatestatereportingperiod) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId} | Updates a Reporting Period. |
| [**UpdateStateReportingPeriodBulk**](EnvironmentsReportingPeriodsApi.md#updatestatereportingperiodbulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods | Updates Reporting Periods in bulk. |

<a id="cancelstatereportingperiodrun"></a>
# **CancelStateReportingPeriodRun**
> EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse CancelStateReportingPeriodRun (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Cancel the Validation Run of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CancelStateReportingPeriodRunExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Cancel the Validation Run of a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse result = apiInstance.CancelStateReportingPeriodRun(tenantId, environmentId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.CancelStateReportingPeriodRun: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelStateReportingPeriodRunWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancel the Validation Run of a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse> response = apiInstance.CancelStateReportingPeriodRunWithHttpInfo(tenantId, environmentId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.CancelStateReportingPeriodRunWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse**](EdGraphServicesStateReportingV1ReportingPeriodValidationsCancelledResponse.md)

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

<a id="closestatereportingperiod"></a>
# **CloseStateReportingPeriod**
> EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse CloseStateReportingPeriod (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Closes a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CloseStateReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Closes a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse result = apiInstance.CloseStateReportingPeriod(tenantId, environmentId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.CloseStateReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CloseStateReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Closes a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse> response = apiInstance.CloseStateReportingPeriodWithHttpInfo(tenantId, environmentId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.CloseStateReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createstatereportingperiod"></a>
# **CreateStateReportingPeriod**
> EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse CreateStateReportingPeriod (Guid tenantId, Guid environmentId, EdGraphServicesStateReportingV1CreateReportingPeriodRequest edGraphServicesStateReportingV1CreateReportingPeriodRequest = null)

Creates a new Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateStateReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var edGraphServicesStateReportingV1CreateReportingPeriodRequest = new EdGraphServicesStateReportingV1CreateReportingPeriodRequest(); // EdGraphServicesStateReportingV1CreateReportingPeriodRequest |  (optional) 

            try
            {
                // Creates a new Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse result = apiInstance.CreateStateReportingPeriod(tenantId, environmentId, edGraphServicesStateReportingV1CreateReportingPeriodRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.CreateStateReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateStateReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse> response = apiInstance.CreateStateReportingPeriodWithHttpInfo(tenantId, environmentId, edGraphServicesStateReportingV1CreateReportingPeriodRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.CreateStateReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1CreateReportingPeriodRequest** | [**EdGraphServicesStateReportingV1CreateReportingPeriodRequest**](EdGraphServicesStateReportingV1CreateReportingPeriodRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

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

<a id="deletestatereportingperiod"></a>
# **DeleteStateReportingPeriod**
> EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse DeleteStateReportingPeriod (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Deletes a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteStateReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Deletes a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse result = apiInstance.DeleteStateReportingPeriod(tenantId, environmentId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.DeleteStateReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteStateReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse> response = apiInstance.DeleteStateReportingPeriodWithHttpInfo(tenantId, environmentId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.DeleteStateReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse**](EdGraphServicesStateReportingV1ReportingPeriodDeletedResponse.md)

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

<a id="getstatereportingperiod"></a>
# **GetStateReportingPeriod**
> EdGraphServicesStateReportingV1ReportingPeriodProfileResponse GetStateReportingPeriod (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Retrieves a Reporting Period by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStateReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Retrieves a Reporting Period by ID.
                EdGraphServicesStateReportingV1ReportingPeriodProfileResponse result = apiInstance.GetStateReportingPeriod(tenantId, environmentId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStateReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Reporting Period by ID.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodProfileResponse> response = apiInstance.GetStateReportingPeriodWithHttpInfo(tenantId, environmentId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodProfileResponse**](EdGraphServicesStateReportingV1ReportingPeriodProfileResponse.md)

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

<a id="getstatereportingperiodcertificationstatus"></a>
# **GetStateReportingPeriodCertificationStatus**
> EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus GetStateReportingPeriodCertificationStatus (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Retrieves the Certification Status of Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStateReportingPeriodCertificationStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Retrieves the Certification Status of Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus result = apiInstance.GetStateReportingPeriodCertificationStatus(tenantId, environmentId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriodCertificationStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStateReportingPeriodCertificationStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Certification Status of Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus> response = apiInstance.GetStateReportingPeriodCertificationStatusWithHttpInfo(tenantId, environmentId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriodCertificationStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus**](EdGraphServicesStateReportingV1ReportingPeriodCertificationStatus.md)

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

<a id="getstatereportingperiodvalidationsummary"></a>
# **GetStateReportingPeriodValidationSummary**
> EdGraphServicesStateReportingV1ReportingPeriodValidationSummary GetStateReportingPeriodValidationSummary (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Retrieves the Validation Summary of Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStateReportingPeriodValidationSummaryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Retrieves the Validation Summary of Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodValidationSummary result = apiInstance.GetStateReportingPeriodValidationSummary(tenantId, environmentId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriodValidationSummary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStateReportingPeriodValidationSummaryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Validation Summary of Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodValidationSummary> response = apiInstance.GetStateReportingPeriodValidationSummaryWithHttpInfo(tenantId, environmentId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriodValidationSummaryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodValidationSummary**](EdGraphServicesStateReportingV1ReportingPeriodValidationSummary.md)

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

<a id="getstatereportingperiodvalidationsummarybycategory"></a>
# **GetStateReportingPeriodValidationSummaryByCategory**
> EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId GetStateReportingPeriodValidationSummaryByCategory (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid categoryId)

Retrieves the Validation Summary of Reporting Period by Category.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStateReportingPeriodValidationSummaryByCategoryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 

            try
            {
                // Retrieves the Validation Summary of Reporting Period by Category.
                EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId result = apiInstance.GetStateReportingPeriodValidationSummaryByCategory(tenantId, environmentId, reportingPeriodId, categoryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriodValidationSummaryByCategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStateReportingPeriodValidationSummaryByCategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Validation Summary of Reporting Period by Category.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId> response = apiInstance.GetStateReportingPeriodValidationSummaryByCategoryWithHttpInfo(tenantId, environmentId, reportingPeriodId, categoryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.GetStateReportingPeriodValidationSummaryByCategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId**](EdGraphServicesStateReportingV1ReportingPeriodValidationSummaryByCategoryId.md)

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

<a id="poststatereportingperiod"></a>
# **PostStateReportingPeriod**
> EdGraphServicesStateReportingV1ReportingPeriodPostedResponse PostStateReportingPeriod (Guid tenantId, Guid environmentId, Guid reportingPeriodId, EdGraphServicesStateReportingV1PostReportingPeriodRequest edGraphServicesStateReportingV1PostReportingPeriodRequest = null)

Posts a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class PostStateReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var edGraphServicesStateReportingV1PostReportingPeriodRequest = new EdGraphServicesStateReportingV1PostReportingPeriodRequest(); // EdGraphServicesStateReportingV1PostReportingPeriodRequest |  (optional) 

            try
            {
                // Posts a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodPostedResponse result = apiInstance.PostStateReportingPeriod(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1PostReportingPeriodRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.PostStateReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostStateReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Posts a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodPostedResponse> response = apiInstance.PostStateReportingPeriodWithHttpInfo(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1PostReportingPeriodRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.PostStateReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1PostReportingPeriodRequest** | [**EdGraphServicesStateReportingV1PostReportingPeriodRequest**](EdGraphServicesStateReportingV1PostReportingPeriodRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodPostedResponse**](EdGraphServicesStateReportingV1ReportingPeriodPostedResponse.md)

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

<a id="runstatereportingperiod"></a>
# **RunStateReportingPeriod**
> EdGraphServicesStateReportingV1ReportingPeriodRunResponse RunStateReportingPeriod (Guid tenantId, Guid environmentId, Guid reportingPeriodId, EdGraphServicesStateReportingV1RunReportingPeriodRequest edGraphServicesStateReportingV1RunReportingPeriodRequest = null)

Run a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RunStateReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var edGraphServicesStateReportingV1RunReportingPeriodRequest = new EdGraphServicesStateReportingV1RunReportingPeriodRequest(); // EdGraphServicesStateReportingV1RunReportingPeriodRequest |  (optional) 

            try
            {
                // Run a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodRunResponse result = apiInstance.RunStateReportingPeriod(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1RunReportingPeriodRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.RunStateReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RunStateReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodRunResponse> response = apiInstance.RunStateReportingPeriodWithHttpInfo(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1RunReportingPeriodRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.RunStateReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1RunReportingPeriodRequest** | [**EdGraphServicesStateReportingV1RunReportingPeriodRequest**](EdGraphServicesStateReportingV1RunReportingPeriodRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodRunResponse**](EdGraphServicesStateReportingV1ReportingPeriodRunResponse.md)

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

<a id="searchstatereportingperiods"></a>
# **SearchStateReportingPeriods**
> EdGraphServicesStateReportingV1PaginatedReportingPeriods SearchStateReportingPeriods (Guid tenantId, Guid environmentId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of Reporting Periods.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchStateReportingPeriodsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "orderBy_example";  // string |  (optional) 
            var filter = "filter_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Reporting Periods.
                EdGraphServicesStateReportingV1PaginatedReportingPeriods result = apiInstance.SearchStateReportingPeriods(tenantId, environmentId, pageIndex, pageSize, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.SearchStateReportingPeriods: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchStateReportingPeriodsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Reporting Periods.
    ApiResponse<EdGraphServicesStateReportingV1PaginatedReportingPeriods> response = apiInstance.SearchStateReportingPeriodsWithHttpInfo(tenantId, environmentId, pageIndex, pageSize, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.SearchStateReportingPeriodsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional]  |
| **filter** | **string** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedReportingPeriods**](EdGraphServicesStateReportingV1PaginatedReportingPeriods.md)

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

<a id="setstatereportingperiodcurrentstep"></a>
# **SetStateReportingPeriodCurrentStep**
> EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse SetStateReportingPeriodCurrentStep (Guid tenantId, Guid environmentId, Guid reportingPeriodId, EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest = null)

Sets the current step of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetStateReportingPeriodCurrentStepExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest = new EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest(); // EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest |  (optional) 

            try
            {
                // Sets the current step of a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse result = apiInstance.SetStateReportingPeriodCurrentStep(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.SetStateReportingPeriodCurrentStep: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetStateReportingPeriodCurrentStepWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the current step of a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse> response = apiInstance.SetStateReportingPeriodCurrentStepWithHttpInfo(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.SetStateReportingPeriodCurrentStepWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest** | [**EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest**](EdGraphServicesStateReportingV1SetReportingPeriodCurrentStepRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse**](EdGraphServicesStateReportingV1ReportingPeriodCurrentStepSetResponse.md)

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

<a id="setstatereportingperiodstepstatus"></a>
# **SetStateReportingPeriodStepStatus**
> EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse SetStateReportingPeriodStepStatus (Guid tenantId, Guid environmentId, Guid reportingPeriodId, int stepNumber, EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest = null)

Sets the status of a Reporting Period step.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetStateReportingPeriodStepStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var stepNumber = 56;  // int | 
            var edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest = new EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest(); // EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest |  (optional) 

            try
            {
                // Sets the status of a Reporting Period step.
                EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse result = apiInstance.SetStateReportingPeriodStepStatus(tenantId, environmentId, reportingPeriodId, stepNumber, edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.SetStateReportingPeriodStepStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetStateReportingPeriodStepStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the status of a Reporting Period step.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse> response = apiInstance.SetStateReportingPeriodStepStatusWithHttpInfo(tenantId, environmentId, reportingPeriodId, stepNumber, edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.SetStateReportingPeriodStepStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **stepNumber** | **int** |  |  |
| **edGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest** | [**EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest**](EdGraphServicesStateReportingV1SetReportingPeriodStepStatusRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

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

<a id="togglestatereportingperiodselected"></a>
# **ToggleStateReportingPeriodSelected**
> EdGraphServicesStateReportingV1ReportingPeriodToggledResponse ToggleStateReportingPeriodSelected (Guid tenantId, Guid environmentId, Guid reportingPeriodId, EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest = null)

Toggles the Selected state of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ToggleStateReportingPeriodSelectedExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest = new EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest(); // EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest |  (optional) 

            try
            {
                // Toggles the Selected state of a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodToggledResponse result = apiInstance.ToggleStateReportingPeriodSelected(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.ToggleStateReportingPeriodSelected: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ToggleStateReportingPeriodSelectedWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Toggles the Selected state of a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodToggledResponse> response = apiInstance.ToggleStateReportingPeriodSelectedWithHttpInfo(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.ToggleStateReportingPeriodSelectedWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest** | [**EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest**](EdGraphServicesStateReportingV1ToggleReportingPeriodSelectedRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodToggledResponse**](EdGraphServicesStateReportingV1ReportingPeriodToggledResponse.md)

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

<a id="updatestatereportingperiod"></a>
# **UpdateStateReportingPeriod**
> EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse UpdateStateReportingPeriod (Guid tenantId, Guid environmentId, Guid reportingPeriodId, EdGraphServicesStateReportingV1UpdateReportingPeriodRequest edGraphServicesStateReportingV1UpdateReportingPeriodRequest = null)

Updates a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateStateReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var edGraphServicesStateReportingV1UpdateReportingPeriodRequest = new EdGraphServicesStateReportingV1UpdateReportingPeriodRequest(); // EdGraphServicesStateReportingV1UpdateReportingPeriodRequest |  (optional) 

            try
            {
                // Updates a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse result = apiInstance.UpdateStateReportingPeriod(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1UpdateReportingPeriodRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.UpdateStateReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStateReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse> response = apiInstance.UpdateStateReportingPeriodWithHttpInfo(tenantId, environmentId, reportingPeriodId, edGraphServicesStateReportingV1UpdateReportingPeriodRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.UpdateStateReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1UpdateReportingPeriodRequest** | [**EdGraphServicesStateReportingV1UpdateReportingPeriodRequest**](EdGraphServicesStateReportingV1UpdateReportingPeriodRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse**](EdGraphServicesStateReportingV1ReportingPeriodUpdatedResponse.md)

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

<a id="updatestatereportingperiodbulk"></a>
# **UpdateStateReportingPeriodBulk**
> EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse UpdateStateReportingPeriodBulk (Guid tenantId, Guid environmentId, EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest = null)

Updates Reporting Periods in bulk.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateStateReportingPeriodBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest = new EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest(); // EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest |  (optional) 

            try
            {
                // Updates Reporting Periods in bulk.
                EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse result = apiInstance.UpdateStateReportingPeriodBulk(tenantId, environmentId, edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.UpdateStateReportingPeriodBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateStateReportingPeriodBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates Reporting Periods in bulk.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse> response = apiInstance.UpdateStateReportingPeriodBulkWithHttpInfo(tenantId, environmentId, edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsApi.UpdateStateReportingPeriodBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest** | [**EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest**](EdGraphServicesStateReportingV1UpdateReportingPeriodBulkRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse**](EdGraphServicesStateReportingV1ReportingPeriodUpdatedBulkResponse.md)

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

