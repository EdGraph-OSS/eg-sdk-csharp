# EdGraph.Platform.Client.Api.OnboardingStepsConnectionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOnboardingStepConnection**](OnboardingStepsConnectionsApi.md#createonboardingstepconnection) | **POST** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections | Creates an Onboarding Step connection. |
| [**GetOnboardingStepConnectionById**](OnboardingStepsConnectionsApi.md#getonboardingstepconnectionbyid) | **GET** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Get an Onboarding Step connection by Id |
| [**UpdateOnboardingStepConnection**](OnboardingStepsConnectionsApi.md#updateonboardingstepconnection) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber}/connections/{connectionId} | Update an Onboarding Step connection by Id |

<a id="createonboardingstepconnection"></a>
# **CreateOnboardingStepConnection**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse CreateOnboardingStepConnection (string tenantId, int stepNumber, Object body = null)

Creates an Onboarding Step connection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionCreatedResponse.md)

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

<a id="getonboardingstepconnectionbyid"></a>
# **GetOnboardingStepConnectionById**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse GetOnboardingStepConnectionById (string tenantId, int stepNumber, string connectionId)

Get an Onboarding Step connection by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **connectionId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionResponse.md)

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

<a id="updateonboardingstepconnection"></a>
# **UpdateOnboardingStepConnection**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse UpdateOnboardingStepConnection (string tenantId, int stepNumber, string connectionId, Object body = null)

Update an Onboarding Step connection by Id


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **connectionId** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsConnectionUpdatedResponse.md)

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

