# EdGraph.Platform.Client.Api.TenantBrandingApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**UpdateTenantBranding**](TenantBrandingApi.md#updatetenantbranding) | **PUT** /tenants/{tenantId}/branding | Updates the branding of tenant |

<a id="updatetenantbranding"></a>
# **UpdateTenantBranding**
> TenantApiTenantV1TenantUpdatedResponse UpdateTenantBranding (Guid tenantId, System.IO.Stream logoFile = null, System.IO.Stream backgroundFile = null, string brandName = null, bool enabled = null, bool removeBackground = null, bool removeLogo = null)

Updates the branding of tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **logoFile** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **backgroundFile** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **brandName** | **string** |  | [optional]  |
| **enabled** | **bool** |  | [optional]  |
| **removeBackground** | **bool** |  | [optional]  |
| **removeLogo** | **bool** |  | [optional]  |

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

