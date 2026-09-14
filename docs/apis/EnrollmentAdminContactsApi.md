# EdGraph.Platform.Client.Api.EnrollmentAdminContactsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateEnrollmentContact**](EnrollmentAdminContactsApi.md#createenrollmentcontact) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts | Creates an Enrollment Contact. |
| [**GetEnrollmentContactById**](EnrollmentAdminContactsApi.md#getenrollmentcontactbyid) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Gets an Enrollment Contact by its record id, with its linked students. |
| [**GetEnrollmentContactOverrides**](EnrollmentAdminContactsApi.md#getenrollmentcontactoverrides) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/overrides | Reads a contact&#39;s override history, newest first. |
| [**GetEnrollmentContacts**](EnrollmentAdminContactsApi.md#getenrollmentcontacts) | **GET** /tenants/{tenantId}/enrollmentadmin/contacts | Searches Enrollment Contacts. |
| [**OverrideEnrollmentContactEmail**](EnrollmentAdminContactsApi.md#overrideenrollmentcontactemail) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/email-override | Overrides a contact&#39;s email address. |
| [**OverrideEnrollmentContactPhone**](EnrollmentAdminContactsApi.md#overrideenrollmentcontactphone) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/phone-override | Overrides a contact&#39;s phone number. |
| [**RemoveEnrollmentContactEmailOverride**](EnrollmentAdminContactsApi.md#removeenrollmentcontactemailoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/email-override | Removes a contact&#39;s email override, letting the SIS value show through again. |
| [**RemoveEnrollmentContactPhoneOverride**](EnrollmentAdminContactsApi.md#removeenrollmentcontactphoneoverride) | **DELETE** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/phone-override | Removes a contact&#39;s phone override, letting the SIS value show through again. |
| [**UnlockEnrollmentContactSignIn**](EnrollmentAdminContactsApi.md#unlockenrollmentcontactsignin) | **POST** /tenants/{tenantId}/enrollmentadmin/contacts/{id}/unlock | Unlocks a contact&#39;s sign-in, resetting exhausted parent-verification tries. |
| [**UpdateEnrollmentContact**](EnrollmentAdminContactsApi.md#updateenrollmentcontact) | **PUT** /tenants/{tenantId}/enrollmentadmin/contacts/{id} | Updates an Enrollment Contact name and its linked students. |

<a id="createenrollmentcontact"></a>
# **CreateEnrollmentContact**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactMutationResultDto CreateEnrollmentContact (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateContactRequestDto = null)

Creates an Enrollment Contact.

`email` and `phone` here are the SIS-sourced values, which is what a contact starts              with. Changing either afterwards is an override rather than an update - see the              `email-override` and `phone-override` routes.


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
| **201** | The contact was created. |  -  |
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

<a id="getenrollmentcontacts"></a>
# **GetEnrollmentContacts**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactResponseDtoPaginatedItemsViewModel GetEnrollmentContacts (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, string search = null, string schoolCode = null, bool locked = null)

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
| **schoolCode** | **string** | Narrows to contacts with at least one linked student at this school. | [optional] [default to &quot;&quot;] |
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
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto RemoveEnrollmentContactEmailOverride (string tenantId, Guid id, string studentId = null, string expectedVersion = null)

Removes a contact's email override, letting the SIS value show through again.

The removal is itself recorded in the history - the superseded value stays recoverable.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **studentId** | **string** | The student whose screen the removal was made from. | [optional] [default to &quot;&quot;] |
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
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminContactOverrideResultDto RemoveEnrollmentContactPhoneOverride (string tenantId, Guid id, string studentId = null, string expectedVersion = null)

Removes a contact's phone override, letting the SIS value show through again.

The removal is itself recorded in the history - the superseded value stays recoverable.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **studentId** | **string** | The student whose screen the removal was made from. | [optional] [default to &quot;&quot;] |
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

Updates an Enrollment Contact name and its linked students.

<br>              The student list is REPLACED, not merged: a student omitted from the body is unlinked from the              contact.                <br>              Email and phone cannot be changed here. Correcting either is an override, which records who              changed it and keeps the SIS value beside the correction; a body carrying `email` or              `phone` is rejected with a 400 naming the route to use instead. Note that a contact whose              email is overridden keeps that override across this call - an update to the name leaves a              standing correction alone.              


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

