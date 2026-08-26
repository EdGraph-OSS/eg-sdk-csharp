# EdGraph.Platform.Client.Api.EnrollmentAdminStudentsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetEnrollmentStudent**](EnrollmentAdminStudentsApi.md#getenrollmentstudent) | **GET** /tenants/{tenantId}/enrollmentadmin/students/{studentId} | Gets an Enrollment Student. |
| [**GetEnrollmentStudents**](EnrollmentAdminStudentsApi.md#getenrollmentstudents) | **GET** /tenants/{tenantId}/enrollmentadmin/students | Searches Enrollment Students. |

<a id="getenrollmentstudent"></a>
# **GetEnrollmentStudent**
> EnrollmentApiEnrollmentStudentsV1StudentResponse GetEnrollmentStudent (string tenantId, string studentId)

Gets an Enrollment Student.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **studentId** | **string** |  |  |

### Return type

[**EnrollmentApiEnrollmentStudentsV1StudentResponse**](EnrollmentApiEnrollmentStudentsV1StudentResponse.md)

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

<a id="getenrollmentstudents"></a>
# **GetEnrollmentStudents**
> EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse GetEnrollmentStudents (string tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Searches Enrollment Students.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

### Return type

[**EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse**](EnrollmentApiEnrollmentStudentsV1StudentsSearchResponse.md)

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

