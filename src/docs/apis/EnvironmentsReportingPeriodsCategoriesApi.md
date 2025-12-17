# EdGraph.Platform.Client.Api.EnvironmentsReportingPeriodsCategoriesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**SearchStateReportingPeriodCategories**](EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories | Retrieves the Categories of a Reporting Period. |
| [**SearchStateReportingPeriodSubCategories**](EnvironmentsReportingPeriodsCategoriesApi.md#searchstatereportingperiodsubcategories) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/categories/{categoryId}/subcategories | Retrieves the Sub-Categories of a Reporting Period. |

<a id="searchstatereportingperiodcategories"></a>
# **SearchStateReportingPeriodCategories**
> EdGraphServicesStateReportingV1PaginatedCategories SearchStateReportingPeriodCategories (Guid tenantId, Guid environmentId, Guid reportingPeriodId, int pageIndex = null, int pageSize = null, string orderBy = null)

Retrieves the Categories of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchStateReportingPeriodCategoriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsCategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var pageIndex = 56;  // int |  (optional) 
            var pageSize = 56;  // int |  (optional) 
            var orderBy = "orderBy_example";  // string |  (optional) 

            try
            {
                // Retrieves the Categories of a Reporting Period.
                EdGraphServicesStateReportingV1PaginatedCategories result = apiInstance.SearchStateReportingPeriodCategories(tenantId, environmentId, reportingPeriodId, pageIndex, pageSize, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsCategoriesApi.SearchStateReportingPeriodCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchStateReportingPeriodCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Categories of a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1PaginatedCategories> response = apiInstance.SearchStateReportingPeriodCategoriesWithHttpInfo(tenantId, environmentId, reportingPeriodId, pageIndex, pageSize, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsCategoriesApi.SearchStateReportingPeriodCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedCategories**](EdGraphServicesStateReportingV1PaginatedCategories.md)

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

<a id="searchstatereportingperiodsubcategories"></a>
# **SearchStateReportingPeriodSubCategories**
> EdGraphServicesStateReportingV1PaginatedSubCategories SearchStateReportingPeriodSubCategories (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid categoryId, int pageIndex = null, int pageSize = null, string orderBy = null)

Retrieves the Sub-Categories of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchStateReportingPeriodSubCategoriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsCategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 
            var pageIndex = 56;  // int |  (optional) 
            var pageSize = 56;  // int |  (optional) 
            var orderBy = "orderBy_example";  // string |  (optional) 

            try
            {
                // Retrieves the Sub-Categories of a Reporting Period.
                EdGraphServicesStateReportingV1PaginatedSubCategories result = apiInstance.SearchStateReportingPeriodSubCategories(tenantId, environmentId, reportingPeriodId, categoryId, pageIndex, pageSize, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsCategoriesApi.SearchStateReportingPeriodSubCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchStateReportingPeriodSubCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Sub-Categories of a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1PaginatedSubCategories> response = apiInstance.SearchStateReportingPeriodSubCategoriesWithHttpInfo(tenantId, environmentId, reportingPeriodId, categoryId, pageIndex, pageSize, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsCategoriesApi.SearchStateReportingPeriodSubCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedSubCategories**](EdGraphServicesStateReportingV1PaginatedSubCategories.md)

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

