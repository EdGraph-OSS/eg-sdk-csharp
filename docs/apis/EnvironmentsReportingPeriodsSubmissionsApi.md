# EdGraph.Platform.Client.Api.EnvironmentsReportingPeriodsSubmissionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddReportingPeriodSubmissionMetricsBulkV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#addreportingperiodsubmissionmetricsbulkv2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics/bulk | Adds Metrics to a Submission in bulk. |
| [**AddReportingPeriodSubmissionMetricsV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#addreportingperiodsubmissionmetricsv2) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Adds Metrics to a Submission. |
| [**CancelReportingPeriodSubmissionV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#cancelreportingperiodsubmissionv2) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/cancel | Cancels a Submission. |
| [**GetReportingPeriodSubmissionLatestV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionlatestv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/latest | Retrieves the latest Submission of a Reporting Period. |
| [**GetReportingPeriodSubmissionLogsV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionlogsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/logs | Retrieves a list of Submission Logs of a Reporting Period. |
| [**GetReportingPeriodSubmissionMetricsV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionmetricsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/metrics | Retrieves the Metrics of a Submission. |
| [**GetReportingPeriodSubmissionV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#getreportingperiodsubmissionv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId} | Retrieves the Submission of a Reporting Period. |
| [**GetStateReportingPeriodSubmissionsV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#getstatereportingperiodsubmissionsv2) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions | Retrieves a list of Submissions of a Reporting Period. |
| [**SetReportingPeriodSubmissionStatusV2**](EnvironmentsReportingPeriodsSubmissionsApi.md#setreportingperiodsubmissionstatusv2) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/submissions/{submissionId}/status | Sets the Status of a Submission. |

<a id="addreportingperiodsubmissionmetricsbulkv2"></a>
# **AddReportingPeriodSubmissionMetricsBulkV2**
> EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse AddReportingPeriodSubmissionMetricsBulkV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid submissionId, EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest edGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest = null)

Adds Metrics to a Submission in bulk.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest** | [**EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest**](EdGraphServicesStateReportingV1AddSubmissionMetricsBulkRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse**](EdGraphServicesStateReportingV1SubmissionMetricsAddedBulkResponse.md)

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

<a id="addreportingperiodsubmissionmetricsv2"></a>
# **AddReportingPeriodSubmissionMetricsV2**
> EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse AddReportingPeriodSubmissionMetricsV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid submissionId, EdGraphServicesStateReportingV1AddSubmissionMetricsRequest edGraphServicesStateReportingV1AddSubmissionMetricsRequest = null)

Adds Metrics to a Submission.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1AddSubmissionMetricsRequest** | [**EdGraphServicesStateReportingV1AddSubmissionMetricsRequest**](EdGraphServicesStateReportingV1AddSubmissionMetricsRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse**](EdGraphServicesStateReportingV1SubmissionMetricsAddedResponse.md)

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

<a id="cancelreportingperiodsubmissionv2"></a>
# **CancelReportingPeriodSubmissionV2**
> EdGraphServicesStateReportingV1SubmissionCancelledResponse CancelReportingPeriodSubmissionV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid submissionId)

Cancels a Submission.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1SubmissionCancelledResponse**](EdGraphServicesStateReportingV1SubmissionCancelledResponse.md)

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

<a id="getreportingperiodsubmissionlatestv2"></a>
# **GetReportingPeriodSubmissionLatestV2**
> EdGraphServicesStateReportingV1SubmissionProfile GetReportingPeriodSubmissionLatestV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Retrieves the latest Submission of a Reporting Period.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1SubmissionProfile**](EdGraphServicesStateReportingV1SubmissionProfile.md)

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

<a id="getreportingperiodsubmissionlogsv2"></a>
# **GetReportingPeriodSubmissionLogsV2**
> EdGraphServicesStateReportingV1PaginatedSubmissionLogs GetReportingPeriodSubmissionLogsV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid submissionId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Submission Logs of a Reporting Period.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedSubmissionLogs**](EdGraphServicesStateReportingV1PaginatedSubmissionLogs.md)

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

<a id="getreportingperiodsubmissionmetricsv2"></a>
# **GetReportingPeriodSubmissionMetricsV2**
> EdGraphServicesStateReportingV1SubmissionMetricsResponse GetReportingPeriodSubmissionMetricsV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid submissionId)

Retrieves the Metrics of a Submission.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1SubmissionMetricsResponse**](EdGraphServicesStateReportingV1SubmissionMetricsResponse.md)

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

<a id="getreportingperiodsubmissionv2"></a>
# **GetReportingPeriodSubmissionV2**
> EdGraphServicesStateReportingV1SubmissionProfile GetReportingPeriodSubmissionV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid submissionId)

Retrieves the Submission of a Reporting Period.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1SubmissionProfile**](EdGraphServicesStateReportingV1SubmissionProfile.md)

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

<a id="getstatereportingperiodsubmissionsv2"></a>
# **GetStateReportingPeriodSubmissionsV2**
> EdGraphServicesStateReportingV1PaginatedSubmissions GetStateReportingPeriodSubmissionsV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Submissions of a Reporting Period.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphServicesStateReportingV1PaginatedSubmissions**](EdGraphServicesStateReportingV1PaginatedSubmissions.md)

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

<a id="setreportingperiodsubmissionstatusv2"></a>
# **SetReportingPeriodSubmissionStatusV2**
> EdGraphServicesStateReportingV1SubmissionStatusSetResponse SetReportingPeriodSubmissionStatusV2 (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid submissionId, EdGraphServicesStateReportingV1SetSubmissionStatusRequest edGraphServicesStateReportingV1SetSubmissionStatusRequest = null)

Sets the Status of a Submission.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1SetSubmissionStatusRequest** | [**EdGraphServicesStateReportingV1SetSubmissionStatusRequest**](EdGraphServicesStateReportingV1SetSubmissionStatusRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1SubmissionStatusSetResponse**](EdGraphServicesStateReportingV1SubmissionStatusSetResponse.md)

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

