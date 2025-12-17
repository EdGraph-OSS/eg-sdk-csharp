# EdGraph.Platform.Client.Api.TenantBrandingApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**UpdateTenantBranding**](TenantBrandingApi.md#updatetenantbranding) | **PUT** /tenants/{tenantId}/branding | Updates the branding of tenant |

<a id="updatetenantbranding"></a>
# **UpdateTenantBranding**
> TenantApiTenantV1TenantUpdatedResponse UpdateTenantBranding (Guid tenantId, System.IO.Stream logoFile = null, System.IO.Stream backgroundFile = null, string brandName = null, bool enabled = null)

Updates the branding of tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateTenantBrandingExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new TenantBrandingApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var logoFile = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream |  (optional) 
            var backgroundFile = new System.IO.MemoryStream(System.IO.File.ReadAllBytes("/path/to/file.txt"));  // System.IO.Stream |  (optional) 
            var brandName = "brandName_example";  // string |  (optional) 
            var enabled = true;  // bool |  (optional) 

            try
            {
                // Updates the branding of tenant
                TenantApiTenantV1TenantUpdatedResponse result = apiInstance.UpdateTenantBranding(tenantId, logoFile, backgroundFile, brandName, enabled);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling TenantBrandingApi.UpdateTenantBranding: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateTenantBrandingWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates the branding of tenant
    ApiResponse<TenantApiTenantV1TenantUpdatedResponse> response = apiInstance.UpdateTenantBrandingWithHttpInfo(tenantId, logoFile, backgroundFile, brandName, enabled);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling TenantBrandingApi.UpdateTenantBrandingWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **logoFile** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **backgroundFile** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **brandName** | **string** |  | [optional]  |
| **enabled** | **bool** |  | [optional]  |

### Return type

[**TenantApiTenantV1TenantUpdatedResponse**](TenantApiTenantV1TenantUpdatedResponse.md)

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
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

