# EdGraph.Platform.Client.Api.EvaluationSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetEvaluationSetting**](EvaluationSettingsApi.md#getevaluationsetting) | **GET** /tenants/{tenantId}/evaluations/configuration | Gets the Evaluation Settings for a given tenant |
| [**SetEvaluationSettingApplicationSetting**](EvaluationSettingsApi.md#setevaluationsettingapplicationsetting) | **POST** /tenants/{tenantId}/evaluations/configuration/application | Sets the Application Settings of an Evaluation for a given Tenant |
| [**SetEvaluationSettingUserSetting**](EvaluationSettingsApi.md#setevaluationsettingusersetting) | **POST** /tenants/{tenantId}/evaluations/configuration/users | Sets the User Settings of an Evaluation for a given Tenant |

<a id="getevaluationsetting"></a>
# **GetEvaluationSetting**
> EvaluationApiEvaluationSettingsV1EvaluationSettingResponse GetEvaluationSetting (Guid tenantId)

Gets the Evaluation Settings for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EvaluationApiEvaluationSettingsV1EvaluationSettingResponse**](EvaluationApiEvaluationSettingsV1EvaluationSettingResponse.md)

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

<a id="setevaluationsettingapplicationsetting"></a>
# **SetEvaluationSettingApplicationSetting**
> EvaluationApiEvaluationSettingsV1ApplicationSetResponse SetEvaluationSettingApplicationSetting (Guid tenantId, EvaluationApiEvaluationSettingsV1SetApplicationRequest evaluationApiEvaluationSettingsV1SetApplicationRequest = null)

Sets the Application Settings of an Evaluation for a given Tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationApiEvaluationSettingsV1SetApplicationRequest** | [**EvaluationApiEvaluationSettingsV1SetApplicationRequest**](EvaluationApiEvaluationSettingsV1SetApplicationRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationSettingsV1ApplicationSetResponse**](EvaluationApiEvaluationSettingsV1ApplicationSetResponse.md)

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

<a id="setevaluationsettingusersetting"></a>
# **SetEvaluationSettingUserSetting**
> EvaluationApiEvaluationSettingsV1UsersSetResponse SetEvaluationSettingUserSetting (Guid tenantId, EvaluationApiEvaluationSettingsV1SetUsersRequest evaluationApiEvaluationSettingsV1SetUsersRequest = null)

Sets the User Settings of an Evaluation for a given Tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evaluationApiEvaluationSettingsV1SetUsersRequest** | [**EvaluationApiEvaluationSettingsV1SetUsersRequest**](EvaluationApiEvaluationSettingsV1SetUsersRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationSettingsV1UsersSetResponse**](EvaluationApiEvaluationSettingsV1UsersSetResponse.md)

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

