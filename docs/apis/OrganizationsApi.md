# EdGraph.Platform.Client.Api.OrganizationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOrganizationAsync**](OrganizationsApi.md#createorganizationasync) | **POST** /tenants/{tenantId}/organizations | Creates an Organization. |
| [**DeleteOrganizationAsync**](OrganizationsApi.md#deleteorganizationasync) | **DELETE** /tenants/{tenantId}/organizations/{organizationIdentifier} | Deletes an Organization. |
| [**GetOrganizationByIdAsync**](OrganizationsApi.md#getorganizationbyidasync) | **GET** /tenants/{tenantId}/organizations/{organizationIdentifier} | Retrieves an Organization by ID. |
| [**GetOrganizationsAsync**](OrganizationsApi.md#getorganizationsasync) | **GET** /tenants/{tenantId}/organizations | Retrieves a list of Organizations. |
| [**UpdateOrganizationAsync**](OrganizationsApi.md#updateorganizationasync) | **PUT** /tenants/{tenantId}/organizations/{organizationIdentifier} | Updates an Organization. |

<a id="createorganizationasync"></a>
# **CreateOrganizationAsync**
> TenantApiTenantV1OrganizationCreatedResponse CreateOrganizationAsync (string tenantId, TenantApiTenantV1CreateOrganizationRequest tenantApiTenantV1CreateOrganizationRequest = null)

Creates an Organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **tenantApiTenantV1CreateOrganizationRequest** | [**TenantApiTenantV1CreateOrganizationRequest**](TenantApiTenantV1CreateOrganizationRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1OrganizationCreatedResponse**](TenantApiTenantV1OrganizationCreatedResponse.md)

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

<a id="deleteorganizationasync"></a>
# **DeleteOrganizationAsync**
> TenantApiTenantV1OrganizationDeletedResponse DeleteOrganizationAsync (string tenantId, string organizationIdentifier)

Deletes an Organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **organizationIdentifier** | **string** |  |  |

### Return type

[**TenantApiTenantV1OrganizationDeletedResponse**](TenantApiTenantV1OrganizationDeletedResponse.md)

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

<a id="getorganizationbyidasync"></a>
# **GetOrganizationByIdAsync**
> TenantApiTenantV1Organization GetOrganizationByIdAsync (string tenantId, string organizationIdentifier)

Retrieves an Organization by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **organizationIdentifier** | **string** |  |  |

### Return type

[**TenantApiTenantV1Organization**](TenantApiTenantV1Organization.md)

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

<a id="getorganizationsasync"></a>
# **GetOrganizationsAsync**
> TenantApiTenantV1GetOrganizationsPaginatedResponse GetOrganizationsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Organizations.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiTenantV1GetOrganizationsPaginatedResponse**](TenantApiTenantV1GetOrganizationsPaginatedResponse.md)

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

<a id="updateorganizationasync"></a>
# **UpdateOrganizationAsync**
> TenantApiTenantV1OrganizationUpdatedResponse UpdateOrganizationAsync (string tenantId, string organizationIdentifier, TenantApiTenantV1UpdateOrganizationRequest tenantApiTenantV1UpdateOrganizationRequest = null)

Updates an Organization.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **organizationIdentifier** | **string** |  |  |
| **tenantApiTenantV1UpdateOrganizationRequest** | [**TenantApiTenantV1UpdateOrganizationRequest**](TenantApiTenantV1UpdateOrganizationRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1OrganizationUpdatedResponse**](TenantApiTenantV1OrganizationUpdatedResponse.md)

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

