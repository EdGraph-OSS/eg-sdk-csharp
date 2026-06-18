# EdGraph.Platform.Client.Api.StateReportingStepsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetSteps**](StateReportingStepsApi.md#getsteps) | **GET** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Get Steps Status for the tenant. |
| [**UpdateStep**](StateReportingStepsApi.md#updatestep) | **POST** /tenants/{tenantId}/statereporting/schoolYear/{schoolYear}/steps | Update Steps Status for the tenant. |

<a id="getsteps"></a>
# **GetSteps**
> ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse GetSteps (Guid tenantId, int schoolYear)

Get Steps Status for the tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **schoolYear** | **int** |  |  |

### Return type

[**ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse**](ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)

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

<a id="updatestep"></a>
# **UpdateStep**
> ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse UpdateStep (Guid tenantId, int schoolYear, ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest validationsApiStateReportingStepsV1UpdateStateReportingStepRequest = null)

Update Steps Status for the tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **schoolYear** | **int** |  |  |
| **validationsApiStateReportingStepsV1UpdateStateReportingStepRequest** | [**ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest**](ValidationsApiStateReportingStepsV1UpdateStateReportingStepRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse**](ValidationsApiStateReportingStepsV1GetStateReportingStepsResponse.md)

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

