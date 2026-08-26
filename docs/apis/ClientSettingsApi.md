# EdGraph.Platform.Client.Api.ClientSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateClientSetting**](ClientSettingsApi.md#createclientsetting) | **POST** /v2/tenants/{tenantId}/clients/{clientId}/settings | Create a Client-scope setting |
| [**DeleteClientSetting**](ClientSettingsApi.md#deleteclientsetting) | **DELETE** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Delete the Client-scope setting for a key, addressed by SettingType id or Code |
| [**GetClientSetting**](ClientSettingsApi.md#getclientsetting) | **GET** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Get a Client-scope setting |
| [**SearchClientSettings**](ClientSettingsApi.md#searchclientsettings) | **GET** /v2/tenants/{tenantId}/clients/{clientId}/settings | List Client-scope settings |
| [**SetClientSetting**](ClientSettingsApi.md#setclientsetting) | **PUT** /v2/tenants/{tenantId}/clients/{clientId}/settings | Create or update (upsert) a Client-scope setting, addressed by the SettingTypeId in the body |
| [**UpdateClientSetting**](ClientSettingsApi.md#updateclientsetting) | **PUT** /v2/tenants/{tenantId}/clients/{clientId}/settings/{settingIdOrCode} | Update the Client-scope setting for a key, addressed by SettingType id or Code |

<a id="createclientsetting"></a>
# **CreateClientSetting**
> SettingsApiClientSettingsV1CreateClientSettingResponse CreateClientSetting (Guid tenantId, string clientId, EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody = null)

Create a Client-scope setting


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2CreateClientSettingRequestBody.md) |  | [optional]  |

### Return type

[**SettingsApiClientSettingsV1CreateClientSettingResponse**](SettingsApiClientSettingsV1CreateClientSettingResponse.md)

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

<a id="deleteclientsetting"></a>
# **DeleteClientSetting**
> void DeleteClientSetting (Guid tenantId, string clientId, string settingIdOrCode, EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody = null)

Delete the Client-scope setting for a key, addressed by SettingType id or Code


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **settingIdOrCode** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2DeleteClientSettingRequestBody.md) |  | [optional]  |

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

<a id="getclientsetting"></a>
# **GetClientSetting**
> SettingsApiClientSettingsV1ClientSettingMessage GetClientSetting (Guid tenantId, string clientId, string settingIdOrCode, Guid settingTypeId = null, string provider = null, Guid applicationId = null, bool resolveEffectiveValue = null)

Get a Client-scope setting

Answers with the stored record alone. Effective-value resolution is opt-in: pass  `resolveEffectiveValue=true` to instead receive the value in force at this scope — every  layer above it merged under the setting's own value.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **settingIdOrCode** | **string** |  |  |
| **settingTypeId** | **Guid** |  | [optional]  |
| **provider** | **string** |  | [optional]  |
| **applicationId** | **Guid** |  | [optional]  |
| **resolveEffectiveValue** | **bool** |  | [optional] [default to false] |

### Return type

[**SettingsApiClientSettingsV1ClientSettingMessage**](SettingsApiClientSettingsV1ClientSettingMessage.md)

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

<a id="searchclientsettings"></a>
# **SearchClientSettings**
> SettingsApiClientSettingsV1SearchClientSettingsResponse SearchClientSettings (Guid tenantId, string clientId, Guid applicationId = null, Guid settingTypeId = null, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

List Client-scope settings


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **applicationId** | **Guid** |  | [optional]  |
| **settingTypeId** | **Guid** |  | [optional]  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**SettingsApiClientSettingsV1SearchClientSettingsResponse**](SettingsApiClientSettingsV1SearchClientSettingsResponse.md)

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

<a id="setclientsetting"></a>
# **SetClientSetting**
> SettingsApiClientSettingsV1SetClientSettingResponse SetClientSetting (Guid tenantId, string clientId, EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody = null)

Create or update (upsert) a Client-scope setting, addressed by the SettingTypeId in the body


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2SetClientSettingRequestBody.md) |  | [optional]  |

### Return type

[**SettingsApiClientSettingsV1SetClientSettingResponse**](SettingsApiClientSettingsV1SetClientSettingResponse.md)

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

<a id="updateclientsetting"></a>
# **UpdateClientSetting**
> void UpdateClientSetting (Guid tenantId, string clientId, string settingIdOrCode, EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody edGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody = null)

Update the Client-scope setting for a key, addressed by SettingType id or Code


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **clientId** | **string** |  |  |
| **settingIdOrCode** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody** | [**EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody**](EdGraphHttpAggregatorsTenantApiControllersV2UpdateClientSettingRequestBody.md) |  | [optional]  |

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

