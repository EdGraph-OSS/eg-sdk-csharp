# EdGraph.Platform.Client.Api.UsersLicensesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AssignLicenseTenantUserAsync**](UsersLicensesApi.md#assignlicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assign | Assigns a license to a user in the context of a specific tenant |
| [**AssignLicenseTenantUserBulkAsync**](UsersLicensesApi.md#assignlicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/assignbulk | Assigns one or more licenses to a user in the context of a specific tenant |
| [**GetAllTenantUserApplicationLicensesAsync**](UsersLicensesApi.md#getalltenantuserapplicationlicensesasync) | **GET** /tenants/{tenantId}/users/{userId}/licenses | Retrieves a list of user licenses in the context of a specific tenant |
| [**RevokeLicenseTenantUserAsync**](UsersLicensesApi.md#revokelicensetenantuserasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revoke | Revokes a license from a user in the context of a specific tenant |
| [**RevokeLicenseTenantUserBulkAsync**](UsersLicensesApi.md#revokelicensetenantuserbulkasync) | **PUT** /tenants/{tenantId}/users/{userId}/licenses/revokebulk | Revokes one or more licenses from a user in the context of a specific tenant |

<a id="assignlicensetenantuserasync"></a>
# **AssignLicenseTenantUserAsync**
> IdentityApiUserV1LicenseAssignedResponse AssignLicenseTenantUserAsync (string tenantId, string userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest = null)

Assigns a license to a user in the context of a specific tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseAssignedResponse**](IdentityApiUserV1LicenseAssignedResponse.md)

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

<a id="assignlicensetenantuserbulkasync"></a>
# **AssignLicenseTenantUserBulkAsync**
> IdentityApiUserV1LicenseAssignedBulkResponse AssignLicenseTenantUserBulkAsync (string tenantId, string userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest = null)

Assigns one or more licenses to a user in the context of a specific tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesAssignLicenseBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseAssignedBulkResponse**](IdentityApiUserV1LicenseAssignedBulkResponse.md)

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

<a id="getalltenantuserapplicationlicensesasync"></a>
# **GetAllTenantUserApplicationLicensesAsync**
> EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel GetAllTenantUserApplicationLicensesAsync (string tenantId, string userId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of user licenses in the context of a specific tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserLicensePaginatedItemsViewModel.md)

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

<a id="revokelicensetenantuserasync"></a>
# **RevokeLicenseTenantUserAsync**
> IdentityApiUserV1LicenseRevokedResponse RevokeLicenseTenantUserAsync (string tenantId, string userId, IdentityApiUserV1RevokeLicenseRequest identityApiUserV1RevokeLicenseRequest = null)

Revokes a license from a user in the context of a specific tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **identityApiUserV1RevokeLicenseRequest** | [**IdentityApiUserV1RevokeLicenseRequest**](IdentityApiUserV1RevokeLicenseRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseRevokedResponse**](IdentityApiUserV1LicenseRevokedResponse.md)

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

<a id="revokelicensetenantuserbulkasync"></a>
# **RevokeLicenseTenantUserBulkAsync**
> IdentityApiUserV1LicenseRevokedBulkResponse RevokeLicenseTenantUserBulkAsync (string tenantId, string userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest = null)

Revokes one or more licenses from a user in the context of a specific tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **userId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsLicensesRevokeLicenseBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1LicenseRevokedBulkResponse**](IdentityApiUserV1LicenseRevokedBulkResponse.md)

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

