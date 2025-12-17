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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateSubmissionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SubmissionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var formApiSubmissionsV1CreateSubmissionRequest = new FormApiSubmissionsV1CreateSubmissionRequest(); // FormApiSubmissionsV1CreateSubmissionRequest |  (optional) 

            try
            {
                // Creates a new Submission for a given question
                FormApiSubmissionsV1SubmissionCreatedResponse result = apiInstance.CreateSubmission(tenantId, formId, formApiSubmissionsV1CreateSubmissionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubmissionsApi.CreateSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Submission for a given question
    ApiResponse<FormApiSubmissionsV1SubmissionCreatedResponse> response = apiInstance.CreateSubmissionWithHttpInfo(tenantId, formId, formApiSubmissionsV1CreateSubmissionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubmissionsApi.CreateSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteSubmissionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SubmissionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 

            try
            {
                // Deletes a Submission.
                FormApiSubmissionsV1SubmissionDeletedResponse result = apiInstance.DeleteSubmission(tenantId, formId, submissionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubmissionsApi.DeleteSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes a Submission.
    ApiResponse<FormApiSubmissionsV1SubmissionDeletedResponse> response = apiInstance.DeleteSubmissionWithHttpInfo(tenantId, formId, submissionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubmissionsApi.DeleteSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ExportSubmissionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SubmissionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var type = (FormApiSubmissionsV1ExportType) "Unknown";  // FormApiSubmissionsV1ExportType |  (optional) 

            try
            {
                // Exports Submission data for a Form for a given tenant. (With JSON and CSV support)
                FormApiSubmissionsV1SubmissionsExportedResponse result = apiInstance.ExportSubmissions(tenantId, formId, type);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubmissionsApi.ExportSubmissions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ExportSubmissionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Exports Submission data for a Form for a given tenant. (With JSON and CSV support)
    ApiResponse<FormApiSubmissionsV1SubmissionsExportedResponse> response = apiInstance.ExportSubmissionsWithHttpInfo(tenantId, formId, type);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubmissionsApi.ExportSubmissionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetSubmissionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SubmissionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 

            try
            {
                // Get Submission.
                FormApiSubmissionsV1SubmissionResponse result = apiInstance.GetSubmission(tenantId, formId, submissionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubmissionsApi.GetSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Submission.
    ApiResponse<FormApiSubmissionsV1SubmissionResponse> response = apiInstance.GetSubmissionWithHttpInfo(tenantId, formId, submissionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubmissionsApi.GetSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchSubmissionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SubmissionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Search Submissions
                FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel result = apiInstance.SearchSubmissions(tenantId, formId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubmissionsApi.SearchSubmissions: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchSubmissionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Search Submissions
    ApiResponse<FormApiSubmissionsV1SubmissionResponsePaginatedItemsViewModel> response = apiInstance.SearchSubmissionsWithHttpInfo(tenantId, formId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubmissionsApi.SearchSubmissionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateSubmissionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new SubmissionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var formId = "formId_example";  // Guid | 
            var submissionId = "submissionId_example";  // Guid | 
            var formApiSubmissionsV1UpdateSubmissionRequest = new FormApiSubmissionsV1UpdateSubmissionRequest(); // FormApiSubmissionsV1UpdateSubmissionRequest |  (optional) 

            try
            {
                // Updates a Submission.
                FormApiSubmissionsV1SubmissionUpdatedResponse result = apiInstance.UpdateSubmission(tenantId, formId, submissionId, formApiSubmissionsV1UpdateSubmissionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling SubmissionsApi.UpdateSubmission: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateSubmissionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a Submission.
    ApiResponse<FormApiSubmissionsV1SubmissionUpdatedResponse> response = apiInstance.UpdateSubmissionWithHttpInfo(tenantId, formId, submissionId, formApiSubmissionsV1UpdateSubmissionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling SubmissionsApi.UpdateSubmissionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

