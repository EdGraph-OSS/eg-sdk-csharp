# EdGraph.Platform.Client.Api.QuestionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateQuestion**](QuestionsApi.md#createquestion) | **POST** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Creates a new Question for a given section |
| [**DeleteQuestion**](QuestionsApi.md#deletequestion) | **DELETE** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Deletes a Question. |
| [**GetQuestion**](QuestionsApi.md#getquestion) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Get Question. |
| [**SearchQuestions**](QuestionsApi.md#searchquestions) | **GET** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions | Search Questions |
| [**UpdateQuestion**](QuestionsApi.md#updatequestion) | **PUT** /tenants/{tenantId}/forms/{formId}/sections/{sectionId}/questions/{questionId} | Updates a Question. |

<a id="createquestion"></a>
# **CreateQuestion**
> FormApiQuestionsV1QuestionCreatedResponse CreateQuestion (Guid tenantId, Guid formId, Guid sectionId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto = null)

Creates a new Question for a given section


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **sectionId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto.md) |  | [optional]  |

### Return type

[**FormApiQuestionsV1QuestionCreatedResponse**](FormApiQuestionsV1QuestionCreatedResponse.md)

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

<a id="deletequestion"></a>
# **DeleteQuestion**
> FormApiQuestionsV1QuestionDeletedResponse DeleteQuestion (Guid tenantId, Guid formId, Guid sectionId, Guid questionId)

Deletes a Question.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **sectionId** | **Guid** |  |  |
| **questionId** | **Guid** |  |  |

### Return type

[**FormApiQuestionsV1QuestionDeletedResponse**](FormApiQuestionsV1QuestionDeletedResponse.md)

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

<a id="getquestion"></a>
# **GetQuestion**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto GetQuestion (Guid tenantId, Guid formId, Guid sectionId, Guid questionId)

Get Question.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **sectionId** | **Guid** |  |  |
| **questionId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto.md)

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

<a id="searchquestions"></a>
# **SearchQuestions**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel SearchQuestions (Guid tenantId, Guid formId, Guid sectionId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search Questions


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **sectionId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel.md)

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

<a id="updatequestion"></a>
# **UpdateQuestion**
> FormApiQuestionsV1QuestionUpdatedResponse UpdateQuestion (Guid tenantId, Guid formId, Guid sectionId, Guid questionId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto = null)

Updates a Question.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **sectionId** | **Guid** |  |  |
| **questionId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto.md) |  | [optional]  |

### Return type

[**FormApiQuestionsV1QuestionUpdatedResponse**](FormApiQuestionsV1QuestionUpdatedResponse.md)

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

