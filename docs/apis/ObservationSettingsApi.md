# EdGraph.Platform.Client.Api.ObservationSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddAvailablePersona**](ObservationSettingsApi.md#addavailablepersona) | **POST** /tenants/{tenantId}/observations/settings/personas | Adds a persona for a given Tenant |
| [**GetApplicationSettings**](ObservationSettingsApi.md#getapplicationsettings) | **GET** /tenants/{tenantId}/observations/settings/application | Gets the application settings for the tenant |
| [**GetPaginatedForms**](ObservationSettingsApi.md#getpaginatedforms) | **GET** /tenants/{tenantId}/observations/forms | Get Paginated Forms |
| [**GetPaginatedPersonas**](ObservationSettingsApi.md#getpaginatedpersonas) | **GET** /tenants/{tenantId}/observations/settings/personas | Gets available personas |
| [**GetPaginatedStaffClassifications**](ObservationSettingsApi.md#getpaginatedstaffclassifications) | **GET** /tenants/{tenantId}/observations/settings/available-staffclassifications | Get Paginated Available StaffClassifications |
| [**GetStaffClassificationsSettings**](ObservationSettingsApi.md#getstaffclassificationssettings) | **GET** /tenants/{tenantId}/observations/settings/staffclassifications | Gets the staffClassification settings for the tenant |
| [**GetTEATenantOrganizations**](ObservationSettingsApi.md#getteatenantorganizations) | **GET** /tenants/{tenantId}/observations/tenantorganizations | Get TEA tenant organizations |
| [**SetApplicationSettings**](ObservationSettingsApi.md#setapplicationsettings) | **POST** /tenants/{tenantId}/observations/settings/application | Sets the Application Settings of an Observation for a given Tenant |
| [**SetRolePersonasSettings**](ObservationSettingsApi.md#setrolepersonassettings) | **POST** /tenants/{tenantId}/observations/settings/rolepersonas | Updates personas assigned to a role configuration of the tenants setting |
| [**VerifySysAdminCredentials**](ObservationSettingsApi.md#verifysysadmincredentials) | **GET** /tenants/{tenantId}/observations/settings/verify-credentials | Gets the staffClassification settings for the tenant |

<a id="addavailablepersona"></a>
# **AddAvailablePersona**
> EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse AddAvailablePersona (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest = null)

Adds a persona for a given Tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse.md)

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

<a id="getapplicationsettings"></a>
# **GetApplicationSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse GetApplicationSettings (Guid tenantId)

Gets the application settings for the tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse.md)

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

<a id="getpaginatedforms"></a>
# **GetPaginatedForms**
> EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse GetPaginatedForms (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Get Paginated Forms


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse**](EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse.md)

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

<a id="getpaginatedpersonas"></a>
# **GetPaginatedPersonas**
> EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse GetPaginatedPersonas (Guid tenantId)

Gets available personas


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse.md)

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

<a id="getpaginatedstaffclassifications"></a>
# **GetPaginatedStaffClassifications**
> IdentityApiStaffClassificationV1GetStaffClassificationsResponse GetPaginatedStaffClassifications (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Get Paginated Available StaffClassifications


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiStaffClassificationV1GetStaffClassificationsResponse**](IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)

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

<a id="getstaffclassificationssettings"></a>
# **GetStaffClassificationsSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse GetStaffClassificationsSettings (Guid tenantId)

Gets the staffClassification settings for the tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse.md)

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

<a id="getteatenantorganizations"></a>
# **GetTEATenantOrganizations**
> TenantApiTenantV1OrganizationGetPaginatedItemsResponse GetTEATenantOrganizations (Guid tenantId, string teaTenantId = null, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Get TEA tenant organizations


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **teaTenantId** | **string** |  | [optional] [default to &quot;&quot;] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiTenantV1OrganizationGetPaginatedItemsResponse**](TenantApiTenantV1OrganizationGetPaginatedItemsResponse.md)

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

<a id="setapplicationsettings"></a>
# **SetApplicationSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse SetApplicationSettings (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest = null)

Sets the Application Settings of an Observation for a given Tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse.md)

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

<a id="setrolepersonassettings"></a>
# **SetRolePersonasSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse SetRolePersonasSettings (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest = null)

Updates personas assigned to a role configuration of the tenants setting


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse.md)

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

<a id="verifysysadmincredentials"></a>
# **VerifySysAdminCredentials**
> Object VerifySysAdminCredentials (Guid tenantId)

Gets the staffClassification settings for the tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

**Object**

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

