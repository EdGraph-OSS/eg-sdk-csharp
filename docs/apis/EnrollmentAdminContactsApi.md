# EdGraph.Platform.Client.Api.EnrollmentAdminContactsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddEnrollmentContactStudent**](EnrollmentAdminContactsApi.md#addenrollmentcontactstudent) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students | Links a student to a contact. |
| [**CreateEnrollmentContact**](EnrollmentAdminContactsApi.md#createenrollmentcontact) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts | Creates or updates an Enrollment Contact by its source-system &#x60;contactId&#x60;. |
| [**GetEnrollmentContactById**](EnrollmentAdminContactsApi.md#getenrollmentcontactbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Gets an Enrollment Contact by its record id, with its linked students. |
| [**GetEnrollmentContactChangelogs**](EnrollmentAdminContactsApi.md#getenrollmentcontactchangelogs) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/changelogs | Reads every lifecycle event for a contact - create, update, delete, overrides and sign-in  unlocks - newest first. |
| [**GetEnrollmentContactOverrides**](EnrollmentAdminContactsApi.md#getenrollmentcontactoverrides) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides | Reads a contact&#39;s override history, newest first. |
| [**GetEnrollmentContactRegistrations**](EnrollmentAdminContactsApi.md#getenrollmentcontactregistrations) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/registrations | Gets a contact&#39;s Registrations. |
| [**GetEnrollmentContactStudents**](EnrollmentAdminContactsApi.md#getenrollmentcontactstudents) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students | Gets a contact&#39;s linked students, with each link&#39;s association attributes. |
| [**GetEnrollmentContacts**](EnrollmentAdminContactsApi.md#getenrollmentcontacts) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts | Searches Enrollment Contacts. |
| [**OverrideEnrollmentContactEmail**](EnrollmentAdminContactsApi.md#overrideenrollmentcontactemail) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/emails | Overrides a contact&#39;s email address. |
| [**OverrideEnrollmentContactPhone**](EnrollmentAdminContactsApi.md#overrideenrollmentcontactphone) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/phones | Overrides a contact&#39;s phone number. |
| [**RemoveEnrollmentContactEmailOverride**](EnrollmentAdminContactsApi.md#removeenrollmentcontactemailoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/emails | Removes a contact&#39;s email override, letting the SIS value show through again. |
| [**RemoveEnrollmentContactPhoneOverride**](EnrollmentAdminContactsApi.md#removeenrollmentcontactphoneoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides/phones | Removes a contact&#39;s phone override, letting the SIS value show through again. |
| [**RemoveEnrollmentContactStudent**](EnrollmentAdminContactsApi.md#removeenrollmentcontactstudent) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students/{studentId} | Removes a student&#39;s link to a contact. |
| [**UnlockEnrollmentContactSignIn**](EnrollmentAdminContactsApi.md#unlockenrollmentcontactsignin) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/unlock | Unlocks a contact&#39;s sign-in, resetting exhausted parent-verification tries. |
| [**UpdateEnrollmentContact**](EnrollmentAdminContactsApi.md#updateenrollmentcontact) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Updates an Enrollment Contact&#39;s name. |
| [**UpdateEnrollmentContactStudent**](EnrollmentAdminContactsApi.md#updateenrollmentcontactstudent) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/students/{studentId} | Updates a contact-student association&#39;s attributes. |
| [**VerifyEnrollmentContact**](EnrollmentAdminContactsApi.md#verifyenrollmentcontact) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/verify | Verifies a contact. |

<a id="addenrollmentcontactstudent"></a>
# **AddEnrollmentContactStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto AddEnrollmentContactStudent (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto = null)

Links a student to a contact.

Send `studentId` (the SIS code) to resolve or create the linked EnrollmentStudent  document server-side, or `id` (an existing student's own internal id, as returned by  this same route's GET) to link that exact student directly - `id` wins if both are  given, and never creates anything, 404ing instead if it does not exist. Set the association  attributes (priority, relationship, etc.) with a follow-up PUT to  `.../students/{studentId}`.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminAddContactStudentRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto.md)

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
| **201** | The student was linked to the contact. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createenrollmentcontact"></a>
# **CreateEnrollmentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto CreateEnrollmentContact (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto = null)

Creates or updates an Enrollment Contact by its source-system `contactId`.

<br>              Upsert semantics: unique per `contactId`. A first call creates the contact; a later call              for the same `contactId` overwrites the SIS-sourced fields where they differ, and no-ops              when they are identical. An existing email/phone override is never touched by this call - see              the `overrides/emails` and `overrides/phones` routes for that.                <br>    `email` and `phone` here are the SIS-sourced values, which is what a contact starts              with. Changing either afterwards is an override rather than an update - see the              `overrides/emails` and `overrides/phones` routes.              


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto.md)

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
| **201** | The contact was created or updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getenrollmentcontactbyid"></a>
# **GetEnrollmentContactById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto GetEnrollmentContactById (string tenantId, Guid id)

Gets an Enrollment Contact by its record id, with its linked students.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDto.md)

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

<a id="getenrollmentcontactchangelogs"></a>
# **GetEnrollmentContactChangelogs**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel GetEnrollmentContactChangelogs (string tenantId, Guid id, int pageSize = null, int pageIndex = null, string studentId = null)

Reads every lifecycle event for a contact - create, update, delete, overrides and sign-in  unlocks - newest first.

<br>              Eventually consistent, on the same terms as M:EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.EnrollmentAdminController.GetEnrollmentContactOverrides(System.String,System.Guid,System.Int32,System.Int32,System.String,System.Threading.CancellationToken).                <br>    `EventType` on `GetAllChangesRequest` is a single optional string, so it cannot              express \"any of these event types\" on its own. The filter is built through `Filter`              instead - a raw Elasticsearch `query_string` - while `EntityType` and              `EntityId` stay the typed fields M:EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.EnrollmentAdminController.GetEnrollmentContactOverrides(System.String,System.Guid,System.Int32,System.Int32,System.String,System.Threading.CancellationToken) already uses.              The change log applies the typed fields as `filter` clauses and `Filter` as a              `must` clause on the same bool query, so the two combine as an AND: this call still never              leaves this contact's own entity scope.                <br>              The event types covered are EdGraph.HttpAggregators.Tenant.Api.Controllers.v1.ViewModels.Responses.EnrollmentAdmin.ContactOverrideHistoryExtensions.ContactEventTypes,              which tracks what the Enrollment outbox publishes against a contact.              


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 20] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **studentId** | **string** | Narrows to changes affecting one linked student. | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel.md)

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
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getenrollmentcontactoverrides"></a>
# **GetEnrollmentContactOverrides**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel GetEnrollmentContactOverrides (string tenantId, Guid id, int pageSize = null, int pageIndex = null, string studentId = null)

Reads a contact's override history, newest first.

<br>              Eventually consistent. A change reaches the log through Enrollment's outbox, so an entry can              be a few seconds behind a write that has already succeeded. Render the current value from the              contact itself and use this for what preceded it.                <br>              One route for both details, unlike the writes: this is a single ordered log and each entry              names its own detail, so splitting it would mean two requests to render one contact's              timeline and two page counts to reconcile.              


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 20] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **studentId** | **string** | Narrows to changes affecting one linked student. | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideHistoryEntryDtoPaginatedItemsViewModel.md)

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
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getenrollmentcontactregistrations"></a>
# **GetEnrollmentContactRegistrations**
> List&lt;EnrollmentApiEnrollmentRegistrationsV1RegistrationResponse&gt; GetEnrollmentContactRegistrations (string tenantId, Guid id)

Gets a contact's Registrations.


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

<a id="getenrollmentcontactstudents"></a>
# **GetEnrollmentContactStudents**
> List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto&gt; GetEnrollmentContactStudents (string tenantId, Guid id)

Gets a contact's linked students, with each link's association attributes.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**List&lt;EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto&gt;**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentDetailDto.md)

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

<a id="getenrollmentcontacts"></a>
# **GetEnrollmentContacts**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel GetEnrollmentContacts (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, string search = null, string nextSchoolStateShortCode = null, bool locked = null)

Searches Enrollment Contacts.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 50] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **search** | **string** | Free-text match on contact name, email, or phone. | [optional] [default to &quot;&quot;] |
| **nextSchoolStateShortCode** | **string** | Narrows to contacts with at least one linked student whose next school has this state short code. | [optional] [default to &quot;&quot;] |
| **locked** | **bool** | Narrows to contacts by sign-in lock status. Unset returns every contact. | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel.md)

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

<a id="overrideenrollmentcontactemail"></a>
# **OverrideEnrollmentContactEmail**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto OverrideEnrollmentContactEmail (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto = null)

Overrides a contact's email address.

The override is an enrollment-local annotation over SIS data, not a writeback. The SIS value  is kept and returned alongside it, and the correction keeps winning over later SIS imports  until staff revisit it.  <br>  The corrected value is shared by every student linked to the contact. `studentId` in the  body only records whose screen the edit came from.  


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactEmailOverrideRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto.md)

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
| **200** | The override was applied. |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="overrideenrollmentcontactphone"></a>
# **OverrideEnrollmentContactPhone**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto OverrideEnrollmentContactPhone (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto = null)

Overrides a contact's phone number.

The override is an enrollment-local annotation over SIS data, not a writeback. The SIS value  is kept and returned alongside it, and the correction keeps winning over later SIS imports  until staff revisit it.  <br>  The corrected value is shared by every student linked to the contact. `studentId` in the  body only records whose screen the edit came from.  


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactPhoneOverrideRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto.md)

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
| **200** | The override was applied. |  -  |
| **400** | Bad Request |  -  |
| **404** | Not Found |  -  |
| **412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removeenrollmentcontactemailoverride"></a>
# **RemoveEnrollmentContactEmailOverride**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto RemoveEnrollmentContactEmailOverride (string tenantId, Guid id, string studentLocalCode = null, string expectedVersion = null)

Removes a contact's email override, letting the SIS value show through again.

The removal is itself recorded in the history - the superseded value stays recoverable.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **studentLocalCode** | **string** | The local code of the student whose screen the removal was made from. | [optional] [default to &quot;&quot;] |
| **expectedVersion** | **string** | The &#x60;lastUpdatedDateTime&#x60; this edit started from. | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto.md)

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
| **200** | The override was removed, or there was none to remove. |  -  |
| **404** | Not Found |  -  |
| **412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removeenrollmentcontactphoneoverride"></a>
# **RemoveEnrollmentContactPhoneOverride**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto RemoveEnrollmentContactPhoneOverride (string tenantId, Guid id, string studentLocalCode = null, string expectedVersion = null)

Removes a contact's phone override, letting the SIS value show through again.

The removal is itself recorded in the history - the superseded value stays recoverable.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **studentLocalCode** | **string** | The local code of the student whose screen the removal was made from. | [optional] [default to &quot;&quot;] |
| **expectedVersion** | **string** | The &#x60;lastUpdatedDateTime&#x60; this edit started from. | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto.md)

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
| **200** | The override was removed, or there was none to remove. |  -  |
| **404** | Not Found |  -  |
| **412** | The contact changed while it was being edited; the write was refused. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removeenrollmentcontactstudent"></a>
# **RemoveEnrollmentContactStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentRemovedResultDto RemoveEnrollmentContactStudent (string tenantId, Guid id, string studentId)

Removes a student's link to a contact.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **studentId** | **string** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentRemovedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentRemovedResultDto.md)

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

<a id="unlockenrollmentcontactsignin"></a>
# **UnlockEnrollmentContactSignIn**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactSignInUnlockedResultDto UnlockEnrollmentContactSignIn (string tenantId, Guid id)

Unlocks a contact's sign-in, resetting exhausted parent-verification tries.

Idempotent: unlocking an already-unlocked contact, or one with no rows at all, is a 200 with  `resetCount: 0`, not an error.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactSignInUnlockedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactSignInUnlockedResultDto.md)

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
| **200** | The contact&#39;s sign-in was unlocked, or there was nothing to unlock. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateenrollmentcontact"></a>
# **UpdateEnrollmentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto UpdateEnrollmentContact (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto = null)

Updates an Enrollment Contact's name.

Email and phone cannot be changed here. Correcting either is an override, which records who  changed it and keeps the SIS value beside the correction; a body carrying `email` or  `phone` is rejected with a 400 naming the route to use instead. Note that a contact whose  email is overridden keeps that override across this call - an update to the name leaves a  standing correction alone. Student association is managed exclusively through the  `/contacts/{id}/students` sub-resource, not through this call.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto.md)

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
| **200** | The contact was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateenrollmentcontactstudent"></a>
# **UpdateEnrollmentContactStudent**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto UpdateEnrollmentContactStudent (string tenantId, Guid id, string studentId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto = null)

Updates a contact-student association's attributes.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **studentId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateContactStudentRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactStudentAssociatedResultDto.md)

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

<a id="verifyenrollmentcontact"></a>
# **VerifyEnrollmentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactVerifiedResultDto VerifyEnrollmentContact (string tenantId, Guid id)

Verifies a contact.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactVerifiedResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactVerifiedResultDto.md)

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
| **200** | The contact was verified. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

