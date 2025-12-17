# EdGraph.Platform.Client.Api.EnvironmentsReportingPeriodsRulesRecordsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**DeleteStateReportingPeriodRules**](EnvironmentsReportingPeriodsRulesRecordsApi.md#deletestatereportingperiodrules) | **DELETE** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules | Deletes the Rules of a Reporting Period. |
| [**SearchStateReportingPeriodRecords**](EnvironmentsReportingPeriodsRulesRecordsApi.md#searchstatereportingperiodrecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/records | Retrieves the Invalid Records of all the Rules within a Reporting Period. |
| [**SearchStateReportingPeriodRuleRecords**](EnvironmentsReportingPeriodsRulesRecordsApi.md#searchstatereportingperiodrulerecords) | **GET** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records | Retrieves the Invalid Records of a Rule. |
| [**SetStateReportingPeriodRuleRecordPostFlag**](EnvironmentsReportingPeriodsRulesRecordsApi.md#setstatereportingperiodrulerecordpostflag) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/{recordId}/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Record. |
| [**SetStateReportingPeriodRuleRecordPostFlagBulk**](EnvironmentsReportingPeriodsRulesRecordsApi.md#setstatereportingperiodrulerecordpostflagbulk) | **PUT** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/{reportingPeriodId}/rules/{ruleId}/records/excludefrompost | Toggles the \&quot;ExcludeFromPost\&quot; flag of a Rule&#39;s Invalid Records in bulk. |

<a id="deletestatereportingperiodrules"></a>
# **DeleteStateReportingPeriodRules**
> EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse DeleteStateReportingPeriodRules (Guid tenantId, Guid environmentId, Guid reportingPeriodId)

Deletes the Rules of a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteStateReportingPeriodRulesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsRulesRecordsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 

            try
            {
                // Deletes the Rules of a Reporting Period.
                EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse result = apiInstance.DeleteStateReportingPeriodRules(tenantId, environmentId, reportingPeriodId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.DeleteStateReportingPeriodRules: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteStateReportingPeriodRulesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes the Rules of a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse> response = apiInstance.DeleteStateReportingPeriodRulesWithHttpInfo(tenantId, environmentId, reportingPeriodId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.DeleteStateReportingPeriodRulesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse**](EdGraphServicesStateReportingV1ReportingPeriodRulesDeletedResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchstatereportingperiodrecords"></a>
# **SearchStateReportingPeriodRecords**
> EdGraphServicesStateReportingV1PaginatedRecords SearchStateReportingPeriodRecords (Guid tenantId, Guid environmentId, Guid reportingPeriodId, int pageIndex = null, int pageSize = null, bool excludeFromPost = null)

Retrieves the Invalid Records of all the Rules within a Reporting Period.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchStateReportingPeriodRecordsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsRulesRecordsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var pageIndex = 56;  // int |  (optional) 
            var pageSize = 56;  // int |  (optional) 
            var excludeFromPost = true;  // bool |  (optional) 

            try
            {
                // Retrieves the Invalid Records of all the Rules within a Reporting Period.
                EdGraphServicesStateReportingV1PaginatedRecords result = apiInstance.SearchStateReportingPeriodRecords(tenantId, environmentId, reportingPeriodId, pageIndex, pageSize, excludeFromPost);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SearchStateReportingPeriodRecords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchStateReportingPeriodRecordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Invalid Records of all the Rules within a Reporting Period.
    ApiResponse<EdGraphServicesStateReportingV1PaginatedRecords> response = apiInstance.SearchStateReportingPeriodRecordsWithHttpInfo(tenantId, environmentId, reportingPeriodId, pageIndex, pageSize, excludeFromPost);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SearchStateReportingPeriodRecordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |
| **excludeFromPost** | **bool** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedRecords**](EdGraphServicesStateReportingV1PaginatedRecords.md)

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

<a id="searchstatereportingperiodrulerecords"></a>
# **SearchStateReportingPeriodRuleRecords**
> EdGraphServicesStateReportingV1PaginatedRuleRecords SearchStateReportingPeriodRuleRecords (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid ruleId, int pageIndex = null, int pageSize = null)

Retrieves the Invalid Records of a Rule.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchStateReportingPeriodRuleRecordsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsRulesRecordsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var ruleId = "ruleId_example";  // Guid | 
            var pageIndex = 56;  // int |  (optional) 
            var pageSize = 56;  // int |  (optional) 

            try
            {
                // Retrieves the Invalid Records of a Rule.
                EdGraphServicesStateReportingV1PaginatedRuleRecords result = apiInstance.SearchStateReportingPeriodRuleRecords(tenantId, environmentId, reportingPeriodId, ruleId, pageIndex, pageSize);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SearchStateReportingPeriodRuleRecords: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchStateReportingPeriodRuleRecordsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Invalid Records of a Rule.
    ApiResponse<EdGraphServicesStateReportingV1PaginatedRuleRecords> response = apiInstance.SearchStateReportingPeriodRuleRecordsWithHttpInfo(tenantId, environmentId, reportingPeriodId, ruleId, pageIndex, pageSize);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SearchStateReportingPeriodRuleRecordsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **ruleId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional]  |
| **pageSize** | **int** |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1PaginatedRuleRecords**](EdGraphServicesStateReportingV1PaginatedRuleRecords.md)

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

<a id="setstatereportingperiodrulerecordpostflag"></a>
# **SetStateReportingPeriodRuleRecordPostFlag**
> EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse SetStateReportingPeriodRuleRecordPostFlag (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid ruleId, Guid recordId, EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest = null)

Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Record.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetStateReportingPeriodRuleRecordPostFlagExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsRulesRecordsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var ruleId = "ruleId_example";  // Guid | 
            var recordId = "recordId_example";  // Guid | 
            var edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest = new EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest(); // EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest |  (optional) 

            try
            {
                // Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Record.
                EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse result = apiInstance.SetStateReportingPeriodRuleRecordPostFlag(tenantId, environmentId, reportingPeriodId, ruleId, recordId, edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SetStateReportingPeriodRuleRecordPostFlag: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetStateReportingPeriodRuleRecordPostFlagWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Record.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse> response = apiInstance.SetStateReportingPeriodRuleRecordPostFlagWithHttpInfo(tenantId, environmentId, reportingPeriodId, ruleId, recordId, edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SetStateReportingPeriodRuleRecordPostFlagWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **ruleId** | **Guid** |  |  |
| **recordId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest** | [**EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest**](EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setstatereportingperiodrulerecordpostflagbulk"></a>
# **SetStateReportingPeriodRuleRecordPostFlagBulk**
> EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse SetStateReportingPeriodRuleRecordPostFlagBulk (Guid tenantId, Guid environmentId, Guid reportingPeriodId, Guid ruleId, EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest = null)

Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records in bulk.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetStateReportingPeriodRuleRecordPostFlagBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new EnvironmentsReportingPeriodsRulesRecordsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var environmentId = "environmentId_example";  // Guid | 
            var reportingPeriodId = "reportingPeriodId_example";  // Guid | 
            var ruleId = "ruleId_example";  // Guid | 
            var edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest = new EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest(); // EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest |  (optional) 

            try
            {
                // Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records in bulk.
                EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse result = apiInstance.SetStateReportingPeriodRuleRecordPostFlagBulk(tenantId, environmentId, reportingPeriodId, ruleId, edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SetStateReportingPeriodRuleRecordPostFlagBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetStateReportingPeriodRuleRecordPostFlagBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Toggles the \"ExcludeFromPost\" flag of a Rule's Invalid Records in bulk.
    ApiResponse<EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse> response = apiInstance.SetStateReportingPeriodRuleRecordPostFlagBulkWithHttpInfo(tenantId, environmentId, reportingPeriodId, ruleId, edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling EnvironmentsReportingPeriodsRulesRecordsApi.SetStateReportingPeriodRuleRecordPostFlagBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **ruleId** | **Guid** |  |  |
| **edGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest** | [**EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest**](EdGraphServicesStateReportingV1SetReportingPeriodRuleRecordPostFlagBulkRequest.md) |  | [optional]  |

### Return type

[**EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse**](EdGraphServicesStateReportingV1ReportingPeriodCreatedResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

