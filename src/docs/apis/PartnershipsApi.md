# EdGraph.Platform.Client.Api.PartnershipsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetAllPartnerships**](PartnershipsApi.md#getallpartnerships) | **GET** /tenants/{tenantId}/partnerships | Retrieves a list of Partnerships. |
| [**GetPartnershipById**](PartnershipsApi.md#getpartnershipbyid) | **GET** /tenants/{tenantId}/partnerships/{partnershipId} | Retrieves a Partnership by ID. |

<a id="getallpartnerships"></a>
# **GetAllPartnerships**
> TenantApiPartnershipV1PaginatedItemsResponse GetAllPartnerships (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string partnerTenantId = null, List<string> partnershipType = null, bool excludeSoftDeleted = null)

Retrieves a list of Partnerships.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetAllPartnershipsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new PartnershipsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "orderBy_example";  // string |  (optional) 
            var partnerTenantId = "partnerTenantId_example";  // string |  (optional) 
            var partnershipType = new List<string>(); // List<string> |  (optional) 
            var excludeSoftDeleted = true;  // bool |  (optional)  (default to true)

            try
            {
                // Retrieves a list of Partnerships.
                TenantApiPartnershipV1PaginatedItemsResponse result = apiInstance.GetAllPartnerships(tenantId, pageIndex, pageSize, orderBy, partnerTenantId, partnershipType, excludeSoftDeleted);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PartnershipsApi.GetAllPartnerships: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetAllPartnershipsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Partnerships.
    ApiResponse<TenantApiPartnershipV1PaginatedItemsResponse> response = apiInstance.GetAllPartnershipsWithHttpInfo(tenantId, pageIndex, pageSize, orderBy, partnerTenantId, partnershipType, excludeSoftDeleted);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PartnershipsApi.GetAllPartnershipsWithHttpInfo: " + e.Message);
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
| **orderBy** | **string** |  | [optional]  |
| **partnerTenantId** | **string** |  | [optional]  |
| **partnershipType** | [**List&lt;string&gt;**](string.md) |  | [optional]  |
| **excludeSoftDeleted** | **bool** |  | [optional] [default to true] |

### Return type

[**TenantApiPartnershipV1PaginatedItemsResponse**](TenantApiPartnershipV1PaginatedItemsResponse.md)

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

<a id="getpartnershipbyid"></a>
# **GetPartnershipById**
> TenantApiPartnershipV1PartnershipByIdResponse GetPartnershipById (Guid tenantId, Guid partnershipId, bool excludeSoftDeleted = null)

Retrieves a Partnership by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPartnershipByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new PartnershipsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var partnershipId = "partnershipId_example";  // Guid | 
            var excludeSoftDeleted = true;  // bool |  (optional)  (default to true)

            try
            {
                // Retrieves a Partnership by ID.
                TenantApiPartnershipV1PartnershipByIdResponse result = apiInstance.GetPartnershipById(tenantId, partnershipId, excludeSoftDeleted);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling PartnershipsApi.GetPartnershipById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPartnershipByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a Partnership by ID.
    ApiResponse<TenantApiPartnershipV1PartnershipByIdResponse> response = apiInstance.GetPartnershipByIdWithHttpInfo(tenantId, partnershipId, excludeSoftDeleted);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling PartnershipsApi.GetPartnershipByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **partnershipId** | **Guid** |  |  |
| **excludeSoftDeleted** | **bool** |  | [optional] [default to true] |

### Return type

[**TenantApiPartnershipV1PartnershipByIdResponse**](TenantApiPartnershipV1PartnershipByIdResponse.md)

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

