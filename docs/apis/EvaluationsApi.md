# EdGraph.Platform.Client.Api.EvaluationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEvaluation**](EvaluationsApi.md#createevaluation) | **POST** /tenants/{tenantId}/evaluations | Creates a new Evaluation for a given tenant |
| [**DeleteEvaluation**](EvaluationsApi.md#deleteevaluation) | **DELETE** /tenants/{tenantId}/evaluations/{evaluationId} | Deletes an Evaluation for a given tenant |
| [**GetEvaluation**](EvaluationsApi.md#getevaluation) | **GET** /tenants/{tenantId}/evaluations/{evaluationId} | Get an Evaluation for a given tenant |
| [**GetEvaluationCount**](EvaluationsApi.md#getevaluationcount) | **GET** /tenants/{tenantId}/evaluations/count |  |
| [**SearchEvaluationAppraisers**](EvaluationsApi.md#searchevaluationappraisers) | **GET** /tenants/{tenantId}/evaluations/appraisers | Searches the Appraisers associated with an Evaluation for a given Tenant. |
| [**SearchEvaluationCampuses**](EvaluationsApi.md#searchevaluationcampuses) | **GET** /tenants/{tenantId}/evaluations/campuses | Searches the Campuses associated with an Evaluation for a given Tenant. |
| [**SearchEvaluationForms**](EvaluationsApi.md#searchevaluationforms) | **GET** /tenants/{tenantId}/evaluations/forms | Searches the Forms associated with an Evaluation for a given Tenant. |
| [**SearchEvaluationStaff**](EvaluationsApi.md#searchevaluationstaff) | **GET** /tenants/{tenantId}/evaluations/staff | Searches the Staff associated with an Evaluation for a given Tenant. |
| [**SearchEvaluations**](EvaluationsApi.md#searchevaluations) | **GET** /tenants/{tenantId}/evaluations | Searches the Evaluations for a given tenant |
| [**UpdateEvaluation**](EvaluationsApi.md#updateevaluation) | **PUT** /tenants/{tenantId}/evaluations/{evaluationId} | Updates an Evaluation for a given tenant |

<a id="createevaluation"></a>
# **CreateEvaluation**
> EvaluationApiEvaluationsV1EvaluationCreatedResponse CreateEvaluation (Guid tenantId, EvaluationApiEvaluationsV1CreateEvaluationRequest evaluationApiEvaluationsV1CreateEvaluationRequest = null)

Creates a new Evaluation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationApiEvaluationsV1CreateEvaluationRequest** | [**EvaluationApiEvaluationsV1CreateEvaluationRequest**](EvaluationApiEvaluationsV1CreateEvaluationRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationCreatedResponse**](EvaluationApiEvaluationsV1EvaluationCreatedResponse.md)

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

<a id="deleteevaluation"></a>
# **DeleteEvaluation**
> EvaluationApiEvaluationsV1EvaluationDeletedResponse DeleteEvaluation (Guid tenantId, Guid evaluationId)

Deletes an Evaluation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationId** | **Guid** |  |  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationDeletedResponse**](EvaluationApiEvaluationsV1EvaluationDeletedResponse.md)

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

<a id="getevaluation"></a>
# **GetEvaluation**
> EvaluationApiEvaluationsV1EvaluationResponse GetEvaluation (Guid tenantId, Guid evaluationId)

Get an Evaluation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationId** | **Guid** |  |  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationResponse**](EvaluationApiEvaluationsV1EvaluationResponse.md)

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

<a id="getevaluationcount"></a>
# **GetEvaluationCount**
> EvaluationApiEvaluationsV1EvaluationCountResponse GetEvaluationCount (Guid tenantId)




### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationCountResponse**](EvaluationApiEvaluationsV1EvaluationCountResponse.md)

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

<a id="searchevaluationappraisers"></a>
# **SearchEvaluationAppraisers**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse SearchEvaluationAppraisers (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Appraisers associated with an Evaluation for a given Tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse.md)

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

<a id="searchevaluationcampuses"></a>
# **SearchEvaluationCampuses**
> EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel SearchEvaluationCampuses (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Campuses associated with an Evaluation for a given Tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel**](EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel.md)

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

<a id="searchevaluationforms"></a>
# **SearchEvaluationForms**
> EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel SearchEvaluationForms (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Forms associated with an Evaluation for a given Tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel**](EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel.md)

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

<a id="searchevaluationstaff"></a>
# **SearchEvaluationStaff**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse SearchEvaluationStaff (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Staff associated with an Evaluation for a given Tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse.md)

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

<a id="searchevaluations"></a>
# **SearchEvaluations**
> EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel SearchEvaluations (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Evaluations for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel**](EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel.md)

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

<a id="updateevaluation"></a>
# **UpdateEvaluation**
> EvaluationApiEvaluationsV1EvaluationUpdatedResponse UpdateEvaluation (Guid tenantId, Guid evaluationId, EvaluationApiEvaluationsV1UpdateEvaluationRequest evaluationApiEvaluationsV1UpdateEvaluationRequest = null)

Updates an Evaluation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationId** | **Guid** |  |  |
| **evaluationApiEvaluationsV1UpdateEvaluationRequest** | [**EvaluationApiEvaluationsV1UpdateEvaluationRequest**](EvaluationApiEvaluationsV1UpdateEvaluationRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationUpdatedResponse**](EvaluationApiEvaluationsV1EvaluationUpdatedResponse.md)

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

