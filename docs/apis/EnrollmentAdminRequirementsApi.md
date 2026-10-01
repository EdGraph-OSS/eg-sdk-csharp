# EdGraph.Platform.Client.Api.EnrollmentAdminRequirementsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateRequirement**](EnrollmentAdminRequirementsApi.md#createrequirement) | **POST** /tenants/{tenantId}/enrollmentadmin/requirements | Creates a requirement. Leave &#x60;isRequired&#x60; out to create a required one. A &#x60;url&#x60;  requirement needs &#x60;url&#x60;, an absolute http or https link. |
| [**DeleteRequirement**](EnrollmentAdminRequirementsApi.md#deleterequirement) | **DELETE** /tenants/{tenantId}/enrollmentadmin/requirements/{id} | Removes a requirement (soft delete). Programs that embed it keep their copy. |
| [**GetRequirementById**](EnrollmentAdminRequirementsApi.md#getrequirementbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/requirements/{id} | Gets a requirement by its record id. |
| [**GetRequirements**](EnrollmentAdminRequirementsApi.md#getrequirements) | **GET** /tenants/{tenantId}/enrollmentadmin/requirements | Lists the tenant&#39;s requirements, sorted by code. Unpaged. A program names the ones it asks  for by id (&#x60;requirementIds&#x60;) and embeds a copy of each, taken when the program is saved. |
| [**UpdateRequirement**](EnrollmentAdminRequirementsApi.md#updaterequirement) | **PUT** /tenants/{tenantId}/enrollmentadmin/requirements/{id} | Updates a requirement. Every field is replaced except &#x60;isRequired&#x60;, which keeps the  stored value when left out; &#x60;isUploadEnabled&#x60; must be sent. Programs keep the copy  taken when they were last saved, so a change shows on a program only after it is re-saved. |

<a id="createrequirement"></a>
# **CreateRequirement**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto CreateRequirement (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto = null)

Creates a requirement. Leave `isRequired` out to create a required one. A `url`  requirement needs `url`, an absolute http or https link.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRequirementRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **201** | The requirement was created. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **409** | A requirement with this code already exists in the tenant (deleted ones included). |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleterequirement"></a>
# **DeleteRequirement**
> void DeleteRequirement (string tenantId, Guid id)

Removes a requirement (soft delete). Programs that embed it keep their copy.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

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
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **204** | The requirement was removed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getrequirementbyid"></a>
# **GetRequirementById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto GetRequirementById (string tenantId, Guid id)

Gets a requirement by its record id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getrequirements"></a>
# **GetRequirements**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto&gt; GetRequirements (string tenantId)

Lists the tenant's requirements, sorted by code. Unpaged. A program names the ones it asks  for by id (`requirementIds`) and embeds a copy of each, taken when the program is saved.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementResponseDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updaterequirement"></a>
# **UpdateRequirement**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto UpdateRequirement (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto = null)

Updates a requirement. Every field is replaced except `isRequired`, which keeps the  stored value when left out; `isUploadEnabled` must be sent. Programs keep the copy  taken when they were last saved, so a change shows on a program only after it is re-saved.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRequirementRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminRequirementMutationResultDto.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: application/json-patch+json, application/json, text/json, application/*+json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized |  -  |
| **403** | Forbidden |  -  |
| **500** | Server Error |  -  |
| **200** | The requirement was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |
| **409** | Another requirement in the tenant already has this code. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

