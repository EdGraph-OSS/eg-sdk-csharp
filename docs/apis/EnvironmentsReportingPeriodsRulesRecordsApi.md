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

