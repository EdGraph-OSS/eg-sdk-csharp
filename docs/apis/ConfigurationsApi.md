# EdGraph.Platform.Client.Api.ConfigurationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateAnalyticsConfigurationAsync**](ConfigurationsApi.md#createanalyticsconfigurationasync) | **POST** /tenants/{tenantId}/analytics/configurations | Creates a new configuration. |
| [**DeleteAnalyticsConfigurationAsync**](ConfigurationsApi.md#deleteanalyticsconfigurationasync) | **DELETE** /tenants/{tenantId}/analytics/configurations/{configurationId} | Deletes a configuration. |
| [**GetAllAnalyticsConfigurationsAsync**](ConfigurationsApi.md#getallanalyticsconfigurationsasync) | **GET** /tenants/{tenantId}/analytics/configurations | Retrieves all configurations. |
| [**GetAnalyticsConfigurationByIdAsync**](ConfigurationsApi.md#getanalyticsconfigurationbyidasync) | **GET** /tenants/{tenantId}/analytics/configurations/{configurationId} | Retrieves a configuration by ID. |
| [**GetAnalyticsConfigurationByTenantIdAsync**](ConfigurationsApi.md#getanalyticsconfigurationbytenantidasync) | **GET** /tenants/{tenantId}/analytics/configurations/default | Retrieves current default configuration. |
| [**HasValidAnalyticsConfigurationAsync**](ConfigurationsApi.md#hasvalidanalyticsconfigurationasync) | **GET** /tenants/{tenantId}/analytics/configurations/default/valid | Verifies if current default configuration has required values for correct functionality. |
| [**UpdateAnalyticsConfigurationAsync**](ConfigurationsApi.md#updateanalyticsconfigurationasync) | **PUT** /tenants/{tenantId}/analytics/configurations/{configurationId} | Updates a configuration. |
| [**ValidateAADTokenAsync**](ConfigurationsApi.md#validateaadtokenasync) | **POST** /tenants/{tenantId}/analytics/configurations/azure/testconnection | Verifies if AAD token generation is possible with user provided values. |

<a id="createanalyticsconfigurationasync"></a>
# **CreateAnalyticsConfigurationAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfiguration CreateAnalyticsConfigurationAsync (string tenantId, string workspaceName, AnalyticsApiConfigurationsV1CreateConfigurationRequest analyticsApiConfigurationsV1CreateConfigurationRequest = null)

Creates a new configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **workspaceName** | **string** |  |  |
| **analyticsApiConfigurationsV1CreateConfigurationRequest** | [**AnalyticsApiConfigurationsV1CreateConfigurationRequest**](AnalyticsApiConfigurationsV1CreateConfigurationRequest.md) |  | [optional]  |

### Return type

[**AnalyticsApiConfigurationsV1AnalyticsConfiguration**](AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

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

<a id="deleteanalyticsconfigurationasync"></a>
# **DeleteAnalyticsConfigurationAsync**
> void DeleteAnalyticsConfigurationAsync (string tenantId, string configurationId)

Deletes a configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **configurationId** | **string** |  |  |

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

<a id="getallanalyticsconfigurationsasync"></a>
# **GetAllAnalyticsConfigurationsAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel GetAllAnalyticsConfigurationsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves all configurations.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel**](AnalyticsApiConfigurationsV1AnalyticsConfigurationPaginatedItemsViewModel.md)

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

<a id="getanalyticsconfigurationbyidasync"></a>
# **GetAnalyticsConfigurationByIdAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfiguration GetAnalyticsConfigurationByIdAsync (string tenantId, string configurationId)

Retrieves a configuration by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **configurationId** | **string** |  |  |

### Return type

[**AnalyticsApiConfigurationsV1AnalyticsConfiguration**](AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

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

<a id="getanalyticsconfigurationbytenantidasync"></a>
# **GetAnalyticsConfigurationByTenantIdAsync**
> AnalyticsApiConfigurationsV1AnalyticsConfiguration GetAnalyticsConfigurationByTenantIdAsync (string tenantId)

Retrieves current default configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**AnalyticsApiConfigurationsV1AnalyticsConfiguration**](AnalyticsApiConfigurationsV1AnalyticsConfiguration.md)

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

<a id="hasvalidanalyticsconfigurationasync"></a>
# **HasValidAnalyticsConfigurationAsync**
> AnalyticsApiConfigurationsV1HasValidConfigurationResponse HasValidAnalyticsConfigurationAsync (string tenantId)

Verifies if current default configuration has required values for correct functionality.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**AnalyticsApiConfigurationsV1HasValidConfigurationResponse**](AnalyticsApiConfigurationsV1HasValidConfigurationResponse.md)

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

<a id="updateanalyticsconfigurationasync"></a>
# **UpdateAnalyticsConfigurationAsync**
> AnalyticsApiConfigurationsV1ConfigurationResponse UpdateAnalyticsConfigurationAsync (string tenantId, string configurationId, AnalyticsApiConfigurationsV1UpdateConfigurationRequest analyticsApiConfigurationsV1UpdateConfigurationRequest = null)

Updates a configuration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **configurationId** | **string** |  |  |
| **analyticsApiConfigurationsV1UpdateConfigurationRequest** | [**AnalyticsApiConfigurationsV1UpdateConfigurationRequest**](AnalyticsApiConfigurationsV1UpdateConfigurationRequest.md) |  | [optional]  |

### Return type

[**AnalyticsApiConfigurationsV1ConfigurationResponse**](AnalyticsApiConfigurationsV1ConfigurationResponse.md)

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

<a id="validateaadtokenasync"></a>
# **ValidateAADTokenAsync**
> AnalyticsApiConfigurationsV1TestConnectionResponse ValidateAADTokenAsync (string tenantId, AnalyticsApiConfigurationsV1AnalyticsAzureAd analyticsApiConfigurationsV1AnalyticsAzureAd = null)

Verifies if AAD token generation is possible with user provided values.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiConfigurationsV1AnalyticsAzureAd** | [**AnalyticsApiConfigurationsV1AnalyticsAzureAd**](AnalyticsApiConfigurationsV1AnalyticsAzureAd.md) |  | [optional]  |

### Return type

[**AnalyticsApiConfigurationsV1TestConnectionResponse**](AnalyticsApiConfigurationsV1TestConnectionResponse.md)

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

