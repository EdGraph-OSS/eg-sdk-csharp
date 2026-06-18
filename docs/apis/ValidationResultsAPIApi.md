# EdGraph.Platform.Client.Api.ValidationResultsAPIApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**FindResultsApiJobRunRecordsAsync**](ValidationResultsAPIApi.md#findresultsapijobrunrecordsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/records | Retrieves a list of Job Run Records from the Validation Results API. |
| [**FindResultsApiJobRunRuleRecordsAsync**](ValidationResultsAPIApi.md#findresultsapijobrunrulerecordsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/records | Retrieves a list of Job Run Rule Records from the Validation Results API. |
| [**FindResultsApiJobRunRulesAsync**](ValidationResultsAPIApi.md#findresultsapijobrunrulesasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules | Retrieves a list of Job Run Rules from the Validation Results API. |
| [**FindResultsApiJobRunsAsync**](ValidationResultsAPIApi.md#findresultsapijobrunsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs | Retrieves a list of Job Runs from the Validation Results API. |
| [**FindResultsApiJobsAsync**](ValidationResultsAPIApi.md#findresultsapijobsasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs | Retrieves a list of Jobs from the Validation Results API. |
| [**FindResultsApiRuleSummaries**](ValidationResultsAPIApi.md#findresultsapirulesummaries) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/summary | Retrieves a list Rule Summaries from the Validation Results API. |
| [**FindResultsApiRulesAsync**](ValidationResultsAPIApi.md#findresultsapirulesasync) | **GET** /tenants/{tenantId}/validations/results-api/rules | Retrieves a list of Rules from Validation Results API. |
| [**GetLatestJobRunAsync**](ValidationResultsAPIApi.md#getlatestjobrunasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/latest | Retrieves the latest Job Run from the Validation Results API. |
| [**GetResultsApiJobById**](ValidationResultsAPIApi.md#getresultsapijobbyid) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId} | Retrieves a Job by ID from the Validation Results API. |
| [**GetResultsApiJobRunByIdAsync**](ValidationResultsAPIApi.md#getresultsapijobrunbyidasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId} | Retrieves a Job Run by ID from the Validation Results API. |
| [**GetResultsApiJobRunRuleByIdAsync**](ValidationResultsAPIApi.md#getresultsapijobrunrulebyidasync) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId} | Retrieves a Job Run Rule by ID from the Validation Results API. |
| [**GetResultsApiRuleByIdAsync**](ValidationResultsAPIApi.md#getresultsapirulebyidasync) | **GET** /tenants/{tenantId}/validations/results-api/rules/{ruleId} | Retrieves a Rule by ID from the Validation Results API. |
| [**GetResultsApiRuleSummary**](ValidationResultsAPIApi.md#getresultsapirulesummary) | **GET** /tenants/{tenantId}/validations/results-api/jobs/{jobId}/runs/{runId}/rules/{ruleId}/summary | Get Rule Summary by ID from the Validation Results API. |

<a id="findresultsapijobrunrecordsasync"></a>
# **FindResultsApiJobRunRecordsAsync**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto&gt; FindResultsApiJobRunRecordsAsync (string tenantId, string jobId, string runId, int offset = null, int limit = null)

Retrieves a list of Job Run Records from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **runId** | **string** |  |  |
| **offset** | **int** |  | [optional] [default to 0] |
| **limit** | **int** |  | [optional] [default to 25] |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto.md)

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

<a id="findresultsapijobrunrulerecordsasync"></a>
# **FindResultsApiJobRunRuleRecordsAsync**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto&gt; FindResultsApiJobRunRuleRecordsAsync (string tenantId, string jobId, string runId, string ruleId, int offset = null, int limit = null)

Retrieves a list of Job Run Rule Records from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **runId** | **string** |  |  |
| **ruleId** | **string** |  |  |
| **offset** | **int** |  | [optional] [default to 0] |
| **limit** | **int** |  | [optional] [default to 25] |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRecordsRecordDto.md)

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

<a id="findresultsapijobrunrulesasync"></a>
# **FindResultsApiJobRunRulesAsync**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto&gt; FindResultsApiJobRunRulesAsync (string tenantId, string jobId, string runId, int offset = null, int limit = null)

Retrieves a list of Job Run Rules from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **runId** | **string** |  |  |
| **offset** | **int** |  | [optional] [default to 0] |
| **limit** | **int** |  | [optional] [default to 25] |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

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

<a id="findresultsapijobrunsasync"></a>
# **FindResultsApiJobRunsAsync**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto&gt; FindResultsApiJobRunsAsync (string tenantId, string jobId, int offset = null, int limit = null)

Retrieves a list of Job Runs from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **offset** | **int** |  | [optional] [default to 0] |
| **limit** | **int** |  | [optional] [default to 25] |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)

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

<a id="findresultsapijobsasync"></a>
# **FindResultsApiJobsAsync**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto&gt; FindResultsApiJobsAsync (string tenantId, int offset = null, int limit = null)

Retrieves a list of Jobs from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **offset** | **int** |  | [optional] [default to 0] |
| **limit** | **int** |  | [optional] [default to 25] |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto.md)

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

<a id="findresultsapirulesummaries"></a>
# **FindResultsApiRuleSummaries**
> List&lt;ValidationsApiResultsV1RuleSummary&gt; FindResultsApiRuleSummaries (Guid tenantId, Guid jobId, Guid runId, int offset = null, int limit = null)

Retrieves a list Rule Summaries from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |
| **runId** | **Guid** |  |  |
| **offset** | **int** |  | [optional] [default to 0] |
| **limit** | **int** |  | [optional] [default to 25] |

### Return type

[**List&lt;ValidationsApiResultsV1RuleSummary&gt;**](ValidationsApiResultsV1RuleSummary.md)

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

<a id="findresultsapirulesasync"></a>
# **FindResultsApiRulesAsync**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto&gt; FindResultsApiRulesAsync (string tenantId, int offset = null, int limit = null)

Retrieves a list of Rules from Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **offset** | **int** |  | [optional] [default to 0] |
| **limit** | **int** |  | [optional] [default to 25] |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

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

<a id="getlatestjobrunasync"></a>
# **GetLatestJobRunAsync**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto GetLatestJobRunAsync (string tenantId, string jobId)

Retrieves the latest Job Run from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)

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

<a id="getresultsapijobbyid"></a>
# **GetResultsApiJobById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto GetResultsApiJobById (string tenantId, string jobId)

Retrieves a Job by ID from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiJobsJobDto.md)

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

<a id="getresultsapijobrunbyidasync"></a>
# **GetResultsApiJobRunByIdAsync**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto GetResultsApiJobRunByIdAsync (string tenantId, string jobId, string runId)

Retrieves a Job Run by ID from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **runId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRunsRunDto.md)

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

<a id="getresultsapijobrunrulebyidasync"></a>
# **GetResultsApiJobRunRuleByIdAsync**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto GetResultsApiJobRunRuleByIdAsync (string tenantId, string jobId, string runId, string ruleId)

Retrieves a Job Run Rule by ID from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobId** | **string** |  |  |
| **runId** | **string** |  |  |
| **ruleId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

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

<a id="getresultsapirulebyidasync"></a>
# **GetResultsApiRuleByIdAsync**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto GetResultsApiRuleByIdAsync (string tenantId, string ruleId)

Retrieves a Rule by ID from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **ruleId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesValidationResultsApiRulesRuleDto.md)

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

<a id="getresultsapirulesummary"></a>
# **GetResultsApiRuleSummary**
> ValidationsApiResultsV1RuleSummary GetResultsApiRuleSummary (Guid tenantId, Guid jobId, Guid runId, Guid ruleId)

Get Rule Summary by ID from the Validation Results API.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **jobId** | **Guid** |  |  |
| **runId** | **Guid** |  |  |
| **ruleId** | **Guid** |  |  |

### Return type

[**ValidationsApiResultsV1RuleSummary**](ValidationsApiResultsV1RuleSummary.md)

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

