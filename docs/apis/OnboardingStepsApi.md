# EdGraph.Platform.Client.Api.OnboardingStepsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateOnboardingStep**](OnboardingStepsApi.md#createonboardingstep) | **POST** /tenants/{tenantId}/onboardingsteps | Creates an Onboarding Step. |
| [**GetOnboardingSteps**](OnboardingStepsApi.md#getonboardingsteps) | **GET** /tenants/{tenantId}/onboardingsteps | Gets a list of Onboarding Steps. |
| [**UpdateOnboardingStep**](OnboardingStepsApi.md#updateonboardingstep) | **PUT** /tenants/{tenantId}/onboardingsteps/{stepNumber} | Updates the status of an Onboarding Step. |

<a id="createonboardingstep"></a>
# **CreateOnboardingStep**
> TenantApiTenantV1TenantUpdatedResponse CreateOnboardingStep (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto = null)

Creates an Onboarding Step.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsCreateOnboardingStepRequestDto.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1TenantUpdatedResponse**](TenantApiTenantV1TenantUpdatedResponse.md)

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

<a id="getonboardingsteps"></a>
# **GetOnboardingSteps**
> TenantApiTenantV1OnboardingStepsReponse GetOnboardingSteps (string tenantId)

Gets a list of Onboarding Steps.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**TenantApiTenantV1OnboardingStepsReponse**](TenantApiTenantV1OnboardingStepsReponse.md)

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

<a id="updateonboardingstep"></a>
# **UpdateOnboardingStep**
> TenantApiTenantV1TenantUpdatedResponse UpdateOnboardingStep (string tenantId, int stepNumber, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto = null)

Updates the status of an Onboarding Step.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **stepNumber** | **int** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsUpdateOnboardingStepRequestDto.md) |  | [optional]  |

### Return type

[**TenantApiTenantV1TenantUpdatedResponse**](TenantApiTenantV1TenantUpdatedResponse.md)

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

