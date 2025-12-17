# EdGraph.Platform.Client.Api.JobTypesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAllTenantDataSyncJobTypes**](JobTypesApi.md#getalltenantdatasyncjobtypes) | **GET** /tenants/{tenantId}/datasync/jobtypes | Retrieves a list of DataSync job types |
| [**GetTenantDataSyncJobTypeProfileById**](JobTypesApi.md#gettenantdatasyncjobtypeprofilebyid) | **GET** /tenants/{tenantId}/datasync/jobtypes/{jobTypeId} | Retrieves a specific DataSync job type using its primary key |

<a id="getalltenantdatasyncjobtypes"></a>
# **GetAllTenantDataSyncJobTypes**
> DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel GetAllTenantDataSyncJobTypes (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of DataSync job types

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllTenantDataSyncJobTypesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobTypesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of DataSync job types
                DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel result = apiInstance.GetAllTenantDataSyncJobTypes(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobTypesApi.GetAllTenantDataSyncJobTypes: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllTenantDataSyncJobTypesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of DataSync job types
    ApiResponse<DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel> response = apiInstance.GetAllTenantDataSyncJobTypesWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobTypesApi.GetAllTenantDataSyncJobTypesWithHttpInfo: " + e.Message);
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

[**DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel**](DataSyncApiJobTypeV1JobTypeListResponsePaginatedItemsViewModel.md)

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

<a id="gettenantdatasyncjobtypeprofilebyid"></a>
# **GetTenantDataSyncJobTypeProfileById**
> DataSyncApiJobTypeV1JobTypeProfileResponse GetTenantDataSyncJobTypeProfileById (string tenantId, string jobTypeId)

Retrieves a specific DataSync job type using its primary key

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantDataSyncJobTypeProfileByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new JobTypesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var jobTypeId = "jobTypeId_example";  // string | 

            try
            {
                // Retrieves a specific DataSync job type using its primary key
                DataSyncApiJobTypeV1JobTypeProfileResponse result = apiInstance.GetTenantDataSyncJobTypeProfileById(tenantId, jobTypeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling JobTypesApi.GetTenantDataSyncJobTypeProfileById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantDataSyncJobTypeProfileByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a specific DataSync job type using its primary key
    ApiResponse<DataSyncApiJobTypeV1JobTypeProfileResponse> response = apiInstance.GetTenantDataSyncJobTypeProfileByIdWithHttpInfo(tenantId, jobTypeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling JobTypesApi.GetTenantDataSyncJobTypeProfileByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **jobTypeId** | **string** |  |  |

### Return type

[**DataSyncApiJobTypeV1JobTypeProfileResponse**](DataSyncApiJobTypeV1JobTypeProfileResponse.md)

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

