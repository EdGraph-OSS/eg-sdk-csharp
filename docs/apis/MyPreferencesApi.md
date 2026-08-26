# EdGraph.Platform.Client.Api.MyPreferencesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetUserPreferences**](MyPreferencesApi.md#getuserpreferences) | **GET** /me/preferences | Retrieves the user&#39;s preferences.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged. |
| [**Preference**](MyPreferencesApi.md#preference) | **GET** /me/preferences/{code} | Retrieves a user&#39;s preference by code.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings/{code}&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged. |
| [**UpdateUserPreferenceAsync**](MyPreferencesApi.md#updateuserpreferenceasync) | **POST** /me/preferences | Creates or update a user&#39;s preference.  &lt;br&gt;&lt;b&gt;Deprecated.&lt;/b&gt; Use &#x60;/me/settings&#x60; instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged. |

<a id="getuserpreferences"></a>
# **GetUserPreferences**
> IdentityApiUserV1GetUserPreferencesResponse GetUserPreferences (int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves the user's preferences.  <br><b>Deprecated.</b> Use `/me/settings` instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional]  |
| **filter** | **string** |  | [optional]  |

### Return type

[**IdentityApiUserV1GetUserPreferencesResponse**](IdentityApiUserV1GetUserPreferencesResponse.md)

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

<a id="preference"></a>
# **Preference**
> EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse Preference (string code)

Retrieves a user's preference by code.  <br><b>Deprecated.</b> Use `/me/settings/{code}` instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **code** | **string** |  |  |

### Return type

[**EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1ViewModelsResponsesUserCacheResponse.md)

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

<a id="updateuserpreferenceasync"></a>
# **UpdateUserPreferenceAsync**
> IdentityApiUserV1UserPreferenceUpdatedResponse UpdateUserPreferenceAsync (EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest = null)

Creates or update a user's preference.  <br><b>Deprecated.</b> Use `/me/settings` instead. Superseded by  EdGraph.Services.Settings; see docs/settings-deprecation-map.md. This endpoint  still works and is unchanged.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateUserPreferenceRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1UserPreferenceUpdatedResponse**](IdentityApiUserV1UserPreferenceUpdatedResponse.md)

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

