# EdGraph.Platform.Client.Api.ObservationSettingsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddAvailablePersona**](ObservationSettingsApi.md#addavailablepersona) | **POST** /tenants/{tenantId}/observations/settings/personas | Adds a persona for a given Tenant |
| [**GetApplicationSettings**](ObservationSettingsApi.md#getapplicationsettings) | **GET** /tenants/{tenantId}/observations/settings/application | Gets the application settings for the tenant |
| [**GetPaginatedForms**](ObservationSettingsApi.md#getpaginatedforms) | **GET** /tenants/{tenantId}/observations/forms | Get Paginated Forms |
| [**GetPaginatedPersonas**](ObservationSettingsApi.md#getpaginatedpersonas) | **GET** /tenants/{tenantId}/observations/settings/personas | Gets available personas |
| [**GetPaginatedStaffClassifications**](ObservationSettingsApi.md#getpaginatedstaffclassifications) | **GET** /tenants/{tenantId}/observations/settings/available-staffclassifications | Get Paginated Available StaffClassifications |
| [**GetStaffClassificationsSettings**](ObservationSettingsApi.md#getstaffclassificationssettings) | **GET** /tenants/{tenantId}/observations/settings/staffclassifications | Gets the staffClassification settings for the tenant |
| [**GetTEATenantOrganizations**](ObservationSettingsApi.md#getteatenantorganizations) | **GET** /tenants/{tenantId}/observations/tenantorganizations | Get TEA tenant organizations |
| [**SetApplicationSettings**](ObservationSettingsApi.md#setapplicationsettings) | **POST** /tenants/{tenantId}/observations/settings/application | Sets the Application Settings of an Observation for a given Tenant |
| [**SetRolePersonasSettings**](ObservationSettingsApi.md#setrolepersonassettings) | **POST** /tenants/{tenantId}/observations/settings/rolepersonas | Updates personas assigned to a role configuration of the tenants setting |
| [**VerifySysAdminCredentials**](ObservationSettingsApi.md#verifysysadmincredentials) | **GET** /tenants/{tenantId}/observations/settings/verify-credentials | Gets the staffClassification settings for the tenant |

<a id="addavailablepersona"></a>
# **AddAvailablePersona**
> EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse AddAvailablePersona (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest = null)

Adds a persona for a given Tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddAvailablePersonaExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest = new EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest(); // EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest |  (optional) 

            try
            {
                // Adds a persona for a given Tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse result = apiInstance.AddAvailablePersona(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.AddAvailablePersona: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddAvailablePersonaWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds a persona for a given Tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse> response = apiInstance.AddAvailablePersonaWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.AddAvailablePersonaWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsAddAvailablePersonaResponse.md)

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

<a id="getapplicationsettings"></a>
# **GetApplicationSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse GetApplicationSettings (Guid tenantId)

Gets the application settings for the tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetApplicationSettingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Gets the application settings for the tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse result = apiInstance.GetApplicationSettings(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.GetApplicationSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetApplicationSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets the application settings for the tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse> response = apiInstance.GetApplicationSettingsWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.GetApplicationSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsGetApplicationSettingsResponse.md)

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

<a id="getpaginatedforms"></a>
# **GetPaginatedForms**
> EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse GetPaginatedForms (Guid tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Get Paginated Forms

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedFormsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get Paginated Forms
                EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse result = apiInstance.GetPaginatedForms(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.GetPaginatedForms: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedFormsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Paginated Forms
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsFormResponseGetPaginatedItemsResponse> response = apiInstance.GetPaginatedFormsWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.GetPaginatedFormsWithHttpInfo: " + e.Message);
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

<a id="getpaginatedpersonas"></a>
# **GetPaginatedPersonas**
> EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse GetPaginatedPersonas (Guid tenantId)

Gets available personas

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedPersonasExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Gets available personas
                EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse result = apiInstance.GetPaginatedPersonas(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.GetPaginatedPersonas: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedPersonasWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets available personas
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse> response = apiInstance.GetPaginatedPersonasWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.GetPaginatedPersonasWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsPersonaResponseGetPaginatedItemsResponse.md)

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

<a id="getpaginatedstaffclassifications"></a>
# **GetPaginatedStaffClassifications**
> IdentityApiStaffClassificationV1GetStaffClassificationsResponse GetPaginatedStaffClassifications (Guid tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string filter = null)

Get Paginated Available StaffClassifications

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPaginatedStaffClassificationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get Paginated Available StaffClassifications
                IdentityApiStaffClassificationV1GetStaffClassificationsResponse result = apiInstance.GetPaginatedStaffClassifications(tenantId, pageIndex, pageSize, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.GetPaginatedStaffClassifications: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPaginatedStaffClassificationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get Paginated Available StaffClassifications
    ApiResponse<IdentityApiStaffClassificationV1GetStaffClassificationsResponse> response = apiInstance.GetPaginatedStaffClassificationsWithHttpInfo(tenantId, pageIndex, pageSize, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.GetPaginatedStaffClassificationsWithHttpInfo: " + e.Message);
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

[**IdentityApiStaffClassificationV1GetStaffClassificationsResponse**](IdentityApiStaffClassificationV1GetStaffClassificationsResponse.md)

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

<a id="getstaffclassificationssettings"></a>
# **GetStaffClassificationsSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse GetStaffClassificationsSettings (Guid tenantId)

Gets the staffClassification settings for the tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetStaffClassificationsSettingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Gets the staffClassification settings for the tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse result = apiInstance.GetStaffClassificationsSettings(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.GetStaffClassificationsSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetStaffClassificationsSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets the staffClassification settings for the tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse> response = apiInstance.GetStaffClassificationsSettingsWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.GetStaffClassificationsSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsGetStaffClassificationSettingsResponse.md)

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

<a id="getteatenantorganizations"></a>
# **GetTEATenantOrganizations**
> TenantApiTenantV1OrganizationGetPaginatedItemsResponse GetTEATenantOrganizations (Guid tenantId, string teaTenantId = null, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Get TEA tenant organizations

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTEATenantOrganizationsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var teaTenantId = "\"\"";  // string |  (optional)  (default to "")
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get TEA tenant organizations
                TenantApiTenantV1OrganizationGetPaginatedItemsResponse result = apiInstance.GetTEATenantOrganizations(tenantId, teaTenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.GetTEATenantOrganizations: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTEATenantOrganizationsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get TEA tenant organizations
    ApiResponse<TenantApiTenantV1OrganizationGetPaginatedItemsResponse> response = apiInstance.GetTEATenantOrganizationsWithHttpInfo(tenantId, teaTenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.GetTEATenantOrganizationsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **teaTenantId** | **string** |  | [optional] [default to &quot;&quot;] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**TenantApiTenantV1OrganizationGetPaginatedItemsResponse**](TenantApiTenantV1OrganizationGetPaginatedItemsResponse.md)

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

<a id="setapplicationsettings"></a>
# **SetApplicationSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse SetApplicationSettings (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest = null)

Sets the Application Settings of an Observation for a given Tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetApplicationSettingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest = new EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest(); // EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest |  (optional) 

            try
            {
                // Sets the Application Settings of an Observation for a given Tenant
                EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse result = apiInstance.SetApplicationSettings(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.SetApplicationSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetApplicationSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Sets the Application Settings of an Observation for a given Tenant
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse> response = apiInstance.SetApplicationSettingsWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.SetApplicationSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetApplicationSettingsResponse.md)

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

<a id="setrolepersonassettings"></a>
# **SetRolePersonasSettings**
> EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse SetRolePersonasSettings (Guid tenantId, EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest = null)

Updates personas assigned to a role configuration of the tenants setting

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetRolePersonasSettingsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest = new EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest(); // EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest |  (optional) 

            try
            {
                // Updates personas assigned to a role configuration of the tenants setting
                EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse result = apiInstance.SetRolePersonasSettings(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.SetRolePersonasSettings: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetRolePersonasSettingsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates personas assigned to a role configuration of the tenants setting
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse> response = apiInstance.SetRolePersonasSettingsWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.SetRolePersonasSettingsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest** | [**EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse**](EdGraphHttpAggregatorsTenantApiServicesObservationsSetRoleConfigurationResponse.md)

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

<a id="verifysysadmincredentials"></a>
# **VerifySysAdminCredentials**
> Object VerifySysAdminCredentials (Guid tenantId)

Gets the staffClassification settings for the tenant

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class VerifySysAdminCredentialsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ObservationSettingsApi(config);
            var tenantId = "tenantId_example";  // Guid | 

            try
            {
                // Gets the staffClassification settings for the tenant
                Object result = apiInstance.VerifySysAdminCredentials(tenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ObservationSettingsApi.VerifySysAdminCredentials: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the VerifySysAdminCredentialsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets the staffClassification settings for the tenant
    ApiResponse<Object> response = apiInstance.VerifySysAdminCredentialsWithHttpInfo(tenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ObservationSettingsApi.VerifySysAdminCredentialsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |

### Return type

**Object**

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

