# EdGraph.Platform.Client.Api.InstancesReportsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GenerateReportsAsync**](InstancesReportsApi.md#generatereportsasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/generate | Queues a job to generate the report views in the ODS Database. |
| [**GetReportsStatusAsync**](InstancesReportsApi.md#getreportsstatusasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/status | Retrieves the status of the report views in Instance. |
| [**GetSchoolsByTypeReportAsync**](InstancesReportsApi.md#getschoolsbytypereportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/schoolsbytype/{localEducationAgencyId} | Retrieves a \&quot;Schools By Type\&quot; report. |
| [**GetStudentEconomicSituationReportAsync**](InstancesReportsApi.md#getstudenteconomicsituationreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentseconomicsituation/{localEducationAgencyId} | Retrieves a \&quot;Students Economic Situation\&quot; report. |
| [**GetStudentEnrollmentByEthnicityReport**](InstancesReportsApi.md#getstudentenrollmentbyethnicityreport) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/ethnicity/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Ethnicity\&quot; report. |
| [**GetStudentEnrollmentByGenderReportAsync**](InstancesReportsApi.md#getstudentenrollmentbygenderreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/gender/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Gender\&quot; report. |
| [**GetStudentEnrollmentByRaceReportAsync**](InstancesReportsApi.md#getstudentenrollmentbyracereportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentenrollment/race/{localEducationAgencyId} | Retrieves a \&quot;Student Enrollment By Race\&quot; report. |
| [**GetStudentsByProgramReportAsync**](InstancesReportsApi.md#getstudentsbyprogramreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/studentsbyprogram/{localEducationAgencyId} | Retrieves a \&quot;Students By Program\&quot; report. |
| [**GetTotalEnrollmentsReportAsync**](InstancesReportsApi.md#gettotalenrollmentsreportasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/reports/totalenrollments/{localEducationAgencyId} | Retrieves a \&quot;Total Enrollments\&quot; report. |

<a id="generatereportsasync"></a>
# **GenerateReportsAsync**
> EdfiAdminApiEdfiAdminV1GenerateReportsResponse GenerateReportsAsync (string tenantId, string instanceId)

Queues a job to generate the report views in the ODS Database.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1GenerateReportsResponse**](EdfiAdminApiEdfiAdminV1GenerateReportsResponse.md)

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

<a id="getreportsstatusasync"></a>
# **GetReportsStatusAsync**
> EdfiAdminApiEdfiAdminV1ReportsStatusResponse GetReportsStatusAsync (string tenantId, string instanceId)

Retrieves the status of the report views in Instance.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1ReportsStatusResponse**](EdfiAdminApiEdfiAdminV1ReportsStatusResponse.md)

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

<a id="getschoolsbytypereportasync"></a>
# **GetSchoolsByTypeReportAsync**
> EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse GetSchoolsByTypeReportAsync (string tenantId, string instanceId, int localEducationAgencyId)

Retrieves a \"Schools By Type\" report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **localEducationAgencyId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse**](EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse.md)

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

<a id="getstudenteconomicsituationreportasync"></a>
# **GetStudentEconomicSituationReportAsync**
> EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse GetStudentEconomicSituationReportAsync (string tenantId, string instanceId, int localEducationAgencyId)

Retrieves a \"Students Economic Situation\" report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **localEducationAgencyId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse**](EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse.md)

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

<a id="getstudentenrollmentbyethnicityreport"></a>
# **GetStudentEnrollmentByEthnicityReport**
> EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse GetStudentEnrollmentByEthnicityReport (string tenantId, string instanceId, int localEducationAgencyId)

Retrieves a \"Student Enrollment By Ethnicity\" report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **localEducationAgencyId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse**](EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse.md)

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

<a id="getstudentenrollmentbygenderreportasync"></a>
# **GetStudentEnrollmentByGenderReportAsync**
> EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse GetStudentEnrollmentByGenderReportAsync (string tenantId, string instanceId, int localEducationAgencyId)

Retrieves a \"Student Enrollment By Gender\" report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **localEducationAgencyId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse**](EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse.md)

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

<a id="getstudentenrollmentbyracereportasync"></a>
# **GetStudentEnrollmentByRaceReportAsync**
> EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse GetStudentEnrollmentByRaceReportAsync (string tenantId, string instanceId, int localEducationAgencyId)

Retrieves a \"Student Enrollment By Race\" report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **localEducationAgencyId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse**](EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse.md)

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

<a id="getstudentsbyprogramreportasync"></a>
# **GetStudentsByProgramReportAsync**
> EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse GetStudentsByProgramReportAsync (string tenantId, string instanceId, int localEducationAgencyId)

Retrieves a \"Students By Program\" report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **localEducationAgencyId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse**](EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse.md)

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

<a id="gettotalenrollmentsreportasync"></a>
# **GetTotalEnrollmentsReportAsync**
> EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse GetTotalEnrollmentsReportAsync (string tenantId, string instanceId, int localEducationAgencyId)

Retrieves a \"Total Enrollments\" report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **localEducationAgencyId** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse**](EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse.md)

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

