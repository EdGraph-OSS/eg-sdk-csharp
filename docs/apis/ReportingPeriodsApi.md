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

