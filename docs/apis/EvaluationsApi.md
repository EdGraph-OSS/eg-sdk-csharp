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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateEvaluationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var evaluationApiEvaluationsV1CreateEvaluationRequest = new EvaluationApiEvaluationsV1CreateEvaluationRequest(); // EvaluationApiEvaluationsV1CreateEvaluationRequest |  (optional) 

            try
            {
                // Creates a new Evaluation for a given tenant
                EvaluationApiEvaluationsV1EvaluationCreatedResponse result = apiInstance.CreateEvaluation(tenantId, evaluationApiEvaluationsV1CreateEvaluationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.CreateEvaluation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateEvaluationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Evaluation for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationCreatedResponse> response = apiInstance.CreateEvaluationWithHttpInfo(tenantId, evaluationApiEvaluationsV1CreateEvaluationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.CreateEvaluationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteEvaluationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var evaluationId = "evaluationId_example";  // Guid | 

            try
            {
                // Deletes an Evaluation for a given tenant
                EvaluationApiEvaluationsV1EvaluationDeletedResponse result = apiInstance.DeleteEvaluation(tenantId, evaluationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.DeleteEvaluation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteEvaluationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an Evaluation for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationDeletedResponse> response = apiInstance.DeleteEvaluationWithHttpInfo(tenantId, evaluationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.DeleteEvaluationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEvaluationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var evaluationId = "evaluationId_example";  // Guid | 

            try
            {
                // Get an Evaluation for a given tenant
                EvaluationApiEvaluationsV1EvaluationResponse result = apiInstance.GetEvaluation(tenantId, evaluationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.GetEvaluation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEvaluationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an Evaluation for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationResponse> response = apiInstance.GetEvaluationWithHttpInfo(tenantId, evaluationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.GetEvaluationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEvaluationCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                EvaluationApiEvaluationsV1EvaluationCountResponse result = apiInstance.GetEvaluationCount(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.GetEvaluationCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEvaluationCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<EvaluationApiEvaluationsV1EvaluationCountResponse> response = apiInstance.GetEvaluationCountWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.GetEvaluationCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchEvaluationAppraisersExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Appraisers associated with an Evaluation for a given Tenant.
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse result = apiInstance.SearchEvaluationAppraisers(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationAppraisers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchEvaluationAppraisersWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Appraisers associated with an Evaluation for a given Tenant.
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse> response = apiInstance.SearchEvaluationAppraisersWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationAppraisersWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchEvaluationCampusesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Campuses associated with an Evaluation for a given Tenant.
                EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel result = apiInstance.SearchEvaluationCampuses(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationCampuses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchEvaluationCampusesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Campuses associated with an Evaluation for a given Tenant.
    ApiResponse<EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel> response = apiInstance.SearchEvaluationCampusesWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationCampusesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchEvaluationFormsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Forms associated with an Evaluation for a given Tenant.
                EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel result = apiInstance.SearchEvaluationForms(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationForms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchEvaluationFormsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Forms associated with an Evaluation for a given Tenant.
    ApiResponse<EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel> response = apiInstance.SearchEvaluationFormsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationFormsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchEvaluationStaffExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Staff associated with an Evaluation for a given Tenant.
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse result = apiInstance.SearchEvaluationStaff(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationStaff: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchEvaluationStaffWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Staff associated with an Evaluation for a given Tenant.
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse> response = apiInstance.SearchEvaluationStaffWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationStaffWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchEvaluationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Evaluations for a given tenant
                EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel result = apiInstance.SearchEvaluations(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.SearchEvaluations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchEvaluationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Evaluations for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel> response = apiInstance.SearchEvaluationsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.SearchEvaluationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateEvaluationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EvaluationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var evaluationId = "evaluationId_example";  // Guid | 
            var evaluationApiEvaluationsV1UpdateEvaluationRequest = new EvaluationApiEvaluationsV1UpdateEvaluationRequest(); // EvaluationApiEvaluationsV1UpdateEvaluationRequest |  (optional) 

            try
            {
                // Updates an Evaluation for a given tenant
                EvaluationApiEvaluationsV1EvaluationUpdatedResponse result = apiInstance.UpdateEvaluation(tenantId, evaluationId, evaluationApiEvaluationsV1UpdateEvaluationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EvaluationsApi.UpdateEvaluation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateEvaluationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Evaluation for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationUpdatedResponse> response = apiInstance.UpdateEvaluationWithHttpInfo(tenantId, evaluationId, evaluationApiEvaluationsV1UpdateEvaluationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EvaluationsApi.UpdateEvaluationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

