# EdGraph.Platform.Client.Api.SubmissionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateSubmission**](SubmissionsApi.md#createsubmission) | **POST** /tenants/{tenantId}/forms/{formId}/submissions | Creates a new Submission for a given question |
| [**DeleteSubmission**](SubmissionsApi.md#deletesubmission) | **DELETE** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Deletes a Submission. |
| [**ExportSubmissions**](SubmissionsApi.md#exportsubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/export | Exports Submission data for a Form for a given tenant. (With JSON and CSV support) |
| [**GetSubmission**](SubmissionsApi.md#getsubmission) | **GET** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Get Submission. |
| [**SearchSubmissions**](SubmissionsApi.md#searchsubmissions) | **GET** /tenants/{tenantId}/forms/{formId}/submissions | Search Submissions |
| [**UpdateSubmission**](SubmissionsApi.md#updatesubmission) | **PUT** /tenants/{tenantId}/forms/{formId}/submissions/{submissionId} | Updates a Submission. |

<a id="createsubmission"></a>
# **CreateSubmission**
> FormApiSubmissionsV1SubmissionCreatedResponse CreateSubmission (Guid tenantId, Guid formId, FormApiSubmissionsV1CreateSubmissionRequest formApiSubmissionsV1CreateSubmissionRequest = null)

Creates a new Submission for a given question


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **formApiSubmissionsV1CreateSubmissionRequest** | [**FormApiSubmissionsV1CreateSubmissionRequest**](FormApiSubmissionsV1CreateSubmissionRequest.md) |  | [optional]  |

### Return type

[**FormApiSubmissionsV1SubmissionCreatedResponse**](FormApiSubmissionsV1SubmissionCreatedResponse.md)

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

<a id="deletesubmission"></a>
# **DeleteSubmission**
> FormApiSubmissionsV1SubmissionDeletedResponse DeleteSubmission (Guid tenantId, Guid formId, Guid submissionId)

Deletes a Submission.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**FormApiSubmissionsV1SubmissionDeletedResponse**](FormApiSubmissionsV1SubmissionDeletedResponse.md)

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

<a id="exportsubmissions"></a>
# **ExportSubmissions**
> FormApiSubmissionsV1SubmissionsExportedResponse ExportSubmissions (Guid tenantId, Guid formId, FormApiSubmissionsV1ExportType type = null)

Exports Submission data for a Form for a given tenant. (With JSON and CSV support)


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **type** | **FormApiSubmissionsV1ExportType** |  | [optional]  |

### Return type

[**FormApiSubmissionsV1SubmissionsExportedResponse**](FormApiSubmissionsV1SubmissionsExportedResponse.md)

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

<a id="getsubmission"></a>
# **GetSubmission**
> FormApiSubmissionsV1SubmissionResponse GetSubmission (Guid tenantId, Guid formId, Guid submissionId)

Get Submission.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |

### Return type

[**FormApiSubmissionsV1SubmissionResponse**](FormApiSubmissionsV1SubmissionResponse.md)

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

<a id="searchsubmissions"></a>
# **SearchSubmissions**
> FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel SearchSubmissions (Guid tenantId, Guid formId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search Submissions


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel**](FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel.md)

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

<a id="updatesubmission"></a>
# **UpdateSubmission**
> FormApiSubmissionsV1SubmissionUpdatedResponse UpdateSubmission (Guid tenantId, Guid formId, Guid submissionId, FormApiSubmissionsV1UpdateSubmissionRequest formApiSubmissionsV1UpdateSubmissionRequest = null)

Updates a Submission.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **submissionId** | **Guid** |  |  |
| **formApiSubmissionsV1UpdateSubmissionRequest** | [**FormApiSubmissionsV1UpdateSubmissionRequest**](FormApiSubmissionsV1UpdateSubmissionRequest.md) |  | [optional]  |

### Return type

[**FormApiSubmissionsV1SubmissionUpdatedResponse**](FormApiSubmissionsV1SubmissionUpdatedResponse.md)

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

