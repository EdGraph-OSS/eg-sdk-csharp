# EdGraph.Platform.Client.Api.ObservationsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateObservation**](ObservationsApi.md#createobservation) | **POST** /tenants/{tenantId}/observations | Creates a new Observation for a given tenant |
| [**DeleteObservation**](ObservationsApi.md#deleteobservation) | **DELETE** /tenants/{tenantId}/observations/{observationId} | Deletes an Observation for a given tenant |
| [**GetObservation**](ObservationsApi.md#getobservation) | **GET** /tenants/{tenantId}/observations/{observationId} | Get an Observation for a given tenant |
| [**GetObservationCount**](ObservationsApi.md#getobservationcount) | **GET** /tenants/{tenantId}/observations/count |  |
| [**SearchObservationCampuses**](ObservationsApi.md#searchobservationcampuses) | **GET** /tenants/{tenantId}/observations/campuses | Searches the Campuses associated with an Observation for a given Tenant. |
| [**SearchObservationEvaluees**](ObservationsApi.md#searchobservationevaluees) | **GET** /tenants/{tenantId}/observations/evaluees | Searches the Staff associated with an Observation for a given Tenant. |
| [**SearchObservationForms**](ObservationsApi.md#searchobservationforms) | **GET** /tenants/{tenantId}/observations/forms | Searches the Forms associated with an Observation for a given Tenant. |
| [**SearchObservationObservers**](ObservationsApi.md#searchobservationobservers) | **GET** /tenants/{tenantId}/observations/observers | Searches the Appraisers associated with an Observation for a given Tenant. |
| [**SearchObservations**](ObservationsApi.md#searchobservations) | **GET** /tenants/{tenantId}/observations | Searches the Observations for a given tenant |
| [**UpdateObservation**](ObservationsApi.md#updateobservation) | **PUT** /tenants/{tenantId}/observations/{observationId} | Updates an Observation for a given tenant |

<a id="createobservation"></a>
# **CreateObservation**
> EvaluationApiEvaluationsV1EvaluationCreatedResponse CreateObservation (Guid tenantId, EvaluationApiEvaluationsV1CreateEvaluationRequest evaluationApiEvaluationsV1CreateEvaluationRequest = null)

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
            var evaluationApiEvaluationsV1CreateEvaluationRequest = new EvaluationApiEvaluationsV1CreateEvaluationRequest(); // EvaluationApiEvaluationsV1CreateEvaluationRequest |  (optional) 

            try
            {
                // Creates a new Observation for a given tenant
                EvaluationApiEvaluationsV1EvaluationCreatedResponse result = apiInstance.CreateObservation(tenantId, evaluationApiEvaluationsV1CreateEvaluationRequest);
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
    ApiResponse<EvaluationApiEvaluationsV1EvaluationCreatedResponse> response = apiInstance.CreateObservationWithHttpInfo(tenantId, evaluationApiEvaluationsV1CreateEvaluationRequest);
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
| **evaluationApiEvaluationsV1CreateEvaluationRequest** | [**EvaluationApiEvaluationsV1CreateEvaluationRequest**](EvaluationApiEvaluationsV1CreateEvaluationRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationCreatedResponse**](EvaluationApiEvaluationsV1EvaluationCreatedResponse.md)

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
> EvaluationApiEvaluationsV1EvaluationDeletedResponse DeleteObservation (Guid tenantId, Guid observationId)

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
                EvaluationApiEvaluationsV1EvaluationDeletedResponse result = apiInstance.DeleteObservation(tenantId, observationId);
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
    ApiResponse<EvaluationApiEvaluationsV1EvaluationDeletedResponse> response = apiInstance.DeleteObservationWithHttpInfo(tenantId, observationId);
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

[**EvaluationApiEvaluationsV1EvaluationDeletedResponse**](EvaluationApiEvaluationsV1EvaluationDeletedResponse.md)

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

<a id="getobservation"></a>
# **GetObservation**
> EvaluationApiEvaluationsV1EvaluationResponse GetObservation (Guid tenantId, Guid observationId)

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
    public class GetObservationExample
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
                EvaluationApiEvaluationsV1EvaluationResponse result = apiInstance.GetObservation(tenantId, observationId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetObservation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetObservationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get an Observation for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationResponse> response = apiInstance.GetObservationWithHttpInfo(tenantId, observationId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetObservationWithHttpInfo: " + e.Message);
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

[**EvaluationApiEvaluationsV1EvaluationResponse**](EvaluationApiEvaluationsV1EvaluationResponse.md)

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

<a id="getobservationcount"></a>
# **GetObservationCount**
> EvaluationApiEvaluationsV1EvaluationCountResponse GetObservationCount (Guid tenantId)



### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetObservationCountExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                EvaluationApiEvaluationsV1EvaluationCountResponse result = apiInstance.GetObservationCount(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.GetObservationCount: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetObservationCountWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    ApiResponse<EvaluationApiEvaluationsV1EvaluationCountResponse> response = apiInstance.GetObservationCountWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.GetObservationCountWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationCountResponse**](EvaluationApiEvaluationsV1EvaluationCountResponse.md)

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
| **200** | Success |  -  |
| **400** | Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="searchobservationcampuses"></a>
# **SearchObservationCampuses**
> EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel SearchObservationCampuses (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Campuses associated with an Observation for a given Tenant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchObservationCampusesExample
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
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Campuses associated with an Observation for a given Tenant.
                EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel result = apiInstance.SearchObservationCampuses(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.SearchObservationCampuses: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchObservationCampusesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Campuses associated with an Observation for a given Tenant.
    ApiResponse<EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel> response = apiInstance.SearchObservationCampusesWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.SearchObservationCampusesWithHttpInfo: " + e.Message);
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
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel**](EvaluationApiEvaluationsV1CampusResponsePaginatedItemsViewModel.md)

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

<a id="searchobservationevaluees"></a>
# **SearchObservationEvaluees**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse SearchObservationEvaluees (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Staff associated with an Observation for a given Tenant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchObservationEvalueesExample
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
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Staff associated with an Observation for a given Tenant.
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse result = apiInstance.SearchObservationEvaluees(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.SearchObservationEvaluees: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchObservationEvalueesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Staff associated with an Observation for a given Tenant.
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse> response = apiInstance.SearchObservationEvalueesWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.SearchObservationEvalueesWithHttpInfo: " + e.Message);
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
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsStaffSearchedResponse.md)

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

<a id="searchobservationforms"></a>
# **SearchObservationForms**
> EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel SearchObservationForms (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Forms associated with an Observation for a given Tenant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchObservationFormsExample
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
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Forms associated with an Observation for a given Tenant.
                EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel result = apiInstance.SearchObservationForms(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.SearchObservationForms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchObservationFormsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Forms associated with an Observation for a given Tenant.
    ApiResponse<EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel> response = apiInstance.SearchObservationFormsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.SearchObservationFormsWithHttpInfo: " + e.Message);
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
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel**](EvaluationApiEvaluationsV1FormResponsePaginatedItemsViewModel.md)

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

<a id="searchobservationobservers"></a>
# **SearchObservationObservers**
> EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse SearchObservationObservers (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Appraisers associated with an Observation for a given Tenant.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchObservationObserversExample
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
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Appraisers associated with an Observation for a given Tenant.
                EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse result = apiInstance.SearchObservationObservers(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.SearchObservationObservers: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchObservationObserversWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Appraisers associated with an Observation for a given Tenant.
    ApiResponse<EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse> response = apiInstance.SearchObservationObserversWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.SearchObservationObserversWithHttpInfo: " + e.Message);
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
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse**](EdGraphHttpAggregatorsTenantApiControllersV1ViewModelsResponsesEvaluationsAppraisersSearchedResponse.md)

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

<a id="searchobservations"></a>
# **SearchObservations**
> EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel SearchObservations (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Searches the Observations for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SearchObservationsExample
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
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Searches the Observations for a given tenant
                EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel result = apiInstance.SearchObservations(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.SearchObservations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SearchObservationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Searches the Observations for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel> response = apiInstance.SearchObservationsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.SearchObservationsWithHttpInfo: " + e.Message);
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
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel**](EvaluationApiEvaluationsV1EvaluationResponsePaginatedItemsViewModel.md)

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

<a id="updateobservation"></a>
# **UpdateObservation**
> EvaluationApiEvaluationsV1EvaluationUpdatedResponse UpdateObservation (Guid tenantId, Guid observationId, EvaluationApiEvaluationsV1UpdateEvaluationRequest evaluationApiEvaluationsV1UpdateEvaluationRequest = null)

Updates an Observation for a given tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateObservationExample
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
            var evaluationApiEvaluationsV1UpdateEvaluationRequest = new EvaluationApiEvaluationsV1UpdateEvaluationRequest(); // EvaluationApiEvaluationsV1UpdateEvaluationRequest |  (optional) 

            try
            {
                // Updates an Observation for a given tenant
                EvaluationApiEvaluationsV1EvaluationUpdatedResponse result = apiInstance.UpdateObservation(tenantId, observationId, evaluationApiEvaluationsV1UpdateEvaluationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationsApi.UpdateObservation: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateObservationWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Observation for a given tenant
    ApiResponse<EvaluationApiEvaluationsV1EvaluationUpdatedResponse> response = apiInstance.UpdateObservationWithHttpInfo(tenantId, observationId, evaluationApiEvaluationsV1UpdateEvaluationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationsApi.UpdateObservationWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **observationId** | **Guid** |  |  |
| **evaluationApiEvaluationsV1UpdateEvaluationRequest** | [**EvaluationApiEvaluationsV1UpdateEvaluationRequest**](EvaluationApiEvaluationsV1UpdateEvaluationRequest.md) |  | [optional]  |

### Return type

[**EvaluationApiEvaluationsV1EvaluationUpdatedResponse**](EvaluationApiEvaluationsV1EvaluationUpdatedResponse.md)

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

