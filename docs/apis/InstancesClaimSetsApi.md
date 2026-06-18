# EdGraph.Platform.Client.Api.InstancesClaimSetsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateClaimSetAsync**](InstancesClaimSetsApi.md#createclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Creates a ClaimSet. |
| [**DeleteClaimSetAsync**](InstancesClaimSetsApi.md#deleteclaimsetasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Deletes a ClaimSet. |
| [**GetClaimSetByIdAsync**](InstancesClaimSetsApi.md#getclaimsetbyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Retrieves a ClaimSet by ID. |
| [**GetClaimSetsAsync**](InstancesClaimSetsApi.md#getclaimsetsasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets | Retrieves a list of ClaimSets. |
| [**GetResourceClaimsGridAsync**](InstancesClaimSetsApi.md#getresourceclaimsgridasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/resourceclaims | Retrieves a grid of Resource Claims. |
| [**SyncClaimSetAsync**](InstancesClaimSetsApi.md#syncclaimsetasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId}/sync | Copies a Claim Set from one instance to another/other instance(s) |
| [**UpdateClaimSetAsync**](InstancesClaimSetsApi.md#updateclaimsetasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/claimsets/{claimSetId} | Updates a ClaimSet. |

<a id="createclaimsetasync"></a>
# **CreateClaimSetAsync**
> EdfiAdminApiEdfiAdminV1SaveClaimSetResponse CreateClaimSetAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1SaveClaimSetRequest edfiAdminApiEdfiAdminV1SaveClaimSetRequest = null)

Creates a ClaimSet.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1SaveClaimSetRequest** | [**EdfiAdminApiEdfiAdminV1SaveClaimSetRequest**](EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SaveClaimSetResponse**](EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteclaimsetasync"></a>
# **DeleteClaimSetAsync**
> void DeleteClaimSetAsync (string tenantId, string instanceId, int claimSetId)

Deletes a ClaimSet.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getclaimsetbyidasync"></a>
# **GetClaimSetByIdAsync**
> EdfiAdminApiEdfiAdminV1ClaimSet GetClaimSetByIdAsync (string tenantId, string instanceId, int claimSetId)

Retrieves a ClaimSet by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1ClaimSet**](EdfiAdminApiEdfiAdminV1ClaimSet.md)

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

<a id="getclaimsetsasync"></a>
# **GetClaimSetsAsync**
> EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel GetClaimSetsAsync (string tenantId, string instanceId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of ClaimSets.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1ClaimSetPaginatedItemsViewModel.md)

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

<a id="getresourceclaimsgridasync"></a>
# **GetResourceClaimsGridAsync**
> EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse GetResourceClaimsGridAsync (string tenantId, string instanceId, int claimSetId)

Retrieves a grid of Resource Claims.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse**](EdfiAdminApiEdfiAdminV1GetResourceClaimsGridResponse.md)

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

<a id="syncclaimsetasync"></a>
# **SyncClaimSetAsync**
> void SyncClaimSetAsync (string tenantId, string instanceId, int claimSetId, EdfiAdminApiEdfiAdminV1SyncClaimSetRequest edfiAdminApiEdfiAdminV1SyncClaimSetRequest = null)

Copies a Claim Set from one instance to another/other instance(s)


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SyncClaimSetRequest** | [**EdfiAdminApiEdfiAdminV1SyncClaimSetRequest**](EdfiAdminApiEdfiAdminV1SyncClaimSetRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateclaimsetasync"></a>
# **UpdateClaimSetAsync**
> EdfiAdminApiEdfiAdminV1SaveClaimSetResponse UpdateClaimSetAsync (string tenantId, string instanceId, int claimSetId, EdfiAdminApiEdfiAdminV1SaveClaimSetRequest edfiAdminApiEdfiAdminV1SaveClaimSetRequest = null)

Updates a ClaimSet.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **claimSetId** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1SaveClaimSetRequest** | [**EdfiAdminApiEdfiAdminV1SaveClaimSetRequest**](EdfiAdminApiEdfiAdminV1SaveClaimSetRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1SaveClaimSetResponse**](EdfiAdminApiEdfiAdminV1SaveClaimSetResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

