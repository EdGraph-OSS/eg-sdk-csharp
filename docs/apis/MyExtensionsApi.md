# EdGraph.Platform.Client.Api.MyExtensionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**RemoveUserExtension**](MyExtensionsApi.md#removeuserextension) | **DELETE** /me/extensions/{code} | Removes a user&#39;s profile extension. |
| [**SetUserExtension**](MyExtensionsApi.md#setuserextension) | **POST** /me/extensions | Creates or update a user&#39;s profile extension. |

<a id="removeuserextension"></a>
# **RemoveUserExtension**
> IdentityApiUserV1UserExtensionRemovedResponse RemoveUserExtension (string code)

Removes a user's profile extension.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** |  |  |

### Return type

[**IdentityApiUserV1UserExtensionRemovedResponse**](IdentityApiUserV1UserExtensionRemovedResponse.md)

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

<a id="setuserextension"></a>
# **SetUserExtension**
> IdentityApiUserV1UserExtensionSetResponse SetUserExtension (IdentityApiUserV1SetUserExtensionRequest identityApiUserV1SetUserExtensionRequest = null)

Creates or update a user's profile extension.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **identityApiUserV1SetUserExtensionRequest** | [**IdentityApiUserV1SetUserExtensionRequest**](IdentityApiUserV1SetUserExtensionRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1UserExtensionSetResponse**](IdentityApiUserV1UserExtensionSetResponse.md)

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

