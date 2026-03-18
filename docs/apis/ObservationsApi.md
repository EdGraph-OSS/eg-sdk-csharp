# EdGraph.Platform.Client.Api.ObservationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateObservation**](ObservationsApi.md#createobservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant |
| [**DeleteObservation**](ObservationsApi.md#deleteobservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant |
| [**GetObservationById**](ObservationsApi.md#getobservationbyid) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant |
| [**GetPaginatedAvailableCampuses**](ObservationsApi.md#getpaginatedavailablecampuses) | **GET** /tenants/{tenantId}/observations/campuses | Get Available Campuses |
| [**GetPaginatedAvailableForms**](ObservationsApi.md#getpaginatedavailableforms) | **GET** /tenants/{tenantId}/observations/forms/available | Get Paginated Available Forms |
| [**GetPaginatedEvaluees**](ObservationsApi.md#getpaginatedevaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Get paginated evaluees |
| [**GetPaginatedObservations**](ObservationsApi.md#getpaginatedobservations) | **GET** /tenants/{tenantId}/observations | Get Paginated Observations for a given tenant |
| [**GetSubmittedObservationsCount**](ObservationsApi.md#getsubmittedobservationscount) | **GET** /tenants/{tenantId}/submittedobservations | Get submitted Observations count |

<a id="createobservation"></a>
# **CreateObservation**
> EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse CreateObservation (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest = null)

Creates a new Observation for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateObservationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest = new EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest(); // EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest |  (optional) 

            try
            {
                // Creates a new Observation for a given tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse result = apiInstance.CreateObservation(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.CreateObservation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateObservationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Observation for a given tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationResponse> response = apiInstance.CreateObservationWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsCreateObservationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.CreateObservationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="deleteobservation"></a>
# **DeleteObservation**
> EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse DeleteObservation (Guid tenantId, Guid observationId)

Deletes an Observation for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteObservationExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var observationId = "observationId_example";  // Guid | 

            try
            {
                // Deletes an Observation for a given tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse result = apiInstance.DeleteObservation(tenantId, observationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.DeleteObservation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteObservationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an Observation for a given tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsDeleteObservationResponse> response = apiInstance.DeleteObservationWithHttpInfo(tenantId, observationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.DeleteObservationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="getobservationbyid"></a>
# **GetObservationById**
> EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse GetObservationById (Guid tenantId, Guid observationId)

Get an Observation for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetObservationByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var observationId = "observationId_example";  // Guid | 

            try
            {
                // Get an Observation for a given tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse result = apiInstance.GetObservationById(tenantId, observationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetObservationById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetObservationByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an Observation for a given tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponse> response = apiInstance.GetObservationByIdWithHttpInfo(tenantId, observationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetObservationByIdWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

<a id="getpaginatedavailablecampuses"></a>
# **GetPaginatedAvailableCampuses**
> EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse GetPaginatedAvailableCampuses (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null)

Get Available Campuses

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedAvailableCampusesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get Available Campuses
                EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse result = apiInstance.GetPaginatedAvailableCampuses(tenantId, pageSize, pageIndex, orderBy);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetPaginatedAvailableCampuses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedAvailableCampusesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Available Campuses
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsCampusResponseGetPaginatedItemsResponse> response = apiInstance.GetPaginatedAvailableCampusesWithHttpInfo(tenantId, pageSize, pageIndex, orderBy);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetPaginatedAvailableCampusesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |

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
> EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse GetPaginatedAvailableForms (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Get Paginated Available Forms

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedAvailableFormsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get Paginated Available Forms
                EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse result = apiInstance.GetPaginatedAvailableForms(tenantId, pageIndex, pageSize, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetPaginatedAvailableForms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedAvailableFormsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Paginated Available Forms
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse> response = apiInstance.GetPaginatedAvailableFormsWithHttpInfo(tenantId, pageIndex, pageSize, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetPaginatedAvailableFormsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse.md)

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
> EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse GetPaginatedEvaluees (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string campus = null, string evalueeId = null)

Get paginated evaluees

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedEvalueesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var campus = "\"\"";  // string |  (optional)  (default to "")
            var evalueeId = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get paginated evaluees
                EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse result = apiInstance.GetPaginatedEvaluees(tenantId, pageSize, pageIndex, orderBy, campus, evalueeId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetPaginatedEvaluees: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedEvalueesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get paginated evaluees
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsEvalueeResponseGetPaginatedItemsResponse> response = apiInstance.GetPaginatedEvalueesWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, campus, evalueeId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetPaginatedEvalueesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **campus** | **string** |  | [optional] [default to &quot;&quot;] |
| **evalueeId** | **string** |  | [optional] [default to &quot;&quot;] |

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedObservationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var campus = "\"\"";  // string |  (optional)  (default to "")
            var evalueeName = "\"\"";  // string |  (optional)  (default to "")
            var evalueeId = "\"\"";  // string |  (optional)  (default to "")
            var formId = "\"\"";  // string |  (optional)  (default to "")
            var status = "\"\"";  // string |  (optional)  (default to "")
            var from = "\"\"";  // string |  (optional)  (default to "")
            var to = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get Paginated Observations for a given tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel result = apiInstance.GetPaginatedObservations(tenantId, pageSize, pageIndex, orderBy, campus, evalueeName, evalueeId, formId, status, from, to);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetPaginatedObservations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedObservationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Paginated Observations for a given tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsObservationProfileResponsePaginatedItemsViewModel> response = apiInstance.GetPaginatedObservationsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, campus, evalueeName, evalueeId, formId, status, from, to);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetPaginatedObservationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetSubmittedObservationsCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var evalueeId = "evalueeId_example";  // string |  (optional) 
            var campus = "campus_example";  // string |  (optional) 

            try
            {
                // Get submitted Observations count
                EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse result = apiInstance.GetSubmittedObservationsCount(tenantId, evalueeId, campus);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetSubmittedObservationsCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetSubmittedObservationsCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get submitted Observations count
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsGetSubmittedObservationsCountResponse> response = apiInstance.GetSubmittedObservationsCountWithHttpInfo(tenantId, evalueeId, campus);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetSubmittedObservationsCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

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

