# EdGraph.Platform.Client.Api.MySettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateMySetting**](MySettingsApi.md#createmysetting) | **POST** /me/settings | Create a User-scope setting |
| [**DeleteMySetting**](MySettingsApi.md#deletemysetting) | **DELETE** /me/settings/{settingIdOrCode} | Delete the User-scope setting for a key, addressed by SettingType id or Code |
| [**GetMySetting**](MySettingsApi.md#getmysetting) | **GET** /me/settings/{settingIdOrCode} | Get a User-scope setting |
| [**SearchMySettings**](MySettingsApi.md#searchmysettings) | **GET** /me/settings | List User-scope settings |
| [**SetMySetting**](MySettingsApi.md#setmysetting) | **PUT** /me/settings | Create or update (upsert) a User-scope setting, addressed by the SettingTypeId in the body |
| [**UpdateMySetting**](MySettingsApi.md#updatemysetting) | **PUT** /me/settings/{settingIdOrCode} | Update the User-scope setting for a key, addressed by SettingType id or Code |

<a id="createmysetting"></a>
# **CreateMySetting**
> SettingsApiUserSettingsV1CreateUserSettingResponse CreateMySetting (EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody edGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody = null)

Create a User-scope setting


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody** | [**EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1CreateMySettingRequestBody.md) |  | [optional]  |

### Return type

[**SettingsApiUserSettingsV1CreateUserSettingResponse**](SettingsApiUserSettingsV1CreateUserSettingResponse.md)

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
| **201** | Created |  -  |
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletemysetting"></a>
# **DeleteMySetting**
> void DeleteMySetting (string settingIdOrCode, EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody edGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody = null)

Delete the User-scope setting for a key, addressed by SettingType id or Code


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **settingIdOrCode** | **string** |  |  |
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody** | [**EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1DeleteMySettingRequestBody.md) |  | [optional]  |

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
| **204** | No Content |  -  |
| **404** | Not Found |  -  |
| **422** | Client Error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getmysetting"></a>
# **GetMySetting**
> SettingsApiUserSettingsV1UserSettingMessage GetMySetting (string settingIdOrCode, Guid settingTypeId = null, string provider = null, Guid applicationId = null, bool resolveEffectiveValue = null)

Get a User-scope setting

Answers with the stored record alone. Effective-value resolution is opt-in: pass  `resolveEffectiveValue=true` to instead receive the value in force at this scope — every  layer above it merged under the setting's own value.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **settingIdOrCode** | **string** |  |  |
| **settingTypeId** | **Guid** |  | [optional]  |
| **provider** | **string** |  | [optional]  |
| **applicationId** | **Guid** |  | [optional]  |
| **resolveEffectiveValue** | **bool** |  | [optional] [default to false] |

### Return type

[**SettingsApiUserSettingsV1UserSettingMessage**](SettingsApiUserSettingsV1UserSettingMessage.md)

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
| **200** | Success |  -  |
| **404** | Not Found |  -  |
| **422** | Client Error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchmysettings"></a>
# **SearchMySettings**
> SettingsApiUserSettingsV1SearchUserSettingsResponse SearchMySettings (Guid applicationId = null, Guid settingTypeId = null, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

List User-scope settings


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **applicationId** | **Guid** |  | [optional]  |
| **settingTypeId** | **Guid** |  | [optional]  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**SettingsApiUserSettingsV1SearchUserSettingsResponse**](SettingsApiUserSettingsV1SearchUserSettingsResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setmysetting"></a>
# **SetMySetting**
> SettingsApiUserSettingsV1SetUserSettingResponse SetMySetting (EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody edGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody = null)

Create or update (upsert) a User-scope setting, addressed by the SettingTypeId in the body


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody** | [**EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1SetMySettingRequestBody.md) |  | [optional]  |

### Return type

[**SettingsApiUserSettingsV1SetUserSettingResponse**](SettingsApiUserSettingsV1SetUserSettingResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatemysetting"></a>
# **UpdateMySetting**
> void UpdateMySetting (string settingIdOrCode, EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody edGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody = null)

Update the User-scope setting for a key, addressed by SettingType id or Code


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **settingIdOrCode** | **string** |  |  |
| **edGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody** | [**EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody**](EdGraphPlatformHttpAggregatorsTenantApiControllersV1UpdateMySettingRequestBody.md) |  | [optional]  |

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
| **204** | No Content |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **422** | Client Error |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

