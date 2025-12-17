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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateQuestionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new QuestionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var sectionId = "sectionId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto |  (optional) 

            try
            {
                // Creates a new Question for a given section
                FormApiQuestionsV1QuestionCreatedResponse result = apiInstance.CreateQuestion(tenantId, formId, sectionId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuestionsApi.CreateQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Question for a given section
    ApiResponse<FormApiQuestionsV1QuestionCreatedResponse> response = apiInstance.CreateQuestionWithHttpInfo(tenantId, formId, sectionId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsCreateQuestionRequestDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuestionsApi.CreateQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteQuestionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new QuestionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var sectionId = "sectionId_example";  // Guid | 
            var questionId = "questionId_example";  // Guid | 

            try
            {
                // Deletes a Question.
                FormApiQuestionsV1QuestionDeletedResponse result = apiInstance.DeleteQuestion(tenantId, formId, sectionId, questionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuestionsApi.DeleteQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Question.
    ApiResponse<FormApiQuestionsV1QuestionDeletedResponse> response = apiInstance.DeleteQuestionWithHttpInfo(tenantId, formId, sectionId, questionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuestionsApi.DeleteQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetQuestionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new QuestionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var sectionId = "sectionId_example";  // Guid | 
            var questionId = "questionId_example";  // Guid | 

            try
            {
                // Get Question.
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto result = apiInstance.GetQuestion(tenantId, formId, sectionId, questionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuestionsApi.GetQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Question.
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDto> response = apiInstance.GetQuestionWithHttpInfo(tenantId, formId, sectionId, questionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuestionsApi.GetQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchQuestionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new QuestionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var sectionId = "sectionId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Search Questions
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel result = apiInstance.SearchQuestions(tenantId, formId, sectionId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuestionsApi.SearchQuestions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchQuestionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Questions
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel> response = apiInstance.SearchQuestionsWithHttpInfo(tenantId, formId, sectionId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuestionsApi.SearchQuestionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateQuestionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new QuestionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var sectionId = "sectionId_example";  // Guid | 
            var questionId = "questionId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto = new EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto(); // EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto |  (optional) 

            try
            {
                // Updates a Question.
                FormApiQuestionsV1QuestionUpdatedResponse result = apiInstance.UpdateQuestion(tenantId, formId, sectionId, questionId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling QuestionsApi.UpdateQuestion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateQuestionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Question.
    ApiResponse<FormApiQuestionsV1QuestionUpdatedResponse> response = apiInstance.UpdateQuestionWithHttpInfo(tenantId, formId, sectionId, questionId, edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsFormsUpdateQuestionRequestDto);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling QuestionsApi.UpdateQuestionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

