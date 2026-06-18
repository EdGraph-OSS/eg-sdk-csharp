# EdGraph.Platform.Client.Api.ClientsSecretsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddClientSecret**](ClientsSecretsApi.md#addclientsecret) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/secrets | Creates a new secret for an OpenId client |
| [**RegenerateOneRosterApiClientSecretAsync**](ClientsSecretsApi.md#regenerateonerosterapiclientsecretasync) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/regeneratesecret | Regenerate Client Secret |

<a id="addclientsecret"></a>
# **AddClientSecret**
> IMSAdminApiV1ClientsClientSecretAddedResponse AddClientSecret (string tenantId, string instanceId, string clientId, IMSAdminApiV1ClientsAddClientSecretRequest iMSAdminApiV1ClientsAddClientSecretRequest = null)

Creates a new secret for an OpenId client


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **iMSAdminApiV1ClientsAddClientSecretRequest** | [**IMSAdminApiV1ClientsAddClientSecretRequest**](IMSAdminApiV1ClientsAddClientSecretRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientSecretAddedResponse**](IMSAdminApiV1ClientsClientSecretAddedResponse.md)

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

<a id="regenerateonerosterapiclientsecretasync"></a>
# **RegenerateOneRosterApiClientSecretAsync**
> IMSAdminApiV1ClientsClientSecretRegeneratedResponse RegenerateOneRosterApiClientSecretAsync (string tenantId, string instanceId, string clientId, IMSAdminApiV1ClientsRegenerateClientSecretRequest iMSAdminApiV1ClientsRegenerateClientSecretRequest = null)

Regenerate Client Secret


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **iMSAdminApiV1ClientsRegenerateClientSecretRequest** | [**IMSAdminApiV1ClientsRegenerateClientSecretRequest**](IMSAdminApiV1ClientsRegenerateClientSecretRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientSecretRegeneratedResponse**](IMSAdminApiV1ClientsClientSecretRegeneratedResponse.md)

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

