# EdGraph.Platform.Client.Api.MyTenantsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetUserTenants**](MyTenantsApi.md#getusertenants) | **GET** /me/tenants | Retrieves the Tenants of the User that is currently logged in. |
| [**SearchMyLicenses**](MyTenantsApi.md#searchmylicenses) | **GET** /v2/me/tenants/{tenantId}/licenses | Search the user&#39;s licenses. |
| [**SearchMyTenants**](MyTenantsApi.md#searchmytenants) | **GET** /v2/me/tenants | Searches tenants associated to the user. |

<a id="getusertenants"></a>
# **GetUserTenants**
> IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel GetUserTenants (int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves the Tenants of the User that is currently logged in.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel**](IdentityApiUserV1UserTenantProfilePaginatedItemsViewModel.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchmylicenses"></a>
# **SearchMyLicenses**
> IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel SearchMyLicenses (Guid tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Search the user's licenses.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel**](IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchmytenants"></a>
# **SearchMyTenants**
> IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel SearchMyTenants (int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Searches tenants associated to the user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel**](IdentityApiUserV2UserMeTenantsResponsePaginatedItemsViewModel.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

