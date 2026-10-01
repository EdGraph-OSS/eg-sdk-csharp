# EdGraph.Platform.Client.Api.EnrollmentAdminStudentsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddEnrollmentStudentContact**](EnrollmentAdminStudentsApi.md#addenrollmentstudentcontact) | **POST** /tenants/{tenantId}/enrollmentadmin/students/{id}/contacts/{contactId} | Links an existing contact to a student. |
| [**AddOrCreateEnrollmentStudentContact**](EnrollmentAdminStudentsApi.md#addorcreateenrollmentstudentcontact) | **POST** /tenants/{tenantId}/enrollmentadmin/students/{id}/contacts | Links a contact to a student, creating the contact first if its &#x60;contactId&#x60; does not  already exist. |
| [**GetEnrollmentStudentById**](EnrollmentAdminStudentsApi.md#getenrollmentstudentbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/students/{id} | Gets an Enrollment Student by its record id. |
| [**GetEnrollmentStudentContacts**](EnrollmentAdminStudentsApi.md#getenrollmentstudentcontacts) | **GET** /tenants/{tenantId}/enrollmentadmin/students/{id}/contacts | Gets a student&#39;s linked contacts, with each contact&#39;s live name/email/phone and this student&#39;s  own association attributes for it. |
| [**GetEnrollmentStudentRegistrations**](EnrollmentAdminStudentsApi.md#getenrollmentstudentregistrations) | **GET** /tenants/{tenantId}/enrollmentadmin/students/{id}/registrations | Gets a student&#39;s Registrations. |
| [**GetEnrollmentStudents**](EnrollmentAdminStudentsApi.md#getenrollmentstudents) | **GET** /tenants/{tenantId}/enrollmentadmin/students | Searches Enrollment Students. |
| [**RemoveEnrollmentStudentContact**](EnrollmentAdminStudentsApi.md#removeenrollmentstudentcontact) | **DELETE** /tenants/{tenantId}/enrollmentadmin/students/{id}/contacts/{contactId} | Removes a contact&#39;s link to a student. |
| [**UpdateEnrollmentStudent**](EnrollmentAdminStudentsApi.md#updateenrollmentstudent) | **PUT** /tenants/{tenantId}/enrollmentadmin/students/{id} | Updates an Enrollment Student&#39;s fields. |
| [**UpdateEnrollmentStudentContact**](EnrollmentAdminStudentsApi.md#updateenrollmentstudentcontact) | **PUT** /tenants/{tenantId}/enrollmentadmin/students/{id}/contacts/{contactId} | Updates a student-contact association&#39;s attributes. |
| [**UpsertEnrollmentStudent**](EnrollmentAdminStudentsApi.md#upsertenrollmentstudent) | **POST** /tenants/{tenantId}/enrollmentadmin/students | Creates or updates an Enrollment Student by its source-system &#x60;studentId&#x60;. |

<a id="addenrollmentstudentcontact"></a>
# **AddEnrollmentStudentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto AddEnrollmentStudentContact (string tenantId, Guid id, string contactId)

Links an existing contact to a student.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **contactId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto.md)

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
| **201** | The contact was linked to the student. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addorcreateenrollmentstudentcontact"></a>
# **AddOrCreateEnrollmentStudentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto AddOrCreateEnrollmentStudentContact (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto = null)

Links a contact to a student, creating the contact first if its `contactId` does not  already exist.

When a contact with that `contactId` already exists, the submitted name/email/phone are  ignored - this route only ever links an existing contact, never overwrites it. Use  `.../contacts/{contactId}` instead when the contact is known to already exist and no  creation fallback is wanted.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddOrCreateStudentContactRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto.md)

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
| **201** | The contact was linked to the student. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getenrollmentstudentbyid"></a>
# **GetEnrollmentStudentById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDto GetEnrollmentStudentById (string tenantId, Guid id)

Gets an Enrollment Student by its record id.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDto.md)

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

<a id="getenrollmentstudentcontacts"></a>
# **GetEnrollmentStudentContacts**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactDetailDto&gt; GetEnrollmentStudentContacts (string tenantId, Guid id)

Gets a student's linked contacts, with each contact's live name/email/phone and this student's  own association attributes for it.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactDetailDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactDetailDto.md)

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

<a id="getenrollmentstudentregistrations"></a>
# **GetEnrollmentStudentRegistrations**
> List&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse&gt; GetEnrollmentStudentRegistrations (string tenantId, Guid id)

Gets a student's Registrations.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**List&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse&gt;**](EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse.md)

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

<a id="getenrollmentstudents"></a>
# **GetEnrollmentStudents**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDtoPaginatedItemsViewModel GetEnrollmentStudents (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches Enrollment Students.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 50] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentResponseDtoPaginatedItemsViewModel.md)

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
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removeenrollmentstudentcontact"></a>
# **RemoveEnrollmentStudentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactRemovedResultDto RemoveEnrollmentStudentContact (string tenantId, Guid id, string contactId)

Removes a contact's link to a student.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **contactId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactRemovedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactRemovedResultDto.md)

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
| **200** | The link was removed, or there was none to remove. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateenrollmentstudent"></a>
# **UpdateEnrollmentStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentMutationResultDto UpdateEnrollmentStudent (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto = null)

Updates an Enrollment Student's fields.

Contact association is managed exclusively through the `students/{id}/contacts` routes,  not through this call.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentMutationResultDto.md)

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
| **200** | The student was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateenrollmentstudentcontact"></a>
# **UpdateEnrollmentStudentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto UpdateEnrollmentStudentContact (string tenantId, Guid id, string contactId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentContactRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentContactRequestDto = null)

Updates a student-contact association's attributes.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **contactId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentContactRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentContactRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateStudentContactRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentContactAssociatedResultDto.md)

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
| **200** | The association was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="upsertenrollmentstudent"></a>
# **UpsertEnrollmentStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentMutationResultDto UpsertEnrollmentStudent (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertStudentRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertStudentRequestDto = null)

Creates or updates an Enrollment Student by its source-system `studentId`.

Upsert semantics: unique per `studentId`. A first call creates the student; a later call  for the same `studentId` overwrites the SIS-sourced fields. Contact association is managed  exclusively through the `students/{id}/contacts` routes, not through this call.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertStudentRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertStudentRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpsertStudentRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminStudentMutationResultDto.md)

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
| **201** | The student was created or updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

