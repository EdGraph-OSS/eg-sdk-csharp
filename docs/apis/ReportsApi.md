# EdGraph.Platform.Client.Api.ReportsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateReportAsync**](ReportsApi.md#createreportasync) | **POST** /tenants/{tenantId}/analytics/reports | Creates a new report (Does not upload pbix file). |
| [**DeleteReportAsync**](ReportsApi.md#deletereportasync) | **DELETE** /tenants/{tenantId}/analytics/reports/{reportId} | Removes a report. |
| [**DownloadReportAsync**](ReportsApi.md#downloadreportasync) | **GET** /tenants/{tenantId}/analytics/reports/download/{reportId}/{groupId} | Retrieves the PBIX for any report in the list in order to download |
| [**GetAllTenantAnalyticsWorkspaceReportsAsync**](ReportsApi.md#getalltenantanalyticsworkspacereportsasync) | **GET** /tenants/{tenantId}/analytics/reports | Retrieves all reports. |
| [**GetReportByIdAsync**](ReportsApi.md#getreportbyidasync) | **GET** /tenants/{tenantId}/analytics/reports/{reportId} | Retrieves a Report by ID. |
| [**SyncLatestVersion**](ReportsApi.md#synclatestversion) | **POST** /tenants/{tenantId}/analytics/reports/synclatestversion | Sync latest version |
| [**SyncWorkspacesAsync**](ReportsApi.md#syncworkspacesasync) | **POST** /tenants/{tenantId}/analytics/reports/sync | Triggers workspace, ODS and DW automation. |
| [**UpdateReportAsync**](ReportsApi.md#updatereportasync) | **PUT** /tenants/{tenantId}/analytics/reports/{reportId} | Updates a report. |

<a id="createreportasync"></a>
# **CreateReportAsync**
> AnalyticsApiReportsV1ReportIdResponse CreateReportAsync (string tenantId, System.IO.Stream file = null, string name = null, string shortDescription = null, string description = null, string tags = null, bool isVisible = null, string version = null, bool identityRequired = null, bool rolesRequired = null, string state = null)

Creates a new report (Does not upload pbix file).


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **file** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **shortDescription** | **string** |  | [optional]  |
| **description** | **string** |  | [optional]  |
| **tags** | **string** |  | [optional]  |
| **isVisible** | **bool** |  | [optional]  |
| **version** | **string** |  | [optional]  |
| **identityRequired** | **bool** |  | [optional]  |
| **rolesRequired** | **bool** |  | [optional]  |
| **state** | **string** |  | [optional]  |

### Return type

[**AnalyticsApiReportsV1ReportIdResponse**](AnalyticsApiReportsV1ReportIdResponse.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletereportasync"></a>
# **DeleteReportAsync**
> void DeleteReportAsync (string tenantId, string reportId)

Removes a report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |

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
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="downloadreportasync"></a>
# **DownloadReportAsync**
> AnalyticsApiReportsV1DownloadReportResponse DownloadReportAsync (string tenantId, string reportId, string groupId)

Retrieves the PBIX for any report in the list in order to download


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |
| **groupId** | **string** |  |  |

### Return type

[**AnalyticsApiReportsV1DownloadReportResponse**](AnalyticsApiReportsV1DownloadReportResponse.md)

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

<a id="getalltenantanalyticsworkspacereportsasync"></a>
# **GetAllTenantAnalyticsWorkspaceReportsAsync**
> AnalyticsApiReportsV1ReportPaginatedItemsResponse GetAllTenantAnalyticsWorkspaceReportsAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves all reports.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**AnalyticsApiReportsV1ReportPaginatedItemsResponse**](AnalyticsApiReportsV1ReportPaginatedItemsResponse.md)

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

<a id="getreportbyidasync"></a>
# **GetReportByIdAsync**
> AnalyticsApiReportsV1ReportResponse GetReportByIdAsync (string tenantId, string reportId)

Retrieves a Report by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="synclatestversion"></a>
# **SyncLatestVersion**
> Object SyncLatestVersion (string tenantId, AnalyticsApiReportsV1SyncLatestVersionRequest analyticsApiReportsV1SyncLatestVersionRequest = null)

Sync latest version


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiReportsV1SyncLatestVersionRequest** | [**AnalyticsApiReportsV1SyncLatestVersionRequest**](AnalyticsApiReportsV1SyncLatestVersionRequest.md) |  | [optional]  |

### Return type

**Object**

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="syncworkspacesasync"></a>
# **SyncWorkspacesAsync**
> Object SyncWorkspacesAsync (string tenantId, AnalyticsApiReportsV1SyncWorkspacesRequest analyticsApiReportsV1SyncWorkspacesRequest = null)

Triggers workspace, ODS and DW automation.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **analyticsApiReportsV1SyncWorkspacesRequest** | [**AnalyticsApiReportsV1SyncWorkspacesRequest**](AnalyticsApiReportsV1SyncWorkspacesRequest.md) |  | [optional]  |

### Return type

**Object**

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
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="updatereportasync"></a>
# **UpdateReportAsync**
> AnalyticsApiReportsV1AnalyticsReport UpdateReportAsync (string tenantId, string reportId, System.IO.Stream file = null, string id = null, string name = null, string shortDescription = null, string description = null, string tags = null, bool isVisible = null, string version = null, bool rolesRequired = null, bool identityRequired = null, string state = null)

Updates a report.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **reportId** | **string** |  |  |
| **file** | **System.IO.Stream****System.IO.Stream** |  | [optional]  |
| **id** | **string** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **shortDescription** | **string** |  | [optional]  |
| **description** | **string** |  | [optional]  |
| **tags** | **string** |  | [optional]  |
| **isVisible** | **bool** |  | [optional]  |
| **version** | **string** |  | [optional]  |
| **rolesRequired** | **bool** |  | [optional]  |
| **identityRequired** | **bool** |  | [optional]  |
| **state** | **string** |  | [optional]  |

### Return type

[**AnalyticsApiReportsV1AnalyticsReport**](AnalyticsApiReportsV1AnalyticsReport.md)

### Authorization

[oauth2](../README.md#oauth2)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **401** | Unauthorized. The request requires authentication. The OAuth bearer token was either not provided or is invalid. The operation may succeed once authentication has been successfully completed. |  -  |
| **403** | Forbidden. The request cannot be completed in the current authorization context. Contact your administrator if you believe this operation should be allowed. |  -  |
| **500** | An unhandled error occurred on the server.See the response body for details. |  -  |
| **200** | The requested resource was successfully retrieved. |  -  |
| **404** | Not Found |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

