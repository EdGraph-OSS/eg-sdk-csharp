# EdGraph.Platform.Client.Api.GroupsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUsersToGroupAsync**](GroupsApi.md#adduserstogroupasync) | **POST** /tenants/{tenantId}/analytics/groups/{groupId}/users/bulk | Adds users to group. |
| [**CreateAnalyticsPowerBiGroup**](GroupsApi.md#createanalyticspowerbigroup) | **POST** /tenants/{tenantId}/analytics/groups | Creates a group. |
| [**DeleteAnalyticsPowerBiGroup**](GroupsApi.md#deleteanalyticspowerbigroup) | **DELETE** /tenants/{tenantId}/analytics/groups/{groupId} | Deletes a group. |
| [**GetAnalyticsPowerBiGroupUsers**](GroupsApi.md#getanalyticspowerbigroupusers) | **GET** /tenants/{tenantId}/analytics/groups/{groupId}/users | Retrieves all users for a specific group. |
| [**GetGroupsAsync**](GroupsApi.md#getgroupsasync) | **GET** /tenants/{tenantId}/analytics/groups | Retrieves a list of groups. |

<a id="adduserstogroupasync"></a>
# **AddUsersToGroupAsync**
> void AddUsersToGroupAsync (string tenantId, string groupId, AnalyticsApiGroupsV1AddGroupUsersRequest analyticsApiGroupsV1AddGroupUsersRequest = null)

Adds users to group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **groupId** | **string** |  |  |
| **analyticsApiGroupsV1AddGroupUsersRequest** | [**AnalyticsApiGroupsV1AddGroupUsersRequest**](AnalyticsApiGroupsV1AddGroupUsersRequest.md) |  | [optional]  |

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createanalyticspowerbigroup"></a>
# **CreateAnalyticsPowerBiGroup**
> AnalyticsApiGroupsV1GroupResponse CreateAnalyticsPowerBiGroup (string tenantId, AnalyticsApiGroupsV1CreateGroupRequest analyticsApiGroupsV1CreateGroupRequest = null)

Creates a group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiGroupsV1CreateGroupRequest** | [**AnalyticsApiGroupsV1CreateGroupRequest**](AnalyticsApiGroupsV1CreateGroupRequest.md) |  | [optional]  |

### Return type

[**AnalyticsApiGroupsV1GroupResponse**](AnalyticsApiGroupsV1GroupResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteanalyticspowerbigroup"></a>
# **DeleteAnalyticsPowerBiGroup**
> void DeleteAnalyticsPowerBiGroup (string tenantId, string groupId)

Deletes a group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **groupId** | **string** |  |  |

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
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getanalyticspowerbigroupusers"></a>
# **GetAnalyticsPowerBiGroupUsers**
> AnalyticsApiGroupsV1GroupUsersResponse GetAnalyticsPowerBiGroupUsers (string tenantId, string groupId, int skipFirstN = null, int topFirstN = null)

Retrieves all users for a specific group.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **groupId** | **string** |  |  |
| **skipFirstN** | **int** |  | [optional]  |
| **topFirstN** | **int** |  | [optional]  |

### Return type

[**AnalyticsApiGroupsV1GroupUsersResponse**](AnalyticsApiGroupsV1GroupUsersResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getgroupsasync"></a>
# **GetGroupsAsync**
> AnalyticsApiGroupsV1GroupsResponse GetGroupsAsync (string tenantId, string filter = null)

Retrieves a list of groups.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **filter** | **string** |  | [optional]  |

### Return type

[**AnalyticsApiGroupsV1GroupsResponse**](AnalyticsApiGroupsV1GroupsResponse.md)

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

