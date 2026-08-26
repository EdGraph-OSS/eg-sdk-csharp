# EdGraph.Platform.Client.Api.ClientBrandingApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetClientBrandingAsync**](ClientBrandingApi.md#getclientbrandingasync) | **GET** /clients/{clientId}/branding | Public (unauthenticated) read of a client&#39;s branding for the sign-in and other pre-auth  surfaces (Azure DevOps #17086). Returns only render fields + the override flag — never secrets,  storage internals, or other client configuration. |

<a id="getclientbrandingasync"></a>
# **GetClientBrandingAsync**
> EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse GetClientBrandingAsync (string clientId)

Public (unauthenticated) read of a client's branding for the sign-in and other pre-auth  surfaces (Azure DevOps #17086). Returns only render fields + the override flag — never secrets,  storage internals, or other client configuration.

Unauthenticated by design (branding is shown before login). An unknown client returns a  disabled default rather than 404, so the endpoint cannot be used as a client-existence oracle.  The response is cacheable so downstream CDNs/browsers absorb most traffic; rate limiting is  expected at the gateway.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **clientId** | **string** | The OAuth client id (already URL-decoded by routing). |  |

### Return type

[**EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesClientBrandingResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **500** | An unhandled error occurred on the server. See the response body for details. |  -  |
| **200** | The client&#39;s branding (or a disabled default for an unknown client). |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

