# EdGraph.Platform.Client.Api.InstanceOnboardingStepsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateInstanceOnboardingStepAsync**](InstanceOnboardingStepsApi.md#createinstanceonboardingstepasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps | Creates an Onboarding Step. |
| [**UpdateInstanceOnboardingStepAsync**](InstanceOnboardingStepsApi.md#updateinstanceonboardingstepasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step. |

<a id="createinstanceonboardingstepasync"></a>
# **CreateInstanceOnboardingStepAsync**
> EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse CreateInstanceOnboardingStepAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest = null)

Creates an Onboarding Step.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateOnboardingStepRequest** | [**EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest**](EdfiAdminApiEdfiAdminV1CreateOnboardingStepRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse**](EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)

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

<a id="updateinstanceonboardingstepasync"></a>
# **UpdateInstanceOnboardingStepAsync**
> EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse UpdateInstanceOnboardingStepAsync (string tenantId, string instanceId, int stepNumber, EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest = null)

Updates the status of an Onboarding Step.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest** | [**EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest**](EdfiAdminApiEdfiAdminV1UpdateOnboardingStepRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse**](EdfiAdminApiEdfiAdminV1InstanceUpdatedResponse.md)

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

