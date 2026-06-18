# EdGraph.Platform.Client.Api.InvitationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteTenantInvitationAsync**](InvitationsApi.md#deletetenantinvitationasync) | **DELETE** /tenants/{tenantId}/invitations/{invitationId} | Deletes an invitation |
| [**GetAllTenantInvitationsAsync**](InvitationsApi.md#getalltenantinvitationsasync) | **GET** /tenants/{tenantId}/invitations | Retrieves a list of invitations associated to this tenant |
| [**GetTenantInvitationByIdAsync**](InvitationsApi.md#gettenantinvitationbyidasync) | **GET** /tenants/{tenantId}/invitations/{invitationId} | Retrieves a specific invitation |
| [**SendTenantInvitationAsync**](InvitationsApi.md#sendtenantinvitationasync) | **POST** /tenants/{tenantId}/invitations | Creates and sends an invitation to a user |

<a id="deletetenantinvitationasync"></a>
# **DeleteTenantInvitationAsync**
> void DeleteTenantInvitationAsync (string tenantId, string invitationId)

Deletes an invitation


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **invitationId** | **string** |  |  |

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

<a id="getalltenantinvitationsasync"></a>
# **GetAllTenantInvitationsAsync**
> IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel GetAllTenantInvitationsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of invitations associated to this tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel**](IdentityApiInvitationV1InvitationListResponsePaginatedItemsViewModel.md)

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

<a id="gettenantinvitationbyidasync"></a>
# **GetTenantInvitationByIdAsync**
> IdentityApiInvitationV1InvitationResponse GetTenantInvitationByIdAsync (string tenantId, string invitationId)

Retrieves a specific invitation


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **invitationId** | **string** |  |  |

### Return type

[**IdentityApiInvitationV1InvitationResponse**](IdentityApiInvitationV1InvitationResponse.md)

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

<a id="sendtenantinvitationasync"></a>
# **SendTenantInvitationAsync**
> IdentityApiInvitationV1InvitationSentResponse SendTenantInvitationAsync (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest = null)

Creates and sends an invitation to a user


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsSendInvitationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiInvitationV1InvitationSentResponse**](IdentityApiInvitationV1InvitationSentResponse.md)

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

