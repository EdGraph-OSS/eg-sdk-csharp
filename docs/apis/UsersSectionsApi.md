# EdGraph.Platform.Client.Api.UsersSectionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUserSection**](UsersSectionsApi.md#addusersection) | **POST** /tenants/{tenantId}/users/{userId}/sections | Adds a Section to a user. |
| [**AddUserSectionBulk**](UsersSectionsApi.md#addusersectionbulk) | **POST** /tenants/{tenantId}/users/{userId}/sections/bulk | Adds Sections to a user in bulk. |
| [**GetUserSections**](UsersSectionsApi.md#getusersections) | **GET** /tenants/{tenantId}/users/{userId}/sections | Gets the Sections of a user. |
| [**RemoveUserSection**](UsersSectionsApi.md#removeusersection) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Removes a Section from a user. |
| [**RemoveUserSectionBulk**](UsersSectionsApi.md#removeusersectionbulk) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/bulk | Removes Sections from a user in bulk. |
| [**UpdateUserSection**](UsersSectionsApi.md#updateusersection) | **PUT** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Updates the Section of a user. |
| [**UpdateUserSectionBulk**](UsersSectionsApi.md#updateusersectionbulk) | **PUT** /tenants/{tenantId}/users/{userId}/sections/bulk | Updates the Section of a user in bulk. |

<a id="addusersection"></a>
# **AddUserSection**
> IdentityApiUserV1SectionAddedResponse AddUserSection (Guid tenantId, Guid userId, IdentityApiUserV1AddSectionRequest identityApiUserV1AddSectionRequest = null)

Adds a Section to a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1AddSectionRequest** | [**IdentityApiUserV1AddSectionRequest**](IdentityApiUserV1AddSectionRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionAddedResponse**](IdentityApiUserV1SectionAddedResponse.md)

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

<a id="addusersectionbulk"></a>
# **AddUserSectionBulk**
> IdentityApiUserV1SectionAddedBulkResponse AddUserSectionBulk (Guid tenantId, Guid userId, IdentityApiUserV1AddSectionBulkRequest identityApiUserV1AddSectionBulkRequest = null)

Adds Sections to a user in bulk.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1AddSectionBulkRequest** | [**IdentityApiUserV1AddSectionBulkRequest**](IdentityApiUserV1AddSectionBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionAddedBulkResponse**](IdentityApiUserV1SectionAddedBulkResponse.md)

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

<a id="getusersections"></a>
# **GetUserSections**
> IdentityApiUserV1GetSectionsResponse GetUserSections (Guid tenantId, Guid userId)

Gets the Sections of a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |

### Return type

[**IdentityApiUserV1GetSectionsResponse**](IdentityApiUserV1GetSectionsResponse.md)

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

<a id="removeusersection"></a>
# **RemoveUserSection**
> IdentityApiUserV1SectionRemovedResponse RemoveUserSection (Guid tenantId, Guid userId, Guid userSectionId)

Removes a Section from a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **userSectionId** | **Guid** |  |  |

### Return type

[**IdentityApiUserV1SectionRemovedResponse**](IdentityApiUserV1SectionRemovedResponse.md)

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

<a id="removeusersectionbulk"></a>
# **RemoveUserSectionBulk**
> IdentityApiUserV1SectionRemovedBulkResponse RemoveUserSectionBulk (Guid tenantId, Guid userId, IdentityApiUserV1RemoveSectionBulkRequest identityApiUserV1RemoveSectionBulkRequest = null)

Removes Sections from a user in bulk.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1RemoveSectionBulkRequest** | [**IdentityApiUserV1RemoveSectionBulkRequest**](IdentityApiUserV1RemoveSectionBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionRemovedBulkResponse**](IdentityApiUserV1SectionRemovedBulkResponse.md)

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

<a id="updateusersection"></a>
# **UpdateUserSection**
> IdentityApiUserV1SectionUpdatedResponse UpdateUserSection (Guid tenantId, Guid userId, Guid userSectionId, IdentityApiUserV1UpdateSectionRequest identityApiUserV1UpdateSectionRequest = null)

Updates the Section of a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **userSectionId** | **Guid** |  |  |
| **identityApiUserV1UpdateSectionRequest** | [**IdentityApiUserV1UpdateSectionRequest**](IdentityApiUserV1UpdateSectionRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionUpdatedResponse**](IdentityApiUserV1SectionUpdatedResponse.md)

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

<a id="updateusersectionbulk"></a>
# **UpdateUserSectionBulk**
> IdentityApiUserV1SectionUpdatedBulkResponse UpdateUserSectionBulk (Guid tenantId, Guid userId, IdentityApiUserV1UpdateSectionBulkRequest identityApiUserV1UpdateSectionBulkRequest = null)

Updates the Section of a user in bulk.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1UpdateSectionBulkRequest** | [**IdentityApiUserV1UpdateSectionBulkRequest**](IdentityApiUserV1UpdateSectionBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionUpdatedBulkResponse**](IdentityApiUserV1SectionUpdatedBulkResponse.md)

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

