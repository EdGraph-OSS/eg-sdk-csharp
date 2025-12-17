# EdGraph.Platform.Client.Api.ReportingPeriodsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddReportingPeriodSubmissionMetrics**](ReportingPeriodsApi.md#addreportingperiodsubmissionmetrics) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission. |
| [**AddReportingPeriodSubmissionMetricsBulk**](ReportingPeriodsApi.md#addreportingperiodsubmissionmetricsbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk. |
| [**CancelReportingPeriodSubmission**](ReportingPeriodsApi.md#cancelreportingperiodsubmission) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission. |
| [**CloseReportingPeriodAsync**](ReportingPeriodsApi.md#closereportingperiodasync) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/close | Closes the state of a Reporting Period. |
| [**DeleteReportingPeriodRules**](ReportingPeriodsApi.md#deletereportingperiodrules) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules | Delete the Reporting Period and Associated Rules |
| [**GetReportingPeriodCertificationStatus**](ReportingPeriodsApi.md#getreportingperiodcertificationstatus) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/certificationstatus | Retrieves the Certification Status of a Reporting Period. |
| [**GetReportingPeriodRecords**](ReportingPeriodsApi.md#getreportingperiodrecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period. |
| [**GetReportingPeriodRuleRecords**](ReportingPeriodsApi.md#getreportingperiodrulerecords) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule. |
| [**GetReportingPeriodSubmission**](ReportingPeriodsApi.md#getreportingperiodsubmission) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period. |
| [**GetReportingPeriodSubmissionLatest**](ReportingPeriodsApi.md#getreportingperiodsubmissionlatest) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period. |
| [**GetReportingPeriodSubmissionLogs**](ReportingPeriodsApi.md#getreportingperiodsubmissionlogs) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period. |
| [**GetReportingPeriodSubmissionMetrics**](ReportingPeriodsApi.md#getreportingperiodsubmissionmetrics) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission. |
| [**GetReportingPeriodSubmissions**](ReportingPeriodsApi.md#getreportingperiodsubmissions) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period. |
| [**GetReportingPeriodValidationSummary**](ReportingPeriodsApi.md#getreportingperiodvalidationsummary) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary | Retrieves the Validation Summary of a Reporting Period. |
| [**GetReportingPeriodValidationSummaryByCategoryId**](ReportingPeriodsApi.md#getreportingperiodvalidationsummarybycategoryid) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/validationsummary/categories/{categoryId} | Retrieves the Validation Summary of a Reporting Period for a Category. |
| [**GetReportingPeriods**](ReportingPeriodsApi.md#getreportingperiods) | **GET** /tenants/{tenantId}/statereporting/reportingperiods | Retrieves a list of Reporting Periods. |
| [**PostReportingPeriod**](ReportingPeriodsApi.md#postreportingperiod) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/post | Post a Reporting Period. |
| [**RunReportingPeriodValidations**](ReportingPeriodsApi.md#runreportingperiodvalidations) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/run | Run Reporting Period Validations. |
| [**SetReportingPeriodRuleRecordExcludeFromPostFlagBulk**](ReportingPeriodsApi.md#setreportingperiodrulerecordexcludefrompostflagbulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Records. |
| [**SetReportingPeriodSubmissionStatus**](ReportingPeriodsApi.md#setreportingperiodsubmissionstatus) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission. |
| [**ToggleReportingPeriodSelection**](ReportingPeriodsApi.md#togglereportingperiodselection) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/toggle | Toggles the Selected state of a Reporting Period. |
| [**UpdateReportingPeriodBulk**](ReportingPeriodsApi.md#updatereportingperiodbulk) | **PUT** /tenants/{tenantId}/statereporting/reportingperiods | Updates Reporting Periods in bulk. |

<a id="addreportingperiodsubmissionmetrics"></a>
# **AddReportingPeriodSubmissionMetrics**
> ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse AddReportingPeriodSubmissionMetrics (Guid tenantId, Guid reportingPeriodId, Guid submissionId, ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest validationsApiReportingPeriodsV1AddSubmissionMetricsRequest = null)

Adds Metrics to a Submission.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddReportingPeriodSubmissionMetricsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 
            var validationsApiReportingPeriodsV1AddSubmissionMetricsRequest = new ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest(); // ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest |  (optional) 

            try
            {
                // Adds Metrics to a Submission.
                ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse result = apiInstance.AddReportingPeriodSubmissionMetrics(tenantId, reportingPeriodId, submissionId, validationsApiReportingPeriodsV1AddSubmissionMetricsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.AddReportingPeriodSubmissionMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddReportingPeriodSubmissionMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds Metrics to a Submission.
    ApiResponse<ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse> response = apiInstance.AddReportingPeriodSubmissionMetricsWithHttpInfo(tenantId, reportingPeriodId, submissionId, validationsApiReportingPeriodsV1AddSubmissionMetricsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.AddReportingPeriodSubmissionMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **validationsApiReportingPeriodsV1AddSubmissionMetricsRequest** | [**ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest**](ValidationsApiReportingPeriodsV1AddSubmissionMetricsRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse**](ValidationsApiReportingPeriodsV1SubmissionMetricsAddedResponse.md)

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

<a id="addreportingperiodsubmissionmetricsbulk"></a>
# **AddReportingPeriodSubmissionMetricsBulk**
> ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse AddReportingPeriodSubmissionMetricsBulk (Guid tenantId, Guid reportingPeriodId, Guid submissionId, ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest = null)

Adds Metrics to a Submission in bulk.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddReportingPeriodSubmissionMetricsBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 
            var validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest = new ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest(); // ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest |  (optional) 

            try
            {
                // Adds Metrics to a Submission in bulk.
                ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse result = apiInstance.AddReportingPeriodSubmissionMetricsBulk(tenantId, reportingPeriodId, submissionId, validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.AddReportingPeriodSubmissionMetricsBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddReportingPeriodSubmissionMetricsBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds Metrics to a Submission in bulk.
    ApiResponse<ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse> response = apiInstance.AddReportingPeriodSubmissionMetricsBulkWithHttpInfo(tenantId, reportingPeriodId, submissionId, validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.AddReportingPeriodSubmissionMetricsBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **validationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest** | [**ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest**](ValidationsApiReportingPeriodsV1AddSubmissionMetricsBulkRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse**](ValidationsApiReportingPeriodsV1SubmissionMetricsAddedBulkResponse.md)

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

<a id="cancelreportingperiodsubmission"></a>
# **CancelReportingPeriodSubmission**
> ValidationsApiReportingPeriodsV1SubmissionCancelledResponse CancelReportingPeriodSubmission (Guid tenantId, Guid reportingPeriodId, Guid submissionId)

Cancels a Submission.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CancelReportingPeriodSubmissionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 

            try
            {
                // Cancels a Submission.
                ValidationsApiReportingPeriodsV1SubmissionCancelledResponse result = apiInstance.CancelReportingPeriodSubmission(tenantId, reportingPeriodId, submissionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.CancelReportingPeriodSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CancelReportingPeriodSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Cancels a Submission.
    ApiResponse<ValidationsApiReportingPeriodsV1SubmissionCancelledResponse> response = apiInstance.CancelReportingPeriodSubmissionWithHttpInfo(tenantId, reportingPeriodId, submissionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.CancelReportingPeriodSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1SubmissionCancelledResponse**](ValidationsApiReportingPeriodsV1SubmissionCancelledResponse.md)

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
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="closereportingperiodasync"></a>
# **CloseReportingPeriodAsync**
> ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse CloseReportingPeriodAsync (Guid tenantId, Guid reportingPeriodId)

Closes the state of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CloseReportingPeriodAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Closes the state of a Reporting Period.
                ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse result = apiInstance.CloseReportingPeriodAsync(tenantId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.CloseReportingPeriodAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CloseReportingPeriodAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Closes the state of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse> response = apiInstance.CloseReportingPeriodAsyncWithHttpInfo(tenantId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.CloseReportingPeriodAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse**](ValidationsApiReportingPeriodsV1CloseReportingPeriodResponse.md)

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

<a id="deletereportingperiodrules"></a>
# **DeleteReportingPeriodRules**
> ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse DeleteReportingPeriodRules (Guid tenantId, Guid reportingPeriodId)

Delete the Reporting Period and Associated Rules

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteReportingPeriodRulesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Delete the Reporting Period and Associated Rules
                ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse result = apiInstance.DeleteReportingPeriodRules(tenantId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.DeleteReportingPeriodRules: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteReportingPeriodRulesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Delete the Reporting Period and Associated Rules
    ApiResponse<ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse> response = apiInstance.DeleteReportingPeriodRulesWithHttpInfo(tenantId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.DeleteReportingPeriodRulesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse**](ValidationsApiReportingPeriodsV1DeleteReportingPeriodRulesResponse.md)

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
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getreportingperiodcertificationstatus"></a>
# **GetReportingPeriodCertificationStatus**
> ValidationsApiReportingPeriodsV1CertificationStatus GetReportingPeriodCertificationStatus (Guid tenantId, Guid reportingPeriodId)

Retrieves the Certification Status of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodCertificationStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Retrieves the Certification Status of a Reporting Period.
                ValidationsApiReportingPeriodsV1CertificationStatus result = apiInstance.GetReportingPeriodCertificationStatus(tenantId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodCertificationStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodCertificationStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Certification Status of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1CertificationStatus> response = apiInstance.GetReportingPeriodCertificationStatusWithHttpInfo(tenantId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodCertificationStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1CertificationStatus**](ValidationsApiReportingPeriodsV1CertificationStatus.md)

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

<a id="getreportingperiodrecords"></a>
# **GetReportingPeriodRecords**
> ValidationsApiReportingPeriodsV1PaginatedRecords GetReportingPeriodRecords (Guid tenantId, Guid reportingPeriodId, int pageIndex = null, int pageSize = null, bool excludedFromPost = null)

Retrieves the Invalid Records of all the Rules within a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodRecordsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var excludedFromPost = true;  // bool |  (optional) 

            try
            {
                // Retrieves the Invalid Records of all the Rules within a Reporting Period.
                ValidationsApiReportingPeriodsV1PaginatedRecords result = apiInstance.GetReportingPeriodRecords(tenantId, reportingPeriodId, pageIndex, pageSize, excludedFromPost);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodRecords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodRecordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Invalid Records of all the Rules within a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1PaginatedRecords> response = apiInstance.GetReportingPeriodRecordsWithHttpInfo(tenantId, reportingPeriodId, pageIndex, pageSize, excludedFromPost);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodRecordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **excludedFromPost** | **bool** |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1PaginatedRecords**](ValidationsApiReportingPeriodsV1PaginatedRecords.md)

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

<a id="getreportingperiodrulerecords"></a>
# **GetReportingPeriodRuleRecords**
> ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2 GetReportingPeriodRuleRecords (Guid tenantId, Guid reportingPeriodId, Guid ruleId, int pageIndex = null, int pageSize = null)

Retrieves the Invalid Records of a Rule.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodRuleRecordsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var ruleId = "ruleId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)

            try
            {
                // Retrieves the Invalid Records of a Rule.
                ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2 result = apiInstance.GetReportingPeriodRuleRecords(tenantId, reportingPeriodId, ruleId, pageIndex, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodRuleRecords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodRuleRecordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Invalid Records of a Rule.
    ApiResponse<ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2> response = apiInstance.GetReportingPeriodRuleRecordsWithHttpInfo(tenantId, reportingPeriodId, ruleId, pageIndex, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodRuleRecordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **ruleId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |

### Return type

[**ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2**](ValidationsApiReportingPeriodsV1PaginatedRuleRecordsV2.md)

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

<a id="getreportingperiodsubmission"></a>
# **GetReportingPeriodSubmission**
> ValidationsApiReportingPeriodsV1SubmissionProfile GetReportingPeriodSubmission (Guid tenantId, Guid reportingPeriodId, Guid submissionId)

Retrieves the Submission of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodSubmissionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 

            try
            {
                // Retrieves the Submission of a Reporting Period.
                ValidationsApiReportingPeriodsV1SubmissionProfile result = apiInstance.GetReportingPeriodSubmission(tenantId, reportingPeriodId, submissionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Submission of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1SubmissionProfile> response = apiInstance.GetReportingPeriodSubmissionWithHttpInfo(tenantId, reportingPeriodId, submissionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1SubmissionProfile**](ValidationsApiReportingPeriodsV1SubmissionProfile.md)

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

<a id="getreportingperiodsubmissionlatest"></a>
# **GetReportingPeriodSubmissionLatest**
> ValidationsApiReportingPeriodsV1SubmissionProfile GetReportingPeriodSubmissionLatest (Guid tenantId, Guid reportingPeriodId)

Retrieves the latest Submission of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodSubmissionLatestExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Retrieves the latest Submission of a Reporting Period.
                ValidationsApiReportingPeriodsV1SubmissionProfile result = apiInstance.GetReportingPeriodSubmissionLatest(tenantId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionLatest: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodSubmissionLatestWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the latest Submission of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1SubmissionProfile> response = apiInstance.GetReportingPeriodSubmissionLatestWithHttpInfo(tenantId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionLatestWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1SubmissionProfile**](ValidationsApiReportingPeriodsV1SubmissionProfile.md)

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

<a id="getreportingperiodsubmissionlogs"></a>
# **GetReportingPeriodSubmissionLogs**
> ValidationsApiReportingPeriodsV1PaginatedSubmissions GetReportingPeriodSubmissionLogs (Guid tenantId, Guid reportingPeriodId, Guid submissionId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Submission Logs of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodSubmissionLogsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of Submission Logs of a Reporting Period.
                ValidationsApiReportingPeriodsV1PaginatedSubmissions result = apiInstance.GetReportingPeriodSubmissionLogs(tenantId, reportingPeriodId, submissionId, pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionLogs: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodSubmissionLogsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Submission Logs of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1PaginatedSubmissions> response = apiInstance.GetReportingPeriodSubmissionLogsWithHttpInfo(tenantId, reportingPeriodId, submissionId, pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionLogsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**ValidationsApiReportingPeriodsV1PaginatedSubmissions**](ValidationsApiReportingPeriodsV1PaginatedSubmissions.md)

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

<a id="getreportingperiodsubmissionmetrics"></a>
# **GetReportingPeriodSubmissionMetrics**
> ValidationsApiReportingPeriodsV1SubmissionMetricsResponse GetReportingPeriodSubmissionMetrics (Guid tenantId, Guid reportingPeriodId, Guid submissionId)

Retrieves the Metrics of a Submission.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodSubmissionMetricsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 

            try
            {
                // Retrieves the Metrics of a Submission.
                ValidationsApiReportingPeriodsV1SubmissionMetricsResponse result = apiInstance.GetReportingPeriodSubmissionMetrics(tenantId, reportingPeriodId, submissionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionMetrics: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodSubmissionMetricsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Metrics of a Submission.
    ApiResponse<ValidationsApiReportingPeriodsV1SubmissionMetricsResponse> response = apiInstance.GetReportingPeriodSubmissionMetricsWithHttpInfo(tenantId, reportingPeriodId, submissionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionMetricsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1SubmissionMetricsResponse**](ValidationsApiReportingPeriodsV1SubmissionMetricsResponse.md)

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

<a id="getreportingperiodsubmissions"></a>
# **GetReportingPeriodSubmissions**
> ValidationsApiReportingPeriodsV1PaginatedSubmissions GetReportingPeriodSubmissions (Guid tenantId, Guid reportingPeriodId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Submissions of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodSubmissionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of Submissions of a Reporting Period.
                ValidationsApiReportingPeriodsV1PaginatedSubmissions result = apiInstance.GetReportingPeriodSubmissions(tenantId, reportingPeriodId, pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodSubmissionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Submissions of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1PaginatedSubmissions> response = apiInstance.GetReportingPeriodSubmissionsWithHttpInfo(tenantId, reportingPeriodId, pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodSubmissionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**ValidationsApiReportingPeriodsV1PaginatedSubmissions**](ValidationsApiReportingPeriodsV1PaginatedSubmissions.md)

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

<a id="getreportingperiodvalidationsummary"></a>
# **GetReportingPeriodValidationSummary**
> ValidationsApiReportingPeriodsV1ValidationSummary GetReportingPeriodValidationSummary (Guid tenantId, Guid reportingPeriodId)

Retrieves the Validation Summary of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodValidationSummaryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Retrieves the Validation Summary of a Reporting Period.
                ValidationsApiReportingPeriodsV1ValidationSummary result = apiInstance.GetReportingPeriodValidationSummary(tenantId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodValidationSummary: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodValidationSummaryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Validation Summary of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1ValidationSummary> response = apiInstance.GetReportingPeriodValidationSummaryWithHttpInfo(tenantId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodValidationSummaryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1ValidationSummary**](ValidationsApiReportingPeriodsV1ValidationSummary.md)

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

<a id="getreportingperiodvalidationsummarybycategoryid"></a>
# **GetReportingPeriodValidationSummaryByCategoryId**
> ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId GetReportingPeriodValidationSummaryByCategoryId (Guid tenantId, Guid reportingPeriodId, Guid categoryId)

Retrieves the Validation Summary of a Reporting Period for a Category.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportingPeriodValidationSummaryByCategoryIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 

            try
            {
                // Retrieves the Validation Summary of a Reporting Period for a Category.
                ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId result = apiInstance.GetReportingPeriodValidationSummaryByCategoryId(tenantId, reportingPeriodId, categoryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodValidationSummaryByCategoryId: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodValidationSummaryByCategoryIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Validation Summary of a Reporting Period for a Category.
    ApiResponse<ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId> response = apiInstance.GetReportingPeriodValidationSummaryByCategoryIdWithHttpInfo(tenantId, reportingPeriodId, categoryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodValidationSummaryByCategoryIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

### Return type

[**ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId**](ValidationsApiReportingPeriodsV1ValidationSummaryByCategoryId.md)

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

<a id="getreportingperiods"></a>
# **GetReportingPeriods**
> ValidationsApiReportingPeriodsV1PaginatedReportingPeriods GetReportingPeriods (Guid tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

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
    public class GetReportingPeriodsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of Reporting Periods.
                ValidationsApiReportingPeriodsV1PaginatedReportingPeriods result = apiInstance.GetReportingPeriods(tenantId, pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriods: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportingPeriodsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Reporting Periods.
    ApiResponse<ValidationsApiReportingPeriodsV1PaginatedReportingPeriods> response = apiInstance.GetReportingPeriodsWithHttpInfo(tenantId, pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.GetReportingPeriodsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**ValidationsApiReportingPeriodsV1PaginatedReportingPeriods**](ValidationsApiReportingPeriodsV1PaginatedReportingPeriods.md)

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

<a id="postreportingperiod"></a>
# **PostReportingPeriod**
> ValidationsApiReportingPeriodsV1PostedResponse PostReportingPeriod (Guid tenantId, Guid reportingPeriodId, ValidationsApiReportingPeriodsV1PostRequest validationsApiReportingPeriodsV1PostRequest = null)

Post a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class PostReportingPeriodExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var validationsApiReportingPeriodsV1PostRequest = new ValidationsApiReportingPeriodsV1PostRequest(); // ValidationsApiReportingPeriodsV1PostRequest |  (optional) 

            try
            {
                // Post a Reporting Period.
                ValidationsApiReportingPeriodsV1PostedResponse result = apiInstance.PostReportingPeriod(tenantId, reportingPeriodId, validationsApiReportingPeriodsV1PostRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.PostReportingPeriod: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the PostReportingPeriodWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Post a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1PostedResponse> response = apiInstance.PostReportingPeriodWithHttpInfo(tenantId, reportingPeriodId, validationsApiReportingPeriodsV1PostRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.PostReportingPeriodWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiReportingPeriodsV1PostRequest** | [**ValidationsApiReportingPeriodsV1PostRequest**](ValidationsApiReportingPeriodsV1PostRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1PostedResponse**](ValidationsApiReportingPeriodsV1PostedResponse.md)

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

<a id="runreportingperiodvalidations"></a>
# **RunReportingPeriodValidations**
> ValidationsApiReportingPeriodsV1RunResponse RunReportingPeriodValidations (Guid tenantId, Guid reportingPeriodId, Guid categoryId = null)

Run Reporting Period Validations.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RunReportingPeriodValidationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid |  (optional) 

            try
            {
                // Run Reporting Period Validations.
                ValidationsApiReportingPeriodsV1RunResponse result = apiInstance.RunReportingPeriodValidations(tenantId, reportingPeriodId, categoryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.RunReportingPeriodValidations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RunReportingPeriodValidationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Run Reporting Period Validations.
    ApiResponse<ValidationsApiReportingPeriodsV1RunResponse> response = apiInstance.RunReportingPeriodValidationsWithHttpInfo(tenantId, reportingPeriodId, categoryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.RunReportingPeriodValidationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1RunResponse**](ValidationsApiReportingPeriodsV1RunResponse.md)

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

<a id="setreportingperiodrulerecordexcludefrompostflagbulk"></a>
# **SetReportingPeriodRuleRecordExcludeFromPostFlagBulk**
> ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse SetReportingPeriodRuleRecordExcludeFromPostFlagBulk (Guid tenantId, Guid reportingPeriodId, Guid ruleId, ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest = null)

Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetReportingPeriodRuleRecordExcludeFromPostFlagBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var ruleId = "ruleId_example";  // Guid | 
            var validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest = new ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest(); // ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest |  (optional) 

            try
            {
                // Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records.
                ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse result = apiInstance.SetReportingPeriodRuleRecordExcludeFromPostFlagBulk(tenantId, reportingPeriodId, ruleId, validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.SetReportingPeriodRuleRecordExcludeFromPostFlagBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetReportingPeriodRuleRecordExcludeFromPostFlagBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records.
    ApiResponse<ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse> response = apiInstance.SetReportingPeriodRuleRecordExcludeFromPostFlagBulkWithHttpInfo(tenantId, reportingPeriodId, ruleId, validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.SetReportingPeriodRuleRecordExcludeFromPostFlagBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **ruleId** | **Guid** |  |  |
| **validationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest** | [**ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest**](ValidationsApiReportingPeriodsV1SetRuleRecordPostFlagBulkRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse**](ValidationsApiReportingPeriodsV1RuleRecordPostFlagSetBulkResponse.md)

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

<a id="setreportingperiodsubmissionstatus"></a>
# **SetReportingPeriodSubmissionStatus**
> ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse SetReportingPeriodSubmissionStatus (Guid tenantId, Guid reportingPeriodId, Guid submissionId, ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest validationsApiReportingPeriodsV1SetSubmissionStatusRequest = null)

Sets the Status of a Submission.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetReportingPeriodSubmissionStatusExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 
            var validationsApiReportingPeriodsV1SetSubmissionStatusRequest = new ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest(); // ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest |  (optional) 

            try
            {
                // Sets the Status of a Submission.
                ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse result = apiInstance.SetReportingPeriodSubmissionStatus(tenantId, reportingPeriodId, submissionId, validationsApiReportingPeriodsV1SetSubmissionStatusRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.SetReportingPeriodSubmissionStatus: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetReportingPeriodSubmissionStatusWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the Status of a Submission.
    ApiResponse<ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse> response = apiInstance.SetReportingPeriodSubmissionStatusWithHttpInfo(tenantId, reportingPeriodId, submissionId, validationsApiReportingPeriodsV1SetSubmissionStatusRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.SetReportingPeriodSubmissionStatusWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **validationsApiReportingPeriodsV1SetSubmissionStatusRequest** | [**ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest**](ValidationsApiReportingPeriodsV1SetSubmissionStatusRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse**](ValidationsApiReportingPeriodsV1SubmissionStatusSetResponse.md)

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

<a id="togglereportingperiodselection"></a>
# **ToggleReportingPeriodSelection**
> ValidationsApiReportingPeriodsV1ToggledResponse ToggleReportingPeriodSelection (Guid tenantId, Guid reportingPeriodId, ValidationsApiReportingPeriodsV1ToggleSelectedRequest validationsApiReportingPeriodsV1ToggleSelectedRequest = null)

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
    public class ToggleReportingPeriodSelectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var validationsApiReportingPeriodsV1ToggleSelectedRequest = new ValidationsApiReportingPeriodsV1ToggleSelectedRequest(); // ValidationsApiReportingPeriodsV1ToggleSelectedRequest |  (optional) 

            try
            {
                // Toggles the Selected state of a Reporting Period.
                ValidationsApiReportingPeriodsV1ToggledResponse result = apiInstance.ToggleReportingPeriodSelection(tenantId, reportingPeriodId, validationsApiReportingPeriodsV1ToggleSelectedRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.ToggleReportingPeriodSelection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ToggleReportingPeriodSelectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Toggles the Selected state of a Reporting Period.
    ApiResponse<ValidationsApiReportingPeriodsV1ToggledResponse> response = apiInstance.ToggleReportingPeriodSelectionWithHttpInfo(tenantId, reportingPeriodId, validationsApiReportingPeriodsV1ToggleSelectedRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.ToggleReportingPeriodSelectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiReportingPeriodsV1ToggleSelectedRequest** | [**ValidationsApiReportingPeriodsV1ToggleSelectedRequest**](ValidationsApiReportingPeriodsV1ToggleSelectedRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1ToggledResponse**](ValidationsApiReportingPeriodsV1ToggledResponse.md)

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

<a id="updatereportingperiodbulk"></a>
# **UpdateReportingPeriodBulk**
> ValidationsApiReportingPeriodsV1UpdatedBulkResponse UpdateReportingPeriodBulk (Guid tenantId, ValidationsApiReportingPeriodsV1UpdateBulkRequest validationsApiReportingPeriodsV1UpdateBulkRequest = null)

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
    public class UpdateReportingPeriodBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportingPeriodsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var validationsApiReportingPeriodsV1UpdateBulkRequest = new ValidationsApiReportingPeriodsV1UpdateBulkRequest(); // ValidationsApiReportingPeriodsV1UpdateBulkRequest |  (optional) 

            try
            {
                // Updates Reporting Periods in bulk.
                ValidationsApiReportingPeriodsV1UpdatedBulkResponse result = apiInstance.UpdateReportingPeriodBulk(tenantId, validationsApiReportingPeriodsV1UpdateBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportingPeriodsApi.UpdateReportingPeriodBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateReportingPeriodBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates Reporting Periods in bulk.
    ApiResponse<ValidationsApiReportingPeriodsV1UpdatedBulkResponse> response = apiInstance.UpdateReportingPeriodBulkWithHttpInfo(tenantId, validationsApiReportingPeriodsV1UpdateBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportingPeriodsApi.UpdateReportingPeriodBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **validationsApiReportingPeriodsV1UpdateBulkRequest** | [**ValidationsApiReportingPeriodsV1UpdateBulkRequest**](ValidationsApiReportingPeriodsV1UpdateBulkRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiReportingPeriodsV1UpdatedBulkResponse**](ValidationsApiReportingPeriodsV1UpdatedBulkResponse.md)

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

