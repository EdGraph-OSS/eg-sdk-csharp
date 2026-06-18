# EdGraph.Platform.Client.Api.UsersEducationOrganizationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUserEducationOrganization**](UsersEducationOrganizationsApi.md#addusereducationorganization) | **POST** /tenants/{tenantId}/users/{userId}/educationorganizations | Adds an Education Organization to a user. |
| [**GetUserEducationOrganizations**](UsersEducationOrganizationsApi.md#getusereducationorganizations) | **GET** /tenants/{tenantId}/users/{userId}/educationorganizations | Gets the Education Organizations of a user. |
| [**RemoveUserEducationOrganization**](UsersEducationOrganizationsApi.md#removeusereducationorganization) | **DELETE** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Removes an Education Organization from a user. |
| [**UpdateUserEducationOrganization**](UsersEducationOrganizationsApi.md#updateusereducationorganization) | **PUT** /tenants/{tenantId}/users/{userId}/educationorganizations/{educationOrganizationId} | Updates the Education Organization of a user. |

<a id="addusereducationorganization"></a>
# **AddUserEducationOrganization**
> IdentityApiUserV1EducationOrganizationAddedResponse AddUserEducationOrganization (Guid tenantId, Guid userId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest = null)

Adds an Education Organization to a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsAddEducationOrganizationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1EducationOrganizationAddedResponse**](IdentityApiUserV1EducationOrganizationAddedResponse.md)

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

<a id="getusereducationorganizations"></a>
# **GetUserEducationOrganizations**
> IdentityApiUserV1EducationOrganizationPaginatedItemsResponse GetUserEducationOrganizations (Guid tenantId, Guid userId)

Gets the Education Organizations of a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |

### Return type

[**IdentityApiUserV1EducationOrganizationPaginatedItemsResponse**](IdentityApiUserV1EducationOrganizationPaginatedItemsResponse.md)

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

<a id="removeusereducationorganization"></a>
# **RemoveUserEducationOrganization**
> IdentityApiUserV1EducationOrganizationRemovedResponse RemoveUserEducationOrganization (Guid tenantId, Guid userId, int educationOrganizationId)

Removes an Education Organization from a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **educationOrganizationId** | **int** |  |  |

### Return type

[**IdentityApiUserV1EducationOrganizationRemovedResponse**](IdentityApiUserV1EducationOrganizationRemovedResponse.md)

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

<a id="updateusereducationorganization"></a>
# **UpdateUserEducationOrganization**
> IdentityApiUserV1EducationOrganizationUpdatedResponse UpdateUserEducationOrganization (Guid tenantId, Guid userId, int educationOrganizationId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest = null)

Updates the Education Organization of a user.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **educationOrganizationId** | **int** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEducationOrganizationsUpdateEducationOrganizationRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1EducationOrganizationUpdatedResponse**](IdentityApiUserV1EducationOrganizationUpdatedResponse.md)

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

