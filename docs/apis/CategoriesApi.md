# EdGraph.Platform.Client.Api.CategoriesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddCategoryDataSteward**](CategoriesApi.md#addcategorydatasteward) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards | Adds a Data Steward to a Category. |
| [**AddCategoryDataStewardBulk**](CategoriesApi.md#addcategorydatastewardbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/stewards | Adds a Data Steward to Categories. |
| [**CertifyCategory**](CategoriesApi.md#certifycategory) | **POST** /tenants/{tenantId}/statereporting/categories/{categoryId}/certify | Certifies a Category. |
| [**GetDataUsersBulk**](CategoriesApi.md#getdatausersbulk) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/datausers | Get all Data Users |
| [**GetStateReportingCategories**](CategoriesApi.md#getstatereportingcategories) | **GET** /tenants/{tenantId}/statereporting/categories | Retrieves a list of Categories. |
| [**RemoveCategoryDataOwner**](CategoriesApi.md#removecategorydataowner) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Removes the Data Owner of a Category. |
| [**RemoveCategoryDataSteward**](CategoriesApi.md#removecategorydatasteward) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards/{email} | Removes a Data Steward from a Category. |
| [**RequestCategoryCertificationReminder**](CategoriesApi.md#requestcategorycertificationreminder) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/certificationreminder | Requests a Certification Reminder to be sent. |
| [**SetCategoryDataOwner**](CategoriesApi.md#setcategorydataowner) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Sets the Data Owner of a Category. |
| [**SetCategoryDataOwnerBulk**](CategoriesApi.md#setcategorydataownerbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/owner | Sets the Data Owner of Categories. |
| [**UploadStateReportingCategory**](CategoriesApi.md#uploadstatereportingcategory) | **POST** /tenants/{tenantId}/statereporting/categories/upload | Upload a Category via a JSON file. |
| [**UploadStateReportingPeriodsFromCategoryJson**](CategoriesApi.md#uploadstatereportingperiodsfromcategoryjson) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/upload | Upload a Category via a JSON file. |

<a id="addcategorydatasteward"></a>
# **AddCategoryDataSteward**
> ValidationsApiContainersV1DataStewardAddedResponse AddCategoryDataSteward (Guid tenantId, Guid categoryId, Guid reportingPeriodId, ValidationsApiContainersV1AddDataStewardRequest validationsApiContainersV1AddDataStewardRequest = null)

Adds a Data Steward to a Category.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddCategoryDataStewardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var validationsApiContainersV1AddDataStewardRequest = new ValidationsApiContainersV1AddDataStewardRequest(); // ValidationsApiContainersV1AddDataStewardRequest |  (optional) 

            try
            {
                // Adds a Data Steward to a Category.
                ValidationsApiContainersV1DataStewardAddedResponse result = apiInstance.AddCategoryDataSteward(tenantId, categoryId, reportingPeriodId, validationsApiContainersV1AddDataStewardRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.AddCategoryDataSteward: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddCategoryDataStewardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds a Data Steward to a Category.
    ApiResponse<ValidationsApiContainersV1DataStewardAddedResponse> response = apiInstance.AddCategoryDataStewardWithHttpInfo(tenantId, categoryId, reportingPeriodId, validationsApiContainersV1AddDataStewardRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.AddCategoryDataStewardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1AddDataStewardRequest** | [**ValidationsApiContainersV1AddDataStewardRequest**](ValidationsApiContainersV1AddDataStewardRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataStewardAddedResponse**](ValidationsApiContainersV1DataStewardAddedResponse.md)

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

<a id="addcategorydatastewardbulk"></a>
# **AddCategoryDataStewardBulk**
> ValidationsApiContainersV1DataStewardAddedBulkResponse AddCategoryDataStewardBulk (Guid tenantId, Guid reportingPeriodId, ValidationsApiContainersV1AddDataStewardBulkRequest validationsApiContainersV1AddDataStewardBulkRequest = null)

Adds a Data Steward to Categories.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddCategoryDataStewardBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var validationsApiContainersV1AddDataStewardBulkRequest = new ValidationsApiContainersV1AddDataStewardBulkRequest(); // ValidationsApiContainersV1AddDataStewardBulkRequest |  (optional) 

            try
            {
                // Adds a Data Steward to Categories.
                ValidationsApiContainersV1DataStewardAddedBulkResponse result = apiInstance.AddCategoryDataStewardBulk(tenantId, reportingPeriodId, validationsApiContainersV1AddDataStewardBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.AddCategoryDataStewardBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddCategoryDataStewardBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds a Data Steward to Categories.
    ApiResponse<ValidationsApiContainersV1DataStewardAddedBulkResponse> response = apiInstance.AddCategoryDataStewardBulkWithHttpInfo(tenantId, reportingPeriodId, validationsApiContainersV1AddDataStewardBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.AddCategoryDataStewardBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1AddDataStewardBulkRequest** | [**ValidationsApiContainersV1AddDataStewardBulkRequest**](ValidationsApiContainersV1AddDataStewardBulkRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataStewardAddedBulkResponse**](ValidationsApiContainersV1DataStewardAddedBulkResponse.md)

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

<a id="certifycategory"></a>
# **CertifyCategory**
> ValidationsApiContainersV1CertificationStatusSetResponse CertifyCategory (Guid tenantId, Guid categoryId)

Certifies a Category.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CertifyCategoryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 

            try
            {
                // Certifies a Category.
                ValidationsApiContainersV1CertificationStatusSetResponse result = apiInstance.CertifyCategory(tenantId, categoryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.CertifyCategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CertifyCategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Certifies a Category.
    ApiResponse<ValidationsApiContainersV1CertificationStatusSetResponse> response = apiInstance.CertifyCategoryWithHttpInfo(tenantId, categoryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.CertifyCategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

### Return type

[**ValidationsApiContainersV1CertificationStatusSetResponse**](ValidationsApiContainersV1CertificationStatusSetResponse.md)

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

<a id="getdatausersbulk"></a>
# **GetDataUsersBulk**
> ValidationsApiContainersV1CategoriesWithDataUsersResponse GetDataUsersBulk (Guid tenantId, Guid reportingPeriodId)

Get all Data Users

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetDataUsersBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Get all Data Users
                ValidationsApiContainersV1CategoriesWithDataUsersResponse result = apiInstance.GetDataUsersBulk(tenantId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.GetDataUsersBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetDataUsersBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get all Data Users
    ApiResponse<ValidationsApiContainersV1CategoriesWithDataUsersResponse> response = apiInstance.GetDataUsersBulkWithHttpInfo(tenantId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.GetDataUsersBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**ValidationsApiContainersV1CategoriesWithDataUsersResponse**](ValidationsApiContainersV1CategoriesWithDataUsersResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getstatereportingcategories"></a>
# **GetStateReportingCategories**
> ValidationsApiContainersV1PaginatedContainers GetStateReportingCategories (Guid tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Categories.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStateReportingCategoriesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of Categories.
                ValidationsApiContainersV1PaginatedContainers result = apiInstance.GetStateReportingCategories(tenantId, pageIndex, pageSize, filter, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.GetStateReportingCategories: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStateReportingCategoriesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Categories.
    ApiResponse<ValidationsApiContainersV1PaginatedContainers> response = apiInstance.GetStateReportingCategoriesWithHttpInfo(tenantId, pageIndex, pageSize, filter, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.GetStateReportingCategoriesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**ValidationsApiContainersV1PaginatedContainers**](ValidationsApiContainersV1PaginatedContainers.md)

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

<a id="removecategorydataowner"></a>
# **RemoveCategoryDataOwner**
> void RemoveCategoryDataOwner (Guid tenantId, Guid reportingPeriodId, Guid categoryId)

Removes the Data Owner of a Category.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RemoveCategoryDataOwnerExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 

            try
            {
                // Removes the Data Owner of a Category.
                apiInstance.RemoveCategoryDataOwner(tenantId, reportingPeriodId, categoryId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.RemoveCategoryDataOwner: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveCategoryDataOwnerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Removes the Data Owner of a Category.
    apiInstance.RemoveCategoryDataOwnerWithHttpInfo(tenantId, reportingPeriodId, categoryId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.RemoveCategoryDataOwnerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

### Return type

void (empty response body)

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
| **204** | The resource was successfully deleted. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removecategorydatasteward"></a>
# **RemoveCategoryDataSteward**
> void RemoveCategoryDataSteward (Guid tenantId, Guid categoryId, Guid reportingPeriodId, string email)

Removes a Data Steward from a Category.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RemoveCategoryDataStewardExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var email = "email_example";  // string | 

            try
            {
                // Removes a Data Steward from a Category.
                apiInstance.RemoveCategoryDataSteward(tenantId, categoryId, reportingPeriodId, email);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.RemoveCategoryDataSteward: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveCategoryDataStewardWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Removes a Data Steward from a Category.
    apiInstance.RemoveCategoryDataStewardWithHttpInfo(tenantId, categoryId, reportingPeriodId, email);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.RemoveCategoryDataStewardWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **email** | **string** |  |  |

### Return type

void (empty response body)

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
| **204** | The resource was successfully deleted. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="requestcategorycertificationreminder"></a>
# **RequestCategoryCertificationReminder**
> ValidationsApiContainersV1CertificationReminderRequestedResponse RequestCategoryCertificationReminder (Guid tenantId, Guid reportingPeriodId, Guid categoryId)

Requests a Certification Reminder to be sent.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RequestCategoryCertificationReminderExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 

            try
            {
                // Requests a Certification Reminder to be sent.
                ValidationsApiContainersV1CertificationReminderRequestedResponse result = apiInstance.RequestCategoryCertificationReminder(tenantId, reportingPeriodId, categoryId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.RequestCategoryCertificationReminder: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RequestCategoryCertificationReminderWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Requests a Certification Reminder to be sent.
    ApiResponse<ValidationsApiContainersV1CertificationReminderRequestedResponse> response = apiInstance.RequestCategoryCertificationReminderWithHttpInfo(tenantId, reportingPeriodId, categoryId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.RequestCategoryCertificationReminderWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

### Return type

[**ValidationsApiContainersV1CertificationReminderRequestedResponse**](ValidationsApiContainersV1CertificationReminderRequestedResponse.md)

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

<a id="setcategorydataowner"></a>
# **SetCategoryDataOwner**
> ValidationsApiContainersV1DataOwnerSetResponse SetCategoryDataOwner (Guid tenantId, Guid categoryId, Guid reportingPeriodId, ValidationsApiContainersV1SetDataOwnerRequest validationsApiContainersV1SetDataOwnerRequest = null)

Sets the Data Owner of a Category.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetCategoryDataOwnerExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var categoryId = "categoryId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var validationsApiContainersV1SetDataOwnerRequest = new ValidationsApiContainersV1SetDataOwnerRequest(); // ValidationsApiContainersV1SetDataOwnerRequest |  (optional) 

            try
            {
                // Sets the Data Owner of a Category.
                ValidationsApiContainersV1DataOwnerSetResponse result = apiInstance.SetCategoryDataOwner(tenantId, categoryId, reportingPeriodId, validationsApiContainersV1SetDataOwnerRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.SetCategoryDataOwner: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetCategoryDataOwnerWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the Data Owner of a Category.
    ApiResponse<ValidationsApiContainersV1DataOwnerSetResponse> response = apiInstance.SetCategoryDataOwnerWithHttpInfo(tenantId, categoryId, reportingPeriodId, validationsApiContainersV1SetDataOwnerRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.SetCategoryDataOwnerWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1SetDataOwnerRequest** | [**ValidationsApiContainersV1SetDataOwnerRequest**](ValidationsApiContainersV1SetDataOwnerRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataOwnerSetResponse**](ValidationsApiContainersV1DataOwnerSetResponse.md)

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

<a id="setcategorydataownerbulk"></a>
# **SetCategoryDataOwnerBulk**
> ValidationsApiContainersV1DataOwnerSetBulkResponse SetCategoryDataOwnerBulk (Guid tenantId, Guid reportingPeriodId, ValidationsApiContainersV1SetDataOwnerBulkRequest validationsApiContainersV1SetDataOwnerBulkRequest = null)

Sets the Data Owner of Categories.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetCategoryDataOwnerBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var validationsApiContainersV1SetDataOwnerBulkRequest = new ValidationsApiContainersV1SetDataOwnerBulkRequest(); // ValidationsApiContainersV1SetDataOwnerBulkRequest |  (optional) 

            try
            {
                // Sets the Data Owner of Categories.
                ValidationsApiContainersV1DataOwnerSetBulkResponse result = apiInstance.SetCategoryDataOwnerBulk(tenantId, reportingPeriodId, validationsApiContainersV1SetDataOwnerBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.SetCategoryDataOwnerBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetCategoryDataOwnerBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the Data Owner of Categories.
    ApiResponse<ValidationsApiContainersV1DataOwnerSetBulkResponse> response = apiInstance.SetCategoryDataOwnerBulkWithHttpInfo(tenantId, reportingPeriodId, validationsApiContainersV1SetDataOwnerBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.SetCategoryDataOwnerBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1SetDataOwnerBulkRequest** | [**ValidationsApiContainersV1SetDataOwnerBulkRequest**](ValidationsApiContainersV1SetDataOwnerBulkRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataOwnerSetBulkResponse**](ValidationsApiContainersV1DataOwnerSetBulkResponse.md)

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

<a id="uploadstatereportingcategory"></a>
# **UploadStateReportingCategory**
> ValidationsApiContainersV1CollectionUploadedResponse UploadStateReportingCategory (Guid tenantId, string contentType = null, string contentDisposition = null, Dictionary<string, List<string>> headers = null, long length = null, string name = null, string fileName = null)

Upload a Category via a JSON file.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UploadStateReportingCategoryExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var contentType = "contentType_example";  // string |  (optional) 
            var contentDisposition = "contentDisposition_example";  // string |  (optional) 
            var headers = new Dictionary<string, List<string>>(); // Dictionary<string, List<string>> |  (optional) 
            var length = 789L;  // long |  (optional) 
            var name = "name_example";  // string |  (optional) 
            var fileName = "fileName_example";  // string |  (optional) 

            try
            {
                // Upload a Category via a JSON file.
                ValidationsApiContainersV1CollectionUploadedResponse result = apiInstance.UploadStateReportingCategory(tenantId, contentType, contentDisposition, headers, length, name, fileName);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.UploadStateReportingCategory: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadStateReportingCategoryWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload a Category via a JSON file.
    ApiResponse<ValidationsApiContainersV1CollectionUploadedResponse> response = apiInstance.UploadStateReportingCategoryWithHttpInfo(tenantId, contentType, contentDisposition, headers, length, name, fileName);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.UploadStateReportingCategoryWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **contentType** | **string** |  | [optional]  |
| **contentDisposition** | **string** |  | [optional]  |
| **headers** | [**Dictionary&lt;string, List&lt;string&gt;&gt;**](Dictionary.md) |  | [optional]  |
| **length** | **long** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **fileName** | **string** |  | [optional]  |

### Return type

[**ValidationsApiContainersV1CollectionUploadedResponse**](ValidationsApiContainersV1CollectionUploadedResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
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

<a id="uploadstatereportingperiodsfromcategoryjson"></a>
# **UploadStateReportingPeriodsFromCategoryJson**
> ValidationsApiContainersV1CollectionUploadedResponse UploadStateReportingPeriodsFromCategoryJson (Guid tenantId, Guid environmentId, string contentType = null, string contentDisposition = null, Dictionary<string, List<string>> headers = null, long length = null, string name = null, string fileName = null)

Upload a Category via a JSON file.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UploadStateReportingPeriodsFromCategoryJsonExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new CategoriesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var contentType = "contentType_example";  // string |  (optional) 
            var contentDisposition = "contentDisposition_example";  // string |  (optional) 
            var headers = new Dictionary<string, List<string>>(); // Dictionary<string, List<string>> |  (optional) 
            var length = 789L;  // long |  (optional) 
            var name = "name_example";  // string |  (optional) 
            var fileName = "fileName_example";  // string |  (optional) 

            try
            {
                // Upload a Category via a JSON file.
                ValidationsApiContainersV1CollectionUploadedResponse result = apiInstance.UploadStateReportingPeriodsFromCategoryJson(tenantId, environmentId, contentType, contentDisposition, headers, length, name, fileName);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling CategoriesApi.UploadStateReportingPeriodsFromCategoryJson: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UploadStateReportingPeriodsFromCategoryJsonWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Upload a Category via a JSON file.
    ApiResponse<ValidationsApiContainersV1CollectionUploadedResponse> response = apiInstance.UploadStateReportingPeriodsFromCategoryJsonWithHttpInfo(tenantId, environmentId, contentType, contentDisposition, headers, length, name, fileName);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling CategoriesApi.UploadStateReportingPeriodsFromCategoryJsonWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **contentType** | **string** |  | [optional]  |
| **contentDisposition** | **string** |  | [optional]  |
| **headers** | [**Dictionary&lt;string, List&lt;string&gt;&gt;**](Dictionary.md) |  | [optional]  |
| **length** | **long** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **fileName** | **string** |  | [optional]  |

### Return type

[**ValidationsApiContainersV1CollectionUploadedResponse**](ValidationsApiContainersV1CollectionUploadedResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
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

