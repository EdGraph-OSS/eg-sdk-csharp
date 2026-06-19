# EdGraph.Platform.Client.Api.SettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetTenantSettingByCode**](SettingsApi.md#gettenantsettingbycode) | **GET** /tenants/{tenantId}/tenantsettings/{code} | Retrieves a Tenant&#39;s settings by code. |
| [**GetTenantSettings**](SettingsApi.md#gettenantsettings) | **GET** /tenants/{tenantId}/settings | Retrieves a list of the Tenant&#39;s settings. |
| [**GetTenantSettingsByCode**](SettingsApi.md#gettenantsettingsbycode) | **GET** /tenants/{tenantId}/settings/{code} | Retrieves a Tenant&#39;s settings by code. |
| [**SetTenantSettings**](SettingsApi.md#settenantsettings) | **POST** /tenants/{tenantId}/settings/{code} | Creates/updates a Tenant&#39;s settings. |

<a id="gettenantsettingbycode"></a>
# **GetTenantSettingByCode**
> TenantApiTenantV1TenantSetting GetTenantSettingByCode (Guid tenantId, string code)

Retrieves a Tenant's settings by code.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **code** | **string** |  |  |

### Return type

[**TenantApiTenantV1TenantSetting**](TenantApiTenantV1TenantSetting.md)

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

<a id="gettenantsettings"></a>
# **GetTenantSettings**
> TenantApiTenantV1GetAppSettingsResponse GetTenantSettings (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of the Tenant's settings.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiTenantV1GetAppSettingsResponse**](TenantApiTenantV1GetAppSettingsResponse.md)

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

<a id="gettenantsettingsbycode"></a>
# **GetTenantSettingsByCode**
> TenantApiTenantV1TenantAppSettings GetTenantSettingsByCode (Guid tenantId, string code)

Retrieves a Tenant's settings by code.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **code** | **string** |  |  |

### Return type

[**TenantApiTenantV1TenantAppSettings**](TenantApiTenantV1TenantAppSettings.md)

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

<a id="settenantsettings"></a>
# **SetTenantSettings**
> TenantApiTenantV1SetAppSettingsResponse SetTenantSettings (Guid tenantId, string code, TenantApiTenantV1SetAppSettingsRequest tenantApiTenantV1SetAppSettingsRequest = null)

Creates/updates a Tenant's settings.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **code** | **string** |  |  |
| **tenantApiTenantV1SetAppSettingsRequest** | [**TenantApiTenantV1SetAppSettingsRequest**](TenantApiTenantV1SetAppSettingsRequest.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1SetAppSettingsResponse**](TenantApiTenantV1SetAppSettingsResponse.md)

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

