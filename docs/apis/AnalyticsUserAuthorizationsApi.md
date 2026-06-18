# EdGraph.Platform.Client.Api.AnalyticsUserAuthorizationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetPaginatedUserAuthorizations**](AnalyticsUserAuthorizationsApi.md#getpaginateduserauthorizations) | **GET** /tenants/{tenantId}/analytics/userauthorizations | Retrieves paginated user authorizations |
| [**SoftDeleteUserAuthorization**](AnalyticsUserAuthorizationsApi.md#softdeleteuserauthorization) | **DELETE** /tenants/{tenantId}/analytics/userauthorizations/{userAuthorizationId} | Soft Deletes a user authorization by Id |

<a id="getpaginateduserauthorizations"></a>
# **GetPaginatedUserAuthorizations**
> AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse GetPaginatedUserAuthorizations (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves paginated user authorizations


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse**](AnalyticsApiUserAuthorizationsV1UserAuthorizationsPaginatedItemsResponse.md)

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

<a id="softdeleteuserauthorization"></a>
# **SoftDeleteUserAuthorization**
> AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse SoftDeleteUserAuthorization (string tenantId, string userAuthorizationId)

Soft Deletes a user authorization by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userAuthorizationId** | **string** |  |  |

### Return type

[**AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse**](AnalyticsApiUserAuthorizationsV1UserAuthorizationSoftDeletedResponse.md)

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

