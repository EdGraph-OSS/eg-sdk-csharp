# EdGraph.Platform.Client.Api.FormsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateForm**](FormsApi.md#createform) | **POST** /tenants/{tenantId}/forms | Creates a new Form for a given tenant |
| [**CreateFullForm**](FormsApi.md#createfullform) | **POST** /tenants/{tenantId}/forms/full | Fully creates a new Form for a given tenant (with Sections and Questions). |
| [**DeleteForm**](FormsApi.md#deleteform) | **DELETE** /tenants/{tenantId}/forms/{formId} | Deletes a Form. |
| [**DuplicateForm**](FormsApi.md#duplicateform) | **POST** /tenants/{tenantId}/forms/{formId}/duplicate | Duplicates all Form data for a given tenant (with Sections and Questions). |
| [**GetForm**](FormsApi.md#getform) | **GET** /tenants/{tenantId}/forms/{formId} | Get Form. |
| [**GetFormAccess**](FormsApi.md#getformaccess) | **GET** /tenants/{tenantId}/forms/{formId}/access | Get the Access Type for a Form. |
| [**ImportForm**](FormsApi.md#importform) | **POST** /tenants/{tenantId}/forms/import | Imports all form data for a given tenant. |
| [**SearchForms**](FormsApi.md#searchforms) | **GET** /tenants/{tenantId}/forms | Search Forms |
| [**SetFormAccess**](FormsApi.md#setformaccess) | **PUT** /tenants/{tenantId}/forms/{formId}/access | Sets the Access Type for a Form. |
| [**UpdateForm**](FormsApi.md#updateform) | **PUT** /tenants/{tenantId}/forms/{formId} | Updates a Form. |
| [**UpdateFullForm**](FormsApi.md#updatefullform) | **PUT** /tenants/{tenantId}/forms/{formId}/full | Fully updates a Form for a given tenant (with Sections and Questions). |

<a id="createform"></a>
# **CreateForm**
> FormApiFormsV1FormCreatedResponse CreateForm (Guid tenantId, FormApiFormsV1CreateFormRequest formApiFormsV1CreateFormRequest = null)

Creates a new Form for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formApiFormsV1CreateFormRequest** | [**FormApiFormsV1CreateFormRequest**](FormApiFormsV1CreateFormRequest.md) |  | [optional]  |

### Return type

[**FormApiFormsV1FormCreatedResponse**](FormApiFormsV1FormCreatedResponse.md)

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

<a id="createfullform"></a>
# **CreateFullForm**
> FormApiFormsV1FullFormCreatedResponse CreateFullForm (Guid tenantId, FormApiFormsV1CreateFullFormRequest formApiFormsV1CreateFullFormRequest = null)

Fully creates a new Form for a given tenant (with Sections and Questions).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formApiFormsV1CreateFullFormRequest** | [**FormApiFormsV1CreateFullFormRequest**](FormApiFormsV1CreateFullFormRequest.md) |  | [optional]  |

### Return type

[**FormApiFormsV1FullFormCreatedResponse**](FormApiFormsV1FullFormCreatedResponse.md)

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

<a id="deleteform"></a>
# **DeleteForm**
> FormApiFormsV1FormDeletedResponse DeleteForm (Guid tenantId, Guid formId)

Deletes a Form.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |

### Return type

[**FormApiFormsV1FormDeletedResponse**](FormApiFormsV1FormDeletedResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="duplicateform"></a>
# **DuplicateForm**
> FormApiFormsV1FormDuplicatedResponse DuplicateForm (Guid tenantId, Guid formId)

Duplicates all Form data for a given tenant (with Sections and Questions).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |

### Return type

[**FormApiFormsV1FormDuplicatedResponse**](FormApiFormsV1FormDuplicatedResponse.md)

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

<a id="getform"></a>
# **GetForm**
> EdGraphHttpAggregatorsTenantApiServicesFormsV1Form GetForm (Guid tenantId, Guid formId)

Get Form.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesFormsV1Form**](EdGraphHttpAggregatorsTenantApiServicesFormsV1Form.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getformaccess"></a>
# **GetFormAccess**
> FormApiFormsV1FormAccessResponse GetFormAccess (Guid tenantId, Guid formId)

Get the Access Type for a Form.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |

### Return type

[**FormApiFormsV1FormAccessResponse**](FormApiFormsV1FormAccessResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="importform"></a>
# **ImportForm**
> Object ImportForm (Guid tenantId, Object body = null)

Imports all form data for a given tenant.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

**Object**

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

<a id="searchforms"></a>
# **SearchForms**
> EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel SearchForms (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Search Forms


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiServicesFormsV1FormPaginatedItemsViewModel.md)

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

<a id="setformaccess"></a>
# **SetFormAccess**
> FormApiFormsV1FormAccessSetResponse SetFormAccess (Guid tenantId, Guid formId, FormApiFormsV1SetFormAccessRequest formApiFormsV1SetFormAccessRequest = null)

Sets the Access Type for a Form.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **formApiFormsV1SetFormAccessRequest** | [**FormApiFormsV1SetFormAccessRequest**](FormApiFormsV1SetFormAccessRequest.md) |  | [optional]  |

### Return type

[**FormApiFormsV1FormAccessSetResponse**](FormApiFormsV1FormAccessSetResponse.md)

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

<a id="updateform"></a>
# **UpdateForm**
> FormApiFormsV1FormUpdatedResponse UpdateForm (Guid tenantId, Guid formId, FormApiFormsV1UpdateFormRequest formApiFormsV1UpdateFormRequest = null)

Updates a Form.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **formApiFormsV1UpdateFormRequest** | [**FormApiFormsV1UpdateFormRequest**](FormApiFormsV1UpdateFormRequest.md) |  | [optional]  |

### Return type

[**FormApiFormsV1FormUpdatedResponse**](FormApiFormsV1FormUpdatedResponse.md)

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

<a id="updatefullform"></a>
# **UpdateFullForm**
> FormApiFormsV1FullFormUpdatedResponse UpdateFullForm (Guid tenantId, Guid formId, FormApiFormsV1UpdateFullFormRequest formApiFormsV1UpdateFullFormRequest = null)

Fully updates a Form for a given tenant (with Sections and Questions).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **formApiFormsV1UpdateFullFormRequest** | [**FormApiFormsV1UpdateFullFormRequest**](FormApiFormsV1UpdateFullFormRequest.md) |  | [optional]  |

### Return type

[**FormApiFormsV1FullFormUpdatedResponse**](FormApiFormsV1FullFormUpdatedResponse.md)

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

