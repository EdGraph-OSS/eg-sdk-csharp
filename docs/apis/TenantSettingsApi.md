# EdGraph.Platform.Client.Api.TenantSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateTenantSetting**](TenantSettingsApi.md#createtenantsetting) | **POST** /v2/tenants/{tenantId}/settings | Create a Tenant-scope setting |
| [**DeleteTenantSetting**](TenantSettingsApi.md#deletetenantsetting) | **DELETE** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Delete the Tenant-scope setting for a key, addressed by SettingType id or Code |
| [**GetTenantSetting**](TenantSettingsApi.md#gettenantsetting) | **GET** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Get a Tenant-scope setting |
| [**SearchTenantSettings**](TenantSettingsApi.md#searchtenantsettings) | **GET** /v2/tenants/{tenantId}/settings | List Tenant-scope settings |
| [**SetTenantSetting**](TenantSettingsApi.md#settenantsetting) | **PUT** /v2/tenants/{tenantId}/settings | Create or update (upsert) a Tenant-scope setting, addressed by the SettingTypeId in the body |
| [**UpdateTenantSetting**](TenantSettingsApi.md#updatetenantsetting) | **PUT** /v2/tenants/{tenantId}/settings/{settingIdOrCode} | Update the Tenant-scope setting for a key, addressed by SettingType id or Code |

<a id="createtenantsetting"></a>
# **CreateTenantSetting**
> SettingsApiTenantSettingsV1CreateTenantSettingResponse CreateTenantSetting (Guid tenantId, EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody = null)

Create a Tenant-scope setting


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2CreateTenantSettingRequestBody.md) |  | [optional]  |

### Return type

[**SettingsApiTenantSettingsV1CreateTenantSettingResponse**](SettingsApiTenantSettingsV1CreateTenantSettingResponse.md)

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

<a id="deletetenantsetting"></a>
# **DeleteTenantSetting**
> void DeleteTenantSetting (Guid tenantId, string settingIdOrCode, EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody = null)

Delete the Tenant-scope setting for a key, addressed by SettingType id or Code


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **settingIdOrCode** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2DeleteTenantSettingRequestBody.md) |  | [optional]  |

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

<a id="gettenantsetting"></a>
# **GetTenantSetting**
> SettingsApiTenantSettingsV1TenantSettingMessage GetTenantSetting (Guid tenantId, string settingIdOrCode, Guid settingTypeId = null, string provider = null, Guid applicationId = null, bool resolveEffectiveValue = null)

Get a Tenant-scope setting

Answers with the stored record alone. Effective-value resolution is opt-in: pass  `resolveEffectiveValue=true` to instead receive the value in force at this scope — every  layer above it merged under the setting's own value.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **settingIdOrCode** | **string** |  |  |
| **settingTypeId** | **Guid** |  | [optional]  |
| **provider** | **string** |  | [optional]  |
| **applicationId** | **Guid** |  | [optional]  |
| **resolveEffectiveValue** | **bool** |  | [optional] [default to false] |

### Return type

[**SettingsApiTenantSettingsV1TenantSettingMessage**](SettingsApiTenantSettingsV1TenantSettingMessage.md)

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

<a id="searchtenantsettings"></a>
# **SearchTenantSettings**
> SettingsApiTenantSettingsV1SearchTenantSettingsResponse SearchTenantSettings (Guid tenantId, Guid applicationId = null, Guid settingTypeId = null, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

List Tenant-scope settings


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **applicationId** | **Guid** |  | [optional]  |
| **settingTypeId** | **Guid** |  | [optional]  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**SettingsApiTenantSettingsV1SearchTenantSettingsResponse**](SettingsApiTenantSettingsV1SearchTenantSettingsResponse.md)

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

<a id="settenantsetting"></a>
# **SetTenantSetting**
> SettingsApiTenantSettingsV1SetTenantSettingResponse SetTenantSetting (Guid tenantId, EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody = null)

Create or update (upsert) a Tenant-scope setting, addressed by the SettingTypeId in the body


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2SetTenantSettingRequestBody.md) |  | [optional]  |

### Return type

[**SettingsApiTenantSettingsV1SetTenantSettingResponse**](SettingsApiTenantSettingsV1SetTenantSettingResponse.md)

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

<a id="updatetenantsetting"></a>
# **UpdateTenantSetting**
> void UpdateTenantSetting (Guid tenantId, string settingIdOrCode, EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody = null)

Update the Tenant-scope setting for a key, addressed by SettingType id or Code


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **settingIdOrCode** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2UpdateTenantSettingRequestBody.md) |  | [optional]  |

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

