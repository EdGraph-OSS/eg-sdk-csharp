# EdGraph.Platform.Client.Api.EnrollmentAdminRegistrationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddEnrollmentRegistrationApplication**](EnrollmentAdminRegistrationsApi.md#addenrollmentregistrationapplication) | **POST** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/applications | Adds one Program-seat choice to an existing Registration - the standalone counterpart to  passing initial choices at creation time. |
| [**ApproveEnrollmentRegistration**](EnrollmentAdminRegistrationsApi.md#approveenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/approve | Approves a Registration - assigns the linked Student and Contacts and flips its status. |
| [**ApproveEnrollmentRegistrationApplication**](EnrollmentAdminRegistrationsApi.md#approveenrollmentregistrationapplication) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/applications/{applicationId}/approve | Approves a single Application on a Registration, independently of its siblings. |
| [**CreateEnrollmentRegistration**](EnrollmentAdminRegistrationsApi.md#createenrollmentregistration) | **POST** /tenants/{tenantId}/enrollmentadmin/registrations | Creates a Registration. |
| [**DeleteEnrollmentRegistration**](EnrollmentAdminRegistrationsApi.md#deleteenrollmentregistration) | **DELETE** /tenants/{tenantId}/enrollmentadmin/registrations/{id} | Removes a Registration. |
| [**GetEnrollmentRegistration**](EnrollmentAdminRegistrationsApi.md#getenrollmentregistration) | **GET** /tenants/{tenantId}/enrollmentadmin/registrations/{id} | Gets a Registration by its id. |
| [**GetEnrollmentRegistrationApplications**](EnrollmentAdminRegistrationsApi.md#getenrollmentregistrationapplications) | **GET** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/applications | Gets a Registration&#39;s Applications - each a zero-to-many, independently approvable  Program-seat choice. |
| [**GetEnrollmentRegistrations**](EnrollmentAdminRegistrationsApi.md#getenrollmentregistrations) | **GET** /tenants/{tenantId}/enrollmentadmin/registrations | Searches Registrations - a parent&#39;s enrollment submission requesting a seat in a School/District  Program. |
| [**RejectEnrollmentRegistration**](EnrollmentAdminRegistrationsApi.md#rejectenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/reject | Explicitly rejects a Registration - sets its status to Rejected. Terminal, like approve: a  later Update/UpdateScreen/StartOver progress recompute does not revert it. |
| [**SubmitEnrollmentRegistration**](EnrollmentAdminRegistrationsApi.md#submitenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id}/submit | Explicitly submits a Registration - sets its status to Submitted. Terminal, like approve: a  later Update/UpdateScreen/StartOver progress recompute does not revert it. |
| [**UpdateEnrollmentRegistration**](EnrollmentAdminRegistrationsApi.md#updateenrollmentregistration) | **PUT** /tenants/{tenantId}/enrollmentadmin/registrations/{id} | Updates a Registration. |

<a id="addenrollmentregistrationapplication"></a>
# **AddEnrollmentRegistrationApplication**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse AddEnrollmentRegistrationApplication (string tenantId, string id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto = null)

Adds one Program-seat choice to an existing Registration - the standalone counterpart to  passing initial choices at creation time.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddRegistrationApplicationRequestDto.md) |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse.md)

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
| **200** | The application was added. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="approveenrollmentregistration"></a>
# **ApproveEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse ApproveEnrollmentRegistration (string tenantId, string id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto = null)

Approves a Registration - assigns the linked Student and Contacts and flips its status.

The `contacts` array replaces/merges into the Registration's existing Contacts collection,  matched by `contactId` (upsert semantics) - there is no separate scalar contactId field.  The `choices` array sets the status of the Registration's Applications; each Application is  independently approvable - see the `applications/{applicationId}/approve` route to approve  just one without touching the others.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto.md) |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse.md)

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
| **200** | The registration was approved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="approveenrollmentregistrationapplication"></a>
# **ApproveEnrollmentRegistrationApplication**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse ApproveEnrollmentRegistrationApplication (string tenantId, string id, string applicationId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto = null)

Approves a single Application on a Registration, independently of its siblings.

Same request body shape as `PUT .../registrations/{id}/approve`. Future Phase 99:  `PUT .../registrations/{id}/contacts/{id}/match` is out of scope and not implemented here.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |
| **applicationId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminRegistrationApproveRequestDto.md) |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse.md)

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
| **200** | The application was approved. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createenrollmentregistration"></a>
# **CreateEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationCreatedResponse CreateEnrollmentRegistration (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto = null)

Creates a Registration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateRegistrationRequestDto.md) |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationCreatedResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationCreatedResponse.md)

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
| **201** | The registration was created. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteenrollmentregistration"></a>
# **DeleteEnrollmentRegistration**
> void DeleteEnrollmentRegistration (string tenantId, string id)

Removes a Registration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |

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
| **204** | The registration was removed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getenrollmentregistration"></a>
# **GetEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse GetEnrollmentRegistration (string tenantId, string id)

Gets a Registration by its id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse.md)

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

<a id="getenrollmentregistrationapplications"></a>
# **GetEnrollmentRegistrationApplications**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationsListResponse GetEnrollmentRegistrationApplications (string tenantId, string id)

Gets a Registration's Applications - each a zero-to-many, independently approvable  Program-seat choice.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationsListResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationApplicationsListResponse.md)

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

<a id="getenrollmentregistrations"></a>
# **GetEnrollmentRegistrations**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationsSearchResponse GetEnrollmentRegistrations (string tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Searches Registrations - a parent's enrollment submission requesting a seat in a School/District  Program.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationsSearchResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationsSearchResponse.md)

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

<a id="rejectenrollmentregistration"></a>
# **RejectEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse RejectEnrollmentRegistration (string tenantId, string id, Object body = null)

Explicitly rejects a Registration - sets its status to Rejected. Terminal, like approve: a  later Update/UpdateScreen/StartOver progress recompute does not revert it.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse.md)

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
| **200** | The registration was rejected. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="submitenrollmentregistration"></a>
# **SubmitEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse SubmitEnrollmentRegistration (string tenantId, string id, Object body = null)

Explicitly submits a Registration - sets its status to Submitted. Terminal, like approve: a  later Update/UpdateScreen/StartOver progress recompute does not revert it.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse.md)

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
| **200** | The registration was submitted. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateenrollmentregistration"></a>
# **UpdateEnrollmentRegistration**
> EnrollmentApiEnrollmentRegistrationsV1RegistrationUpdatedResponse UpdateEnrollmentRegistration (string tenantId, string id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto = null)

Updates a Registration.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateRegistrationRequestDto.md) |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentRegistrationsV1RegistrationUpdatedResponse**](EnrollmentApiEnrollmentRegistrationsV1RegistrationUpdatedResponse.md)

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
| **200** | The registration was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

