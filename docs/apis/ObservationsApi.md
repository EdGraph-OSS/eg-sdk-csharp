# EdGraph.Platform.Client.Api.ObservationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateObservation**](ObservationsApi.md#createobservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant |
| [**CreateObservationSubmission**](ObservationsApi.md#createobservationsubmission) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submit | Creates a submission for an available form referencing an existing observation |
| [**DeleteObservation**](ObservationsApi.md#deleteobservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant |
| [**GetAvailableCampusesTotalEvaluees**](ObservationsApi.md#getavailablecampusestotalevaluees) | **GET** /tenants/{tenantId}/observations/total-evaluees | Get the total number of evaluees across all available campuses |
| [**GetDashboard**](ObservationsApi.md#getdashboard) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId} | Get Observation Dashboard |
| [**GetDashboardPreferences**](ObservationsApi.md#getdashboardpreferences) | **GET** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard |
| [**GetEvalueeSections**](ObservationsApi.md#getevalueesections) | **GET** /tenants/{tenantId}/observations/evaluees/{evalueeId}/sections | Gets the Sections of an evaluee. |
| [**GetFormQuestions**](ObservationsApi.md#getformquestions) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections/{sectionId}/questions | Search Questions |
| [**GetFormSections**](ObservationsApi.md#getformsections) | **GET** /tenants/{tenantId}/observations/available-forms/{formId}/sections | Search Observation Form Sections |
| [**GetObservationById**](ObservationsApi.md#getobservationbyid) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant |
| [**GetObservationDraft**](ObservationsApi.md#getobservationdraft) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Get an observation form&#39;s draft |
| [**GetObservationSubmission**](ObservationsApi.md#getobservationsubmission) | **GET** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/submission | Gets a submission for a specific observation |
| [**GetPaginatedAvailableCampuses**](ObservationsApi.md#getpaginatedavailablecampuses) | **GET** /tenants/{tenantId}/observations/campuses | Get Available Campuses |
| [**GetPaginatedAvailableForms**](ObservationsApi.md#getpaginatedavailableforms) | **GET** /tenants/{tenantId}/observations/available-forms | Get Paginated Available Forms |
| [**GetPaginatedCampusSections**](ObservationsApi.md#getpaginatedcampussections) | **GET** /tenants/{tenantId}/observations/campuses/{campusId}/sections | Retrieves a list of Sections for a given available campus. |
| [**GetPaginatedCampusesWithEvaluees**](ObservationsApi.md#getpaginatedcampuseswithevaluees) | **GET** /tenants/{tenantId}/observations/campuses-with-evaluees | Get a paginated list of the available campuses that have evaluees, each with its complete list of evaluees. |
| [**GetPaginatedEvaluees**](ObservationsApi.md#getpaginatedevaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Get paginated evaluees |
| [**GetPaginatedObservations**](ObservationsApi.md#getpaginatedobservations) | **GET** /tenants/{tenantId}/observations | Get Paginated Observations for a given tenant |
| [**GetSubmittedObservationsCount**](ObservationsApi.md#getsubmittedobservationscount) | **GET** /tenants/{tenantId}/submittedobservations | Get submitted Observations count |
| [**SaveDashboardPreferences**](ObservationsApi.md#savedashboardpreferences) | **POST** /tenants/{tenantId}/observations/dashboards/{dashboardId}/preferences | Save user preferences for a given Dashboard |
| [**SearchPaginatedEvaluees**](ObservationsApi.md#searchpaginatedevaluees) | **GET** /tenants/{tenantId}/observations/search/evaluees | Search paginated evaluees |
| [**UpdateObservation**](ObservationsApi.md#updateobservation) | **PUT** /tenants/{tenantId}/observations/{observationId} | Update an Observation for a given tenant |
| [**UpsertObservationDraft**](ObservationsApi.md#upsertobservationdraft) | **POST** /tenants/{tenantId}/observations/{observationId}/available-forms/{formId}/draft | Creates a draft for an observation forms |
| [**VerifyDashboardAccess**](ObservationsApi.md#verifydashboardaccess) | **POST** /tenants/{tenantId}/observations/dashboards/access | Verify user access to dashboards |

<a id="createobservation"></a>
# **CreateObservation**
> EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse CreateObservation (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest = null)

Creates a new Observation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse.md)

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

<a id="createobservationsubmission"></a>
# **CreateObservationSubmission**
> EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse CreateObservationSubmission (Guid tenantId, Guid formId, string observationId, EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest = null)

Creates a submission for an available form referencing an existing observation


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **observationId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationSubmissionResponse.md)

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

<a id="deleteobservation"></a>
# **DeleteObservation**
> EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse DeleteObservation (Guid tenantId, Guid observationId)

Deletes an Observation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **observationId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse.md)

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

<a id="getavailablecampusestotalevaluees"></a>
# **GetAvailableCampusesTotalEvaluees**
> EdGraphHttpAggregatorsTenantApiServicesObservationsGetAvailableCampusesTotalEvalueesResponse GetAvailableCampusesTotalEvaluees (Guid tenantId)

Get the total number of evaluees across all available campuses


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsGetAvailableCampusesTotalEvalueesResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsGetAvailableCampusesTotalEvalueesResponse.md)

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

<a id="getdashboard"></a>
# **GetDashboard**
> AnalyticsApiReportsV1ReportResponse GetDashboard (Guid tenantId, Guid dashboardId, string personaIdentifier = null)

Get Observation Dashboard


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **dashboardId** | **Guid** |  |  |
| **personaIdentifier** | **string** |  | [optional]  |

### Return type

[**AnalyticsApiReportsV1ReportResponse**](AnalyticsApiReportsV1ReportResponse.md)

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

<a id="getdashboardpreferences"></a>
# **GetDashboardPreferences**
> AnalyticsApiReportsV1ReportPreferencesResponse GetDashboardPreferences (Guid tenantId, Guid dashboardId)

Save user preferences for a given Dashboard


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **dashboardId** | **Guid** |  |  |

### Return type

[**AnalyticsApiReportsV1ReportPreferencesResponse**](AnalyticsApiReportsV1ReportPreferencesResponse.md)

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

<a id="getevalueesections"></a>
# **GetEvalueeSections**
> IdentityApiUserV1SectionResponseGetPaginatedItemsResponse GetEvalueeSections (Guid tenantId, Guid evalueeId, int pageIndex = null, int pageSize = null, string orderBy = null, string filterBy = null)

Gets the Sections of an evaluee.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evalueeId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filterBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IdentityApiUserV1SectionResponseGetPaginatedItemsResponse**](IdentityApiUserV1SectionResponseGetPaginatedItemsResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getformquestions"></a>
# **GetFormQuestions**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel GetFormQuestions (Guid tenantId, Guid formId, Guid sectionId, int pageIndex = null, int pageSize = null)

Search Questions


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **sectionId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesFormsQuestionResponseDtoPaginatedItemsViewModel.md)

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

<a id="getformsections"></a>
# **GetFormSections**
> FormApiSectionsV1SectionResponsePaginatedItemsViewModel GetFormSections (Guid tenantId, Guid formId, int pageIndex = null, int pageSize = null)

Search Observation Form Sections


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |

### Return type

[**FormApiSectionsV1SectionResponsePaginatedItemsViewModel**](FormApiSectionsV1SectionResponsePaginatedItemsViewModel.md)

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

<a id="getobservationbyid"></a>
# **GetObservationById**
> EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse GetObservationById (Guid tenantId, Guid observationId)

Get an Observation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **observationId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse.md)

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

<a id="getobservationdraft"></a>
# **GetObservationDraft**
> EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse GetObservationDraft (Guid tenantId, Guid observationId, Guid formId)

Get an observation form's draft


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **observationId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsObservationDraftResponse.md)

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

<a id="getobservationsubmission"></a>
# **GetObservationSubmission**
> EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse GetObservationSubmission (Guid tenantId, Guid observationId, Guid formId)

Gets a submission for a specific observation


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **observationId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsObservationSubmissionResponse.md)

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

<a id="getpaginatedavailablecampuses"></a>
# **GetPaginatedAvailableCampuses**
> EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse GetPaginatedAvailableCampuses (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string nameOfInstitution = null)

Get Available Campuses


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **nameOfInstitution** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse.md)

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

<a id="getpaginatedavailableforms"></a>
# **GetPaginatedAvailableForms**
> EdGraphHttpAggregatorsTenantApiServicesFormsV1FormGetPaginatedItemsResponse GetPaginatedAvailableForms (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Get Paginated Available Forms


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
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

<a id="getpaginatedcampussections"></a>
# **GetPaginatedCampusSections**
> TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse GetPaginatedCampusSections (Guid tenantId, string campusId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Retrieves a list of Sections for a given available campus.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **campusId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse**](TenantApiSectionsV1SectionListResponseGetPaginatedItemsResponse.md)

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

<a id="getpaginatedcampuseswithevaluees"></a>
# **GetPaginatedCampusesWithEvaluees**
> EdGraphHttpAggregatorsTenantApiServicesObservationsGetCampusesWithEvalueesResponse GetPaginatedCampusesWithEvaluees (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null)

Get a paginated list of the available campuses that have evaluees, each with its complete list of evaluees.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsGetCampusesWithEvalueesResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsGetCampusesWithEvalueesResponse.md)

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

<a id="getpaginatedevaluees"></a>
# **GetPaginatedEvaluees**
> EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse GetPaginatedEvaluees (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string campus = null, string evalueeId = null, string firstName = null, string lastName = null)

Get paginated evaluees


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **campus** | **string** |  | [optional] [default to &quot;&quot;] |
| **evalueeId** | **string** |  | [optional] [default to &quot;&quot;] |
| **firstName** | **string** |  | [optional] [default to &quot;&quot;] |
| **lastName** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse.md)

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

<a id="getpaginatedobservations"></a>
# **GetPaginatedObservations**
> EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel GetPaginatedObservations (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string campus = null, string evalueeName = null, string evalueeId = null, string formId = null, string status = null, string from = null, string to = null)

Get Paginated Observations for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **campus** | **string** |  | [optional] [default to &quot;&quot;] |
| **evalueeName** | **string** |  | [optional] [default to &quot;&quot;] |
| **evalueeId** | **string** |  | [optional] [default to &quot;&quot;] |
| **formId** | **string** |  | [optional] [default to &quot;&quot;] |
| **status** | **string** |  | [optional] [default to &quot;&quot;] |
| **from** | **string** |  | [optional] [default to &quot;&quot;] |
| **to** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel.md)

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

<a id="getsubmittedobservationscount"></a>
# **GetSubmittedObservationsCount**
> EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse GetSubmittedObservationsCount (Guid tenantId, string evalueeId = null, string campus = null)

Get submitted Observations count


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **evalueeId** | **string** |  | [optional]  |
| **campus** | **string** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse.md)

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

<a id="savedashboardpreferences"></a>
# **SaveDashboardPreferences**
> AnalyticsApiReportsV1ReportPreferencesSavedResponse SaveDashboardPreferences (Guid tenantId, Guid dashboardId, EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest edGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest = null)

Save user preferences for a given Dashboard


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **dashboardId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertDashboardPreferencesRequest.md) |  | [optional]  |

### Return type

[**AnalyticsApiReportsV1ReportPreferencesSavedResponse**](AnalyticsApiReportsV1ReportPreferencesSavedResponse.md)

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

<a id="searchpaginatedevaluees"></a>
# **SearchPaginatedEvaluees**
> EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel SearchPaginatedEvaluees (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string firstName = null, string lastName = null)

Search paginated evaluees


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **firstName** | **string** |  | [optional] [default to &quot;&quot;] |
| **lastName** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponsePaginatedItemsViewModel.md)

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

<a id="updateobservation"></a>
# **UpdateObservation**
> EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse UpdateObservation (Guid tenantId, Guid observationId, EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest edGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest = null)

Update an Observation for a given tenant


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **observationId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsUpdateObservationResponse.md)

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

<a id="upsertobservationdraft"></a>
# **UpsertObservationDraft**
> EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse UpsertObservationDraft (Guid tenantId, Guid observationId, Guid formId, EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest edGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest = null)

Creates a draft for an observation forms


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **observationId** | **Guid** |  |  |
| **formId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsUpsertObservationDraftResponse.md)

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

<a id="verifydashboardaccess"></a>
# **VerifyDashboardAccess**
> EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse VerifyDashboardAccess (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest edGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest = null)

Verify user access to dashboards


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsUseCasesCommandsDashboardAccessResponse.md)

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

