# EdGraph.Platform.Client.Api.EnrollmentAdminProgramsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateProgramCatalogEntry**](EnrollmentAdminProgramsApi.md#createprogramcatalogentry) | **POST** /tenants/{tenantId}/enrollmentadmin/programs/catalog-entries | Creates a district catalog entry - a program the district defines once, which schools may  then be offered at. No school-identifying field; use POST .../programs/school-programs to  offer it at a school. |
| [**CreateSchoolProgram**](EnrollmentAdminProgramsApi.md#createschoolprogram) | **POST** /tenants/{tenantId}/enrollmentadmin/programs/school-programs | Creates a school program - either adding an existing district catalog entry to a school  (a \&quot;school association\&quot;, when &#x60;programCatalogEntryId&#x60; is set) or creating a brand new  school-specific program (when it is not). |
| [**DeleteProgramCatalogEntry**](EnrollmentAdminProgramsApi.md#deleteprogramcatalogentry) | **DELETE** /tenants/{tenantId}/enrollmentadmin/programs/catalog-entries/{id} | Removes a district catalog entry. |
| [**DeleteSchoolProgram**](EnrollmentAdminProgramsApi.md#deleteschoolprogram) | **DELETE** /tenants/{tenantId}/enrollmentadmin/programs/school-programs/{id} | Removes a school program - the API equivalent of \&quot;remove a school association\&quot; when the  row is linked to a catalog entry, or a straightforward delete when it is school-specific. |
| [**GetProgramById**](EnrollmentAdminProgramsApi.md#getprogrambyid) | **GET** /tenants/{tenantId}/enrollmentadmin/programs/{id} | Gets a Program by its record id - a district catalog entry or a school-specific program. |
| [**GetPrograms**](EnrollmentAdminProgramsApi.md#getprograms) | **GET** /tenants/{tenantId}/enrollmentadmin/programs | Searches Programs - the union of district catalog entries and school-specific programs, in  one list distinguished by each row&#39;s Scope. |
| [**UpdateProgramCatalogEntry**](EnrollmentAdminProgramsApi.md#updateprogramcatalogentry) | **PUT** /tenants/{tenantId}/enrollmentadmin/programs/catalog-entries/{id} | Updates a district catalog entry&#39;s own fields. |
| [**UpdateSchoolProgram**](EnrollmentAdminProgramsApi.md#updateschoolprogram) | **PUT** /tenants/{tenantId}/enrollmentadmin/programs/school-programs/{id} | Updates a school program&#39;s grades/capacity/zone/coordinates, and - only when it is  school-specific - its own Code/Name/ProgramType/EligibilityCriteria/RequiredDocuments. |

<a id="createprogramcatalogentry"></a>
# **CreateProgramCatalogEntry**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto CreateProgramCatalogEntry (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto = null)

Creates a district catalog entry - a program the district defines once, which schools may  then be offered at. No school-identifying field; use POST .../programs/school-programs to  offer it at a school.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateProgramCatalogEntryRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto.md)

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
| **201** | The catalog entry was created. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createschoolprogram"></a>
# **CreateSchoolProgram**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto CreateSchoolProgram (string tenantId, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto = null)

Creates a school program - either adding an existing district catalog entry to a school  (a \"school association\", when `programCatalogEntryId` is set) or creating a brand new  school-specific program (when it is not).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminCreateSchoolProgramRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto.md)

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
| **201** | The school program was created. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteprogramcatalogentry"></a>
# **DeleteProgramCatalogEntry**
> void DeleteProgramCatalogEntry (string tenantId, Guid id)

Removes a district catalog entry.


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
| **204** | The catalog entry was removed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteschoolprogram"></a>
# **DeleteSchoolProgram**
> void DeleteSchoolProgram (string tenantId, Guid id)

Removes a school program - the API equivalent of \"remove a school association\" when the  row is linked to a catalog entry, or a straightforward delete when it is school-specific.


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
| **204** | The school program was removed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getprogrambyid"></a>
# **GetProgramById**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto GetProgramById (string tenantId, Guid id)

Gets a Program by its record id - a district catalog entry or a school-specific program.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramDetailDto.md)

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

<a id="getprograms"></a>
# **GetPrograms**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel GetPrograms (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, string search = null, string scope = null, string schoolCode = null, string programType = null)

Searches Programs - the union of district catalog entries and school-specific programs, in  one list distinguished by each row's Scope.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 50] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **search** | **string** | Free-text match on program name/code. | [optional] [default to &quot;&quot;] |
| **scope** | **string** | \&quot;DistrictCatalog\&quot;, \&quot;SchoolSpecific\&quot;, or omitted for all. | [optional] [default to &quot;&quot;] |
| **schoolCode** | **string** | Narrows to programs offered at this school. Not a security boundary. | [optional] [default to &quot;&quot;] |
| **programType** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramListItemDtoPaginatedItemsViewModel.md)

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

<a id="updateprogramcatalogentry"></a>
# **UpdateProgramCatalogEntry**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto UpdateProgramCatalogEntry (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramCatalogEntryRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramCatalogEntryRequestDto = null)

Updates a district catalog entry's own fields.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramCatalogEntryRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramCatalogEntryRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateProgramCatalogEntryRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto.md)

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
| **200** | The catalog entry was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updateschoolprogram"></a>
# **UpdateSchoolProgram**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto UpdateSchoolProgram (string tenantId, Guid id, EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto = null)

Updates a school program's grades/capacity/zone/coordinates, and - only when it is  school-specific - its own Code/Name/ProgramType/EligibilityCriteria/RequiredDocuments.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **id** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto** | [**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsRequestsEnrollmentAdminUpdateSchoolProgramRequestDto.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminProgramMutationResultDto.md)

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
| **200** | The school program was updated. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

