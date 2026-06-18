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

