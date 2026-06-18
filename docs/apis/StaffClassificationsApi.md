# EdGraph.Platform.Client.Api.StaffClassificationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateStaffClassification**](StaffClassificationsApi.md#createstaffclassification) | **POST** /tenants/{tenantId}/staffclassifications | Creates a StaffClassification. |
| [**DeleteStaffClassification**](StaffClassificationsApi.md#deletestaffclassification) | **DELETE** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Deletes a StaffClassification. |
| [**GetStaffClassificationById**](StaffClassificationsApi.md#getstaffclassificationbyid) | **GET** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Retrieves a StaffClassification by ID. |
| [**GetStaffClassifications**](StaffClassificationsApi.md#getstaffclassifications) | **GET** /tenants/{tenantId}/staffclassifications | Retrieves a list of StaffClassifications. |
| [**GetStaffClassificationsNamespaces**](StaffClassificationsApi.md#getstaffclassificationsnamespaces) | **GET** /tenants/{tenantId}/staffclassifications/namespaces | Retrieves a list of unique Staff Classification Namespaces. |
| [**UpdateStaffClassification**](StaffClassificationsApi.md#updatestaffclassification) | **PUT** /tenants/{tenantId}/staffclassifications/{staffClassificationId} | Updates a StaffClassification. |

<a id="createstaffclassification"></a>
# **CreateStaffClassification**
> IdentityApiStaffClassificationV1StaffClassificationCreatedResponse CreateStaffClassification (Guid tenantId, IdentityApiStaffClassificationV1CreateStaffClassificationRequest identityApiStaffClassificationV1CreateStaffClassificationRequest = null)

Creates a StaffClassification.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **identityApiStaffClassificationV1CreateStaffClassificationRequest** | [**IdentityApiStaffClassificationV1CreateStaffClassificationRequest**](IdentityApiStaffClassificationV1CreateStaffClassificationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationCreatedResponse**](IdentityApiStaffClassificationV1StaffClassificationCreatedResponse.md)

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

<a id="deletestaffclassification"></a>
# **DeleteStaffClassification**
> IdentityApiStaffClassificationV1StaffClassificationDeletedResponse DeleteStaffClassification (Guid tenantId, Guid staffClassificationId)

Deletes a StaffClassification.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **staffClassificationId** | **Guid** |  |  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationDeletedResponse**](IdentityApiStaffClassificationV1StaffClassificationDeletedResponse.md)

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

<a id="getstaffclassificationbyid"></a>
# **GetStaffClassificationById**
> IdentityApiStaffClassificationV1StaffClassificationResponse GetStaffClassificationById (Guid tenantId, Guid staffClassificationId)

Retrieves a StaffClassification by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **staffClassificationId** | **Guid** |  |  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationResponse**](IdentityApiStaffClassificationV1StaffClassificationResponse.md)

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

<a id="getstaffclassifications"></a>
# **GetStaffClassifications**
> IdentityApiStaffClassificationV1GetStaffClassificationsResponse GetStaffClassifications (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of StaffClassifications.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiStaffClassificationV1GetStaffClassificationsResponse**](IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)

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

<a id="getstaffclassificationsnamespaces"></a>
# **GetStaffClassificationsNamespaces**
> IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse GetStaffClassificationsNamespaces (Guid tenantId, int pageIndex = null, int pageSize = null, string filter = null)

Retrieves a list of unique Staff Classification Namespaces.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse**](IdentityApiStaffClassificationV1GetStaffClassificationsNamespacesResponse.md)

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

<a id="updatestaffclassification"></a>
# **UpdateStaffClassification**
> IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse UpdateStaffClassification (Guid tenantId, Guid staffClassificationId, IdentityApiStaffClassificationV1UpdateStaffClassificationRequest identityApiStaffClassificationV1UpdateStaffClassificationRequest = null)

Updates a StaffClassification.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **staffClassificationId** | **Guid** |  |  |
| **identityApiStaffClassificationV1UpdateStaffClassificationRequest** | [**IdentityApiStaffClassificationV1UpdateStaffClassificationRequest**](IdentityApiStaffClassificationV1UpdateStaffClassificationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse**](IdentityApiStaffClassificationV1StaffClassificationUpdatedResponse.md)

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

