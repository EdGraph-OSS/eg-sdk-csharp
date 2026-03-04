# EdGraph.Platform.Client.Api.AnalyticsDataLakeApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetPaginatedLakehouseRecords**](AnalyticsDataLakeApi.md#getpaginatedlakehouserecords) | **GET** /tenants/{tenantId}/analytics/datalake/query | Retrieves gold-tier data from the lakehouse |

<a id="getpaginatedlakehouserecords"></a>
# **GetPaginatedLakehouseRecords**
> AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse GetPaginatedLakehouseRecords (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves gold-tier data from the lakehouse

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedLakehouseRecordsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new AnalyticsDataLakeApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves gold-tier data from the lakehouse
                AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse result = apiInstance.GetPaginatedLakehouseRecords(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling AnalyticsDataLakeApi.GetPaginatedLakehouseRecords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedLakehouseRecordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves gold-tier data from the lakehouse
    ApiResponse<AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse> response = apiInstance.GetPaginatedLakehouseRecordsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling AnalyticsDataLakeApi.GetPaginatedLakehouseRecordsWithHttpInfo: " + e.Message);
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

[**AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse**](AnalyticsApiLakehousesV1PaginatedLakehouseRecordsResponse.md)

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

