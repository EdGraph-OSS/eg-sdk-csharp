# EdGraph.Platform.Client.Api.ReportsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateReportAsync**](ReportsApi.md#createreportasync) | **POST** /tenants/{tenantId}/analytics/reports | Creates a new report (Does not upload pbix file). |
| [**DeleteReportAsync**](ReportsApi.md#deletereportasync) | **DELETE** /tenants/{tenantId}/analytics/reports/{reportId} | Removes a report. |
| [**DownloadReportAsync**](ReportsApi.md#downloadreportasync) | **GET** /tenants/{tenantId}/analytics/reports/download/{reportId}/{groupId} | Retrieves the PBIX for any report in the list in order to download |
| [**GetAllTenantAnalyticsWorkspaceReportsAsync**](ReportsApi.md#getalltenantanalyticsworkspacereportsasync) | **GET** /tenants/{tenantId}/analytics/reports | Retrieves all reports. |
| [**GetReportByIdAsync**](ReportsApi.md#getreportbyidasync) | **GET** /tenants/{tenantId}/analytics/reports/{reportId} | Retrieves a Report by ID. |
| [**SyncLatestVersion**](ReportsApi.md#synclatestversion) | **POST** /tenants/{tenantId}/analytics/reports/synclatestversion | Sync latest version |
| [**SyncWorkspacesAsync**](ReportsApi.md#syncworkspacesasync) | **POST** /tenants/{tenantId}/analytics/reports/sync | Triggers workspace, ODS and DW automation. |
| [**UpdateReportAsync**](ReportsApi.md#updatereportasync) | **PUT** /tenants/{tenantId}/analytics/reports/{reportId} | Updates a report. |

<a id="createreportasync"></a>
# **CreateReportAsync**
> AnalyticsApiReportsV1ReportIdResponse CreateReportAsync (string tenantId, System.IO.Stream file = null, string name = null, string shortDescription = null, string description = null, string tags = null, bool isVisible = null, string version = null, bool identityRequired = null, bool rolesRequired = null)

Creates a new report (Does not upload pbix file).

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream |  (optional) 
            var name = "name_example";  // string |  (optional) 
            var shortDescription = "shortDescription_example";  // string |  (optional) 
            var description = "description_example";  // string |  (optional) 
            var tags = "tags_example";  // string |  (optional) 
            var isVisible = true;  // bool |  (optional) 
            var version = "version_example";  // string |  (optional) 
            var identityRequired = true;  // bool |  (optional) 
            var rolesRequired = true;  // bool |  (optional) 

            try
            {
                // Creates a new report (Does not upload pbix file).
                AnalyticsApiReportsV1ReportIdResponse result = apiInstance.CreateReportAsync(tenantId, file, name, shortDescription, description, tags, isVisible, version, identityRequired, rolesRequired);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.CreateReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new report (Does not upload pbix file).
    ApiResponse<AnalyticsApiReportsV1ReportIdResponse> response = apiInstance.CreateReportAsyncWithHttpInfo(tenantId, file, name, shortDescription, description, tags, isVisible, version, identityRequired, rolesRequired);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.CreateReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **file** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **shortDescription** | **string** |  | [optional]  |
| **description** | **string** |  | [optional]  |
| **tags** | **string** |  | [optional]  |
| **isVisible** | **bool** |  | [optional]  |
| **version** | **string** |  | [optional]  |
| **identityRequired** | **bool** |  | [optional]  |
| **rolesRequired** | **bool** |  | [optional]  |

### Return type

[**AnalyticsApiReportsV1ReportIdResponse**](AnalyticsApiReportsV1ReportIdResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletereportasync"></a>
# **DeleteReportAsync**
> void DeleteReportAsync (string tenantId, string reportId)

Removes a report.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var reportId = "reportId_example";  // string | 

            try
            {
                // Removes a report.
                apiInstance.DeleteReportAsync(tenantId, reportId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.DeleteReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Removes a report.
    apiInstance.DeleteReportAsyncWithHttpInfo(tenantId, reportId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.DeleteReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="downloadreportasync"></a>
# **DownloadReportAsync**
> AnalyticsApiReportsV1DownloadReportResponse DownloadReportAsync (string tenantId, string reportId, string groupId)

Retrieves the PBIX for any report in the list in order to download

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DownloadReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var reportId = "reportId_example";  // string | 
            var groupId = "groupId_example";  // string | 

            try
            {
                // Retrieves the PBIX for any report in the list in order to download
                AnalyticsApiReportsV1DownloadReportResponse result = apiInstance.DownloadReportAsync(tenantId, reportId, groupId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.DownloadReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DownloadReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the PBIX for any report in the list in order to download
    ApiResponse<AnalyticsApiReportsV1DownloadReportResponse> response = apiInstance.DownloadReportAsyncWithHttpInfo(tenantId, reportId, groupId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.DownloadReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |
| **groupId** | **string** |  |  |

### Return type

[**AnalyticsApiReportsV1DownloadReportResponse**](AnalyticsApiReportsV1DownloadReportResponse.md)

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

<a id="getalltenantanalyticsworkspacereportsasync"></a>
# **GetAllTenantAnalyticsWorkspaceReportsAsync**
> AnalyticsApiReportsV1ReportPaginatedItemsResponse GetAllTenantAnalyticsWorkspaceReportsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves all reports.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllTenantAnalyticsWorkspaceReportsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves all reports.
                AnalyticsApiReportsV1ReportPaginatedItemsResponse result = apiInstance.GetAllTenantAnalyticsWorkspaceReportsAsync(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.GetAllTenantAnalyticsWorkspaceReportsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantAnalyticsWorkspaceReportsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves all reports.
    ApiResponse<AnalyticsApiReportsV1ReportPaginatedItemsResponse> response = apiInstance.GetAllTenantAnalyticsWorkspaceReportsAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.GetAllTenantAnalyticsWorkspaceReportsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiReportsV1ReportPaginatedItemsResponse**](AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)

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

<a id="getreportbyidasync"></a>
# **GetReportByIdAsync**
> AnalyticsApiReportsV1ReportResponse GetReportByIdAsync (string tenantId, string reportId)

Retrieves a Report by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var reportId = "reportId_example";  // string | 

            try
            {
                // Retrieves a Report by ID.
                AnalyticsApiReportsV1ReportResponse result = apiInstance.GetReportByIdAsync(tenantId, reportId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.GetReportByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Report by ID.
    ApiResponse<AnalyticsApiReportsV1ReportResponse> response = apiInstance.GetReportByIdAsyncWithHttpInfo(tenantId, reportId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.GetReportByIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |

### Return type

[**AnalyticsApiReportsV1ReportResponse**](AnalyticsApiReportsV1ReportResponse.md)

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

<a id="synclatestversion"></a>
# **SyncLatestVersion**
> Object SyncLatestVersion (string tenantId, AnalyticsApiReportsV1SyncLatestVersionRequest analyticsApiReportsV1SyncLatestVersionRequest = null)

Sync latest version

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SyncLatestVersionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var analyticsApiReportsV1SyncLatestVersionRequest = new AnalyticsApiReportsV1SyncLatestVersionRequest(); // AnalyticsApiReportsV1SyncLatestVersionRequest |  (optional) 

            try
            {
                // Sync latest version
                Object result = apiInstance.SyncLatestVersion(tenantId, analyticsApiReportsV1SyncLatestVersionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.SyncLatestVersion: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SyncLatestVersionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sync latest version
    ApiResponse<Object> response = apiInstance.SyncLatestVersionWithHttpInfo(tenantId, analyticsApiReportsV1SyncLatestVersionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.SyncLatestVersionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiReportsV1SyncLatestVersionRequest** | [**AnalyticsApiReportsV1SyncLatestVersionRequest**](AnalyticsApiReportsV1SyncLatestVersionRequest.md) |  | [optional]  |

### Return type

**Object**

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="syncworkspacesasync"></a>
# **SyncWorkspacesAsync**
> Object SyncWorkspacesAsync (string tenantId, AnalyticsApiReportsV1SyncWorkspacesRequest analyticsApiReportsV1SyncWorkspacesRequest = null)

Triggers workspace, ODS and DW automation.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SyncWorkspacesAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var analyticsApiReportsV1SyncWorkspacesRequest = new AnalyticsApiReportsV1SyncWorkspacesRequest(); // AnalyticsApiReportsV1SyncWorkspacesRequest |  (optional) 

            try
            {
                // Triggers workspace, ODS and DW automation.
                Object result = apiInstance.SyncWorkspacesAsync(tenantId, analyticsApiReportsV1SyncWorkspacesRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.SyncWorkspacesAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SyncWorkspacesAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Triggers workspace, ODS and DW automation.
    ApiResponse<Object> response = apiInstance.SyncWorkspacesAsyncWithHttpInfo(tenantId, analyticsApiReportsV1SyncWorkspacesRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.SyncWorkspacesAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiReportsV1SyncWorkspacesRequest** | [**AnalyticsApiReportsV1SyncWorkspacesRequest**](AnalyticsApiReportsV1SyncWorkspacesRequest.md) |  | [optional]  |

### Return type

**Object**

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatereportasync"></a>
# **UpdateReportAsync**
> AnalyticsApiReportsV1AnalyticsReport UpdateReportAsync (string tenantId, string reportId, System.IO.Stream file = null, string id = null, string name = null, string shortDescription = null, string description = null, string tags = null, bool isVisible = null, string version = null, bool rolesRequired = null, bool identityRequired = null)

Updates a report.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var reportId = "reportId_example";  // string | 
            var file = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream |  (optional) 
            var id = "id_example";  // string |  (optional) 
            var name = "name_example";  // string |  (optional) 
            var shortDescription = "shortDescription_example";  // string |  (optional) 
            var description = "description_example";  // string |  (optional) 
            var tags = "tags_example";  // string |  (optional) 
            var isVisible = true;  // bool |  (optional) 
            var version = "version_example";  // string |  (optional) 
            var rolesRequired = true;  // bool |  (optional) 
            var identityRequired = true;  // bool |  (optional) 

            try
            {
                // Updates a report.
                AnalyticsApiReportsV1AnalyticsReport result = apiInstance.UpdateReportAsync(tenantId, reportId, file, id, name, shortDescription, description, tags, isVisible, version, rolesRequired, identityRequired);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ReportsApi.UpdateReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates a report.
    ApiResponse<AnalyticsApiReportsV1AnalyticsReport> response = apiInstance.UpdateReportAsyncWithHttpInfo(tenantId, reportId, file, id, name, shortDescription, description, tags, isVisible, version, rolesRequired, identityRequired);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ReportsApi.UpdateReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |
| **file** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **id** | **string** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **shortDescription** | **string** |  | [optional]  |
| **description** | **string** |  | [optional]  |
| **tags** | **string** |  | [optional]  |
| **isVisible** | **bool** |  | [optional]  |
| **version** | **string** |  | [optional]  |
| **rolesRequired** | **bool** |  | [optional]  |
| **identityRequired** | **bool** |  | [optional]  |

### Return type

[**AnalyticsApiReportsV1AnalyticsReport**](AnalyticsApiReportsV1AnalyticsReport.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

