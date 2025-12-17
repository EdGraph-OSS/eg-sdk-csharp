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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GenerateReportsAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Queues a job to generate the report views in the ODS Database.
                EdfiAdminApiEdfiAdminV1GenerateReportsResponse result = apiInstance.GenerateReportsAsync(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GenerateReportsAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GenerateReportsAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Queues a job to generate the report views in the ODS Database.
    ApiResponse<EdfiAdminApiEdfiAdminV1GenerateReportsResponse> response = apiInstance.GenerateReportsAsyncWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GenerateReportsAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetReportsStatusAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Retrieves the status of the report views in Instance.
                EdfiAdminApiEdfiAdminV1ReportsStatusResponse result = apiInstance.GetReportsStatusAsync(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetReportsStatusAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetReportsStatusAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the status of the report views in Instance.
    ApiResponse<EdfiAdminApiEdfiAdminV1ReportsStatusResponse> response = apiInstance.GetReportsStatusAsyncWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetReportsStatusAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetSchoolsByTypeReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var localEducationAgencyId = 56;  // int | 

            try
            {
                // Retrieves a \"Schools By Type\" report.
                EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse result = apiInstance.GetSchoolsByTypeReportAsync(tenantId, instanceId, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetSchoolsByTypeReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSchoolsByTypeReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a \"Schools By Type\" report.
    ApiResponse<EdfiAdminApiEdfiAdminV1SchoolsByTypeReportResponse> response = apiInstance.GetSchoolsByTypeReportAsyncWithHttpInfo(tenantId, instanceId, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetSchoolsByTypeReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStudentEconomicSituationReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var localEducationAgencyId = 56;  // int | 

            try
            {
                // Retrieves a \"Students Economic Situation\" report.
                EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse result = apiInstance.GetStudentEconomicSituationReportAsync(tenantId, instanceId, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetStudentEconomicSituationReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStudentEconomicSituationReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a \"Students Economic Situation\" report.
    ApiResponse<EdfiAdminApiEdfiAdminV1StudentEconomicSituationReportResponse> response = apiInstance.GetStudentEconomicSituationReportAsyncWithHttpInfo(tenantId, instanceId, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetStudentEconomicSituationReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStudentEnrollmentByEthnicityReportExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var localEducationAgencyId = 56;  // int | 

            try
            {
                // Retrieves a \"Student Enrollment By Ethnicity\" report.
                EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse result = apiInstance.GetStudentEnrollmentByEthnicityReport(tenantId, instanceId, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetStudentEnrollmentByEthnicityReport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStudentEnrollmentByEthnicityReportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a \"Student Enrollment By Ethnicity\" report.
    ApiResponse<EdfiAdminApiEdfiAdminV1StudentEnrollmentByEthnicityReportResponse> response = apiInstance.GetStudentEnrollmentByEthnicityReportWithHttpInfo(tenantId, instanceId, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetStudentEnrollmentByEthnicityReportWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStudentEnrollmentByGenderReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var localEducationAgencyId = 56;  // int | 

            try
            {
                // Retrieves a \"Student Enrollment By Gender\" report.
                EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse result = apiInstance.GetStudentEnrollmentByGenderReportAsync(tenantId, instanceId, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetStudentEnrollmentByGenderReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStudentEnrollmentByGenderReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a \"Student Enrollment By Gender\" report.
    ApiResponse<EdfiAdminApiEdfiAdminV1StudentEnrollmentByGenderReportResponse> response = apiInstance.GetStudentEnrollmentByGenderReportAsyncWithHttpInfo(tenantId, instanceId, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetStudentEnrollmentByGenderReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStudentEnrollmentByRaceReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var localEducationAgencyId = 56;  // int | 

            try
            {
                // Retrieves a \"Student Enrollment By Race\" report.
                EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse result = apiInstance.GetStudentEnrollmentByRaceReportAsync(tenantId, instanceId, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetStudentEnrollmentByRaceReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStudentEnrollmentByRaceReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a \"Student Enrollment By Race\" report.
    ApiResponse<EdfiAdminApiEdfiAdminV1StudentEnrollmentByRaceReportResponse> response = apiInstance.GetStudentEnrollmentByRaceReportAsyncWithHttpInfo(tenantId, instanceId, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetStudentEnrollmentByRaceReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStudentsByProgramReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var localEducationAgencyId = 56;  // int | 

            try
            {
                // Retrieves a \"Students By Program\" report.
                EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse result = apiInstance.GetStudentsByProgramReportAsync(tenantId, instanceId, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetStudentsByProgramReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStudentsByProgramReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a \"Students By Program\" report.
    ApiResponse<EdfiAdminApiEdfiAdminV1StudentsByProgramReportResponse> response = apiInstance.GetStudentsByProgramReportAsyncWithHttpInfo(tenantId, instanceId, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetStudentsByProgramReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTotalEnrollmentsReportAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesReportsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var localEducationAgencyId = 56;  // int | 

            try
            {
                // Retrieves a \"Total Enrollments\" report.
                EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse result = apiInstance.GetTotalEnrollmentsReportAsync(tenantId, instanceId, localEducationAgencyId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesReportsApi.GetTotalEnrollmentsReportAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTotalEnrollmentsReportAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a \"Total Enrollments\" report.
    ApiResponse<EdfiAdminApiEdfiAdminV1TotalEnrollmentsReportResponse> response = apiInstance.GetTotalEnrollmentsReportAsyncWithHttpInfo(tenantId, instanceId, localEducationAgencyId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesReportsApi.GetTotalEnrollmentsReportAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

