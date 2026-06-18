# EdGraph.Platform.Client.Api.WebhooksApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateWebhookAsync**](WebhooksApi.md#createwebhookasync) | **POST** /tenants/{tenantId}/webhooks | Creates a new Webhook |
| [**DeleteWebhookAsync**](WebhooksApi.md#deletewebhookasync) | **DELETE** /tenants/{tenantId}/webhooks/{webhookId} | Removes a webhook. |
| [**GetAllWebhookSubscriptionsAsync**](WebhooksApi.md#getallwebhooksubscriptionsasync) | **GET** /tenants/{tenantId}/webhooks/events |  |
| [**GetAllWebhooksAsync**](WebhooksApi.md#getallwebhooksasync) | **GET** /tenants/{tenantId}/webhooks | Retrieves a list of webhooks. |
| [**GetWebhookByIdAsync**](WebhooksApi.md#getwebhookbyidasync) | **GET** /tenants/{tenantId}/webhooks/{webhookId} | Retrieves a webhook by ID. |
| [**RequestWebhookReRun**](WebhooksApi.md#requestwebhookrerun) | **POST** /tenants/{tenantId}/webhooks/{webhookId}/dispatches/{dispatchId}/rerun |  |
| [**UpdateWebhookAsync**](WebhooksApi.md#updatewebhookasync) | **PUT** /tenants/{tenantId}/webhooks/{webhookId} | Updates a webhook |

<a id="createwebhookasync"></a>
# **CreateWebhookAsync**
> TenantApiWebhookV1WebhookIdResponse CreateWebhookAsync (string tenantId, TenantApiWebhookV1CreateWebhookRequest tenantApiWebhookV1CreateWebhookRequest = null)

Creates a new Webhook


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **tenantApiWebhookV1CreateWebhookRequest** | [**TenantApiWebhookV1CreateWebhookRequest**](TenantApiWebhookV1CreateWebhookRequest.md) |  | [optional]  |

### Return type

[**TenantApiWebhookV1WebhookIdResponse**](TenantApiWebhookV1WebhookIdResponse.md)

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

<a id="deletewebhookasync"></a>
# **DeleteWebhookAsync**
> TenantApiWebhookV1WebhookIdResponse DeleteWebhookAsync (string tenantId, string webhookId)

Removes a webhook.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **webhookId** | **string** |  |  |

### Return type

[**TenantApiWebhookV1WebhookIdResponse**](TenantApiWebhookV1WebhookIdResponse.md)

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

<a id="getallwebhooksubscriptionsasync"></a>
# **GetAllWebhookSubscriptionsAsync**
> TenantApiWebhookV1PaginatedWebhookEventItemsResponse GetAllWebhookSubscriptionsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)




### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiWebhookV1PaginatedWebhookEventItemsResponse**](TenantApiWebhookV1PaginatedWebhookEventItemsResponse.md)

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

<a id="getallwebhooksasync"></a>
# **GetAllWebhooksAsync**
> TenantApiWebhookV1PaginatedItemsResponse GetAllWebhooksAsync (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of webhooks.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiWebhookV1PaginatedItemsResponse**](TenantApiWebhookV1PaginatedItemsResponse.md)

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

<a id="getwebhookbyidasync"></a>
# **GetWebhookByIdAsync**
> TenantApiWebhookV1WebhookResponse GetWebhookByIdAsync (string tenantId, string webhookId)

Retrieves a webhook by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **webhookId** | **string** |  |  |

### Return type

[**TenantApiWebhookV1WebhookResponse**](TenantApiWebhookV1WebhookResponse.md)

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

<a id="requestwebhookrerun"></a>
# **RequestWebhookReRun**
> TenantApiWebhookV1ReRunRequestedResponse RequestWebhookReRun (Guid tenantId, Guid webhookId, Guid dispatchId, TenantApiWebhookV1RequestReRunRequest tenantApiWebhookV1RequestReRunRequest = null)




### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **webhookId** | **Guid** |  |  |
| **dispatchId** | **Guid** |  |  |
| **tenantApiWebhookV1RequestReRunRequest** | [**TenantApiWebhookV1RequestReRunRequest**](TenantApiWebhookV1RequestReRunRequest.md) |  | [optional]  |

### Return type

[**TenantApiWebhookV1ReRunRequestedResponse**](TenantApiWebhookV1ReRunRequestedResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatewebhookasync"></a>
# **UpdateWebhookAsync**
> TenantApiWebhookV1WebhookIdResponse UpdateWebhookAsync (string tenantId, string webhookId, TenantApiWebhookV1UpdateWebhookRequest tenantApiWebhookV1UpdateWebhookRequest = null)

Updates a webhook


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **webhookId** | **string** |  |  |
| **tenantApiWebhookV1UpdateWebhookRequest** | [**TenantApiWebhookV1UpdateWebhookRequest**](TenantApiWebhookV1UpdateWebhookRequest.md) |  | [optional]  |

### Return type

[**TenantApiWebhookV1WebhookIdResponse**](TenantApiWebhookV1WebhookIdResponse.md)

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

