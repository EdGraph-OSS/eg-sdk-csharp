# EdGraph.Platform.Client.Api.CategoriesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddCategoryDataSteward**](CategoriesApi.md#addcategorydatasteward) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards | Adds a Data Steward to a Category. |
| [**AddCategoryDataStewardBulk**](CategoriesApi.md#addcategorydatastewardbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/stewards | Adds a Data Steward to Categories. |
| [**CertifyCategory**](CategoriesApi.md#certifycategory) | **POST** /tenants/{tenantId}/statereporting/categories/{categoryId}/certify | Certifies a Category. |
| [**GetDataUsersBulk**](CategoriesApi.md#getdatausersbulk) | **GET** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/datausers | Get all Data Users |
| [**GetStateReportingCategories**](CategoriesApi.md#getstatereportingcategories) | **GET** /tenants/{tenantId}/statereporting/categories | Retrieves a list of Categories. |
| [**RemoveCategoryDataOwner**](CategoriesApi.md#removecategorydataowner) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Removes the Data Owner of a Category. |
| [**RemoveCategoryDataSteward**](CategoriesApi.md#removecategorydatasteward) | **DELETE** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/stewards/{email} | Removes a Data Steward from a Category. |
| [**RequestCategoryCertificationReminder**](CategoriesApi.md#requestcategorycertificationreminder) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/certificationreminder | Requests a Certification Reminder to be sent. |
| [**SetCategoryDataOwner**](CategoriesApi.md#setcategorydataowner) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/{categoryId}/owner | Sets the Data Owner of a Category. |
| [**SetCategoryDataOwnerBulk**](CategoriesApi.md#setcategorydataownerbulk) | **POST** /tenants/{tenantId}/statereporting/reportingperiods/{reportingPeriodId}/categories/owner | Sets the Data Owner of Categories. |
| [**UploadStateReportingCategory**](CategoriesApi.md#uploadstatereportingcategory) | **POST** /tenants/{tenantId}/statereporting/categories/upload | Upload a Category via a JSON file. |
| [**UploadStateReportingPeriodsFromCategoryJson**](CategoriesApi.md#uploadstatereportingperiodsfromcategoryjson) | **POST** /tenants/{tenantId}/statereporting/environments/{environmentId}/reportingperiods/upload | Upload a Category via a JSON file. |

<a id="addcategorydatasteward"></a>
# **AddCategoryDataSteward**
> ValidationsApiContainersV1DataStewardAddedResponse AddCategoryDataSteward (Guid tenantId, Guid categoryId, Guid reportingPeriodId, ValidationsApiContainersV1AddDataStewardRequest validationsApiContainersV1AddDataStewardRequest = null)

Adds a Data Steward to a Category.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1AddDataStewardRequest** | [**ValidationsApiContainersV1AddDataStewardRequest**](ValidationsApiContainersV1AddDataStewardRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataStewardAddedResponse**](ValidationsApiContainersV1DataStewardAddedResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addcategorydatastewardbulk"></a>
# **AddCategoryDataStewardBulk**
> ValidationsApiContainersV1DataStewardAddedBulkResponse AddCategoryDataStewardBulk (Guid tenantId, Guid reportingPeriodId, ValidationsApiContainersV1AddDataStewardBulkRequest validationsApiContainersV1AddDataStewardBulkRequest = null)

Adds a Data Steward to Categories.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1AddDataStewardBulkRequest** | [**ValidationsApiContainersV1AddDataStewardBulkRequest**](ValidationsApiContainersV1AddDataStewardBulkRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataStewardAddedBulkResponse**](ValidationsApiContainersV1DataStewardAddedBulkResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="certifycategory"></a>
# **CertifyCategory**
> ValidationsApiContainersV1CertificationStatusSetResponse CertifyCategory (Guid tenantId, Guid categoryId)

Certifies a Category.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

### Return type

[**ValidationsApiContainersV1CertificationStatusSetResponse**](ValidationsApiContainersV1CertificationStatusSetResponse.md)

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

<a id="getdatausersbulk"></a>
# **GetDataUsersBulk**
> ValidationsApiContainersV1CategoriesWithDataUsersResponse GetDataUsersBulk (Guid tenantId, Guid reportingPeriodId)

Get all Data Users


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |

### Return type

[**ValidationsApiContainersV1CategoriesWithDataUsersResponse**](ValidationsApiContainersV1CategoriesWithDataUsersResponse.md)

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

<a id="getstatereportingcategories"></a>
# **GetStateReportingCategories**
> ValidationsApiContainersV1PaginatedContainers GetStateReportingCategories (Guid tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Categories.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**ValidationsApiContainersV1PaginatedContainers**](ValidationsApiContainersV1PaginatedContainers.md)

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

<a id="removecategorydataowner"></a>
# **RemoveCategoryDataOwner**
> void RemoveCategoryDataOwner (Guid tenantId, Guid reportingPeriodId, Guid categoryId)

Removes the Data Owner of a Category.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

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
| **204** | The resource was successfully deleted. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="removecategorydatasteward"></a>
# **RemoveCategoryDataSteward**
> void RemoveCategoryDataSteward (Guid tenantId, Guid categoryId, Guid reportingPeriodId, string email)

Removes a Data Steward from a Category.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **email** | **string** |  |  |

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
| **204** | The resource was successfully deleted. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="requestcategorycertificationreminder"></a>
# **RequestCategoryCertificationReminder**
> ValidationsApiContainersV1CertificationReminderRequestedResponse RequestCategoryCertificationReminder (Guid tenantId, Guid reportingPeriodId, Guid categoryId)

Requests a Certification Reminder to be sent.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |

### Return type

[**ValidationsApiContainersV1CertificationReminderRequestedResponse**](ValidationsApiContainersV1CertificationReminderRequestedResponse.md)

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

<a id="setcategorydataowner"></a>
# **SetCategoryDataOwner**
> ValidationsApiContainersV1DataOwnerSetResponse SetCategoryDataOwner (Guid tenantId, Guid categoryId, Guid reportingPeriodId, ValidationsApiContainersV1SetDataOwnerRequest validationsApiContainersV1SetDataOwnerRequest = null)

Sets the Data Owner of a Category.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **categoryId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1SetDataOwnerRequest** | [**ValidationsApiContainersV1SetDataOwnerRequest**](ValidationsApiContainersV1SetDataOwnerRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataOwnerSetResponse**](ValidationsApiContainersV1DataOwnerSetResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setcategorydataownerbulk"></a>
# **SetCategoryDataOwnerBulk**
> ValidationsApiContainersV1DataOwnerSetBulkResponse SetCategoryDataOwnerBulk (Guid tenantId, Guid reportingPeriodId, ValidationsApiContainersV1SetDataOwnerBulkRequest validationsApiContainersV1SetDataOwnerBulkRequest = null)

Sets the Data Owner of Categories.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **reportingPeriodId** | **Guid** |  |  |
| **validationsApiContainersV1SetDataOwnerBulkRequest** | [**ValidationsApiContainersV1SetDataOwnerBulkRequest**](ValidationsApiContainersV1SetDataOwnerBulkRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1DataOwnerSetBulkResponse**](ValidationsApiContainersV1DataOwnerSetBulkResponse.md)

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
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="uploadstatereportingcategory"></a>
# **UploadStateReportingCategory**
> ValidationsApiContainersV1CollectionUploadedResponse UploadStateReportingCategory (Guid tenantId, string contentType = null, string contentDisposition = null, Dictionary<string, List<string>> headers = null, long length = null, string name = null, string fileName = null)

Upload a Category via a JSON file.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **contentType** | **string** |  | [optional]  |
| **contentDisposition** | **string** |  | [optional]  |
| **headers** | [**Dictionary&lt;string, List&lt;string&gt;&gt;**](Dictionary.md) |  | [optional]  |
| **length** | **long** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **fileName** | **string** |  | [optional]  |

### Return type

[**ValidationsApiContainersV1CollectionUploadedResponse**](ValidationsApiContainersV1CollectionUploadedResponse.md)

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
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="uploadstatereportingperiodsfromcategoryjson"></a>
# **UploadStateReportingPeriodsFromCategoryJson**
> ValidationsApiContainersV1CollectionUploadedResponse UploadStateReportingPeriodsFromCategoryJson (Guid tenantId, Guid environmentId, string contentType = null, string contentDisposition = null, Dictionary<string, List<string>> headers = null, long length = null, string name = null, string fileName = null)

Upload a Category via a JSON file.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **environmentId** | **Guid** |  |  |
| **contentType** | **string** |  | [optional]  |
| **contentDisposition** | **string** |  | [optional]  |
| **headers** | [**Dictionary&lt;string, List&lt;string&gt;&gt;**](Dictionary.md) |  | [optional]  |
| **length** | **long** |  | [optional]  |
| **name** | **string** |  | [optional]  |
| **fileName** | **string** |  | [optional]  |

### Return type

[**ValidationsApiContainersV1CollectionUploadedResponse**](ValidationsApiContainersV1CollectionUploadedResponse.md)

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
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

