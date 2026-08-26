# EdGraph.Platform.Client.Api.EnrollmentAdminApplicationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetEnrollmentApplication**](EnrollmentAdminApplicationsApi.md#getenrollmentapplication) | **GET** /tenants/{tenantId}/enrollmentadmin/applications/{applicationId} | Gets an Enrollment Application. |
| [**GetEnrollmentApplications**](EnrollmentAdminApplicationsApi.md#getenrollmentapplications) | **GET** /tenants/{tenantId}/enrollmentadmin/applications | Searches Enrollment Applications. |

<a id="getenrollmentapplication"></a>
# **GetEnrollmentApplication**
> EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse GetEnrollmentApplication (string tenantId, string applicationId)

Gets an Enrollment Application.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **applicationId** | **string** |  |  |

### Return type

[**EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponseResponse.md)

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

<a id="getenrollmentapplications"></a>
# **GetEnrollmentApplications**
> EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse GetEnrollmentApplications (string tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Searches Enrollment Applications.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse**](EnrollmentApiEnrollmentApplicationResponsesV1ApplicationResponsesSearchResponse.md)

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

