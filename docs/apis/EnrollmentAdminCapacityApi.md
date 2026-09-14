# EdGraph.Platform.Client.Api.EnrollmentAdminCapacityApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**GetCapacity**](EnrollmentAdminCapacityApi.md#getcapacity) | **GET** /tenants/{tenantId}/enrollmentadmin/schools/{schoolCode}/capacity | Searches Capacity for one school - one row per program x grade x school year. |

<a id="getcapacity"></a>
# **GetCapacity**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel GetCapacity (string tenantId, string schoolCode, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, string grade = null, string search = null)

Searches Capacity for one school - one row per program x grade x school year.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **schoolCode** | **string** | Required - a seat count is meaningless without a school. |  |
| **pageSize** | **int** |  | [optional] [default to 50] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **grade** | **string** | Optional exact match. | [optional] [default to &quot;&quot;] |
| **search** | **string** | Free-text match on program name/code. | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEnrollmentAdminCapacityListItemDtoPaginatedItemsViewModel.md)

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

