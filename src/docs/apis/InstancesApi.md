# EdGraph.Platform.Client.Api.InstancesApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddRelatedInstances**](InstancesApi.md#addrelatedinstances) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/relatedinstances | Add related instances to root instance by Id |
| [**AddSchoolYear**](InstancesApi.md#addschoolyear) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years | Adds an ODS database to an Instance. |
| [**AddSchoolYearRange**](InstancesApi.md#addschoolyearrange) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/bulk | Adds multiple ODS databases to an instance. |
| [**ChangeInstanceDatabaseTierAsync**](InstancesApi.md#changeinstancedatabasetierasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/tiers | Changes the selected tier of an ODS database. |
| [**CloneInstanceAsync**](InstancesApi.md#cloneinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/clone | Clones an instance. |
| [**CreateInstance**](InstancesApi.md#createinstance) | **POST** /tenants/{tenantId}/oneroster/instances | Creates a new Instance. |
| [**CreateInstanceAsync**](InstancesApi.md#createinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances | Creates a new Instance. |
| [**DeleteInstance**](InstancesApi.md#deleteinstance) | **DELETE** /tenants/{tenantId}/oneroster/instances/{instanceId} | Deletes an Instance. |
| [**DeleteInstanceAsync**](InstancesApi.md#deleteinstanceasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Deletes an Instance. |
| [**DeleteSchoolYearAsync**](InstancesApi.md#deleteschoolyearasync) | **DELETE** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year} | Removes an ODS database from an Instance. |
| [**GetEdFiAdminInstanceEndpoints**](InstancesApi.md#getedfiadmininstanceendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance. |
| [**GetEdFiAdminInstanceYearEndpoints**](InstancesApi.md#getedfiadmininstanceyearendpoints) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/endpoints | Retrieves the Ed-Fi API endpoint URLs of an Instance. |
| [**GetInstanceById**](InstancesApi.md#getinstancebyid) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId} | Retrieves an Instance by ID. |
| [**GetInstanceByIdAsync**](InstancesApi.md#getinstancebyidasync) | **GET** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Retrieves an Instance by ID. |
| [**GetInstanceCsvExport**](InstancesApi.md#getinstancecsvexport) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves an Instance by ID. |
| [**GetInstanceCsvExportV2**](InstancesApi.md#getinstancecsvexportv2) | **GET** /v2/tenants/{tenantId}/oneroster/instances/{instanceId}/csv/export | Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format |
| [**GetInstanceEndpoints**](InstancesApi.md#getinstanceendpoints) | **GET** /tenants/{tenantId}/oneroster/instances/{instanceId}/endpoints | Retrieves the One Roster endpoint URLs of an Instance. |
| [**GetInstancesAsync**](InstancesApi.md#getinstancesasync) | **GET** /tenants/{tenantId}/edfiadmin/instances | Retrieves a list of Instances. |
| [**GetPagedInstances**](InstancesApi.md#getpagedinstances) | **GET** /tenants/{tenantId}/oneroster/instances | Retrieves a list of Instances. |
| [**GetTenantInstancesV2**](InstancesApi.md#gettenantinstancesv2) | **GET** /v2/tenants/{tenantId}/instances | Get list of all instances for a tenant - V2 |
| [**IsInstanceCustomIdAvailable**](InstancesApi.md#isinstancecustomidavailable) | **GET** /tenants/{tenantId}/oneroster/instances/isinstancecustomidavailable/{customId} | Validate if instance is available |
| [**LoadApiMetadata**](InstancesApi.md#loadapimetadata) | **POST** /tenants/{tenantId}/edfiadmin/api-metadata | Loads connection metadata. |
| [**ResetInstance**](InstancesApi.md#resetinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/resetinstance | Resets an Instance. |
| [**ResetInstanceAsync**](InstancesApi.md#resetinstanceasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/resetinstance | Resets an Instance. |
| [**ResetInstanceCacheAsync**](InstancesApi.md#resetinstancecacheasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetcache | Resets the cache of an Instance and the specified ODS database. |
| [**ResetSchoolYearAsync**](InstancesApi.md#resetschoolyearasync) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/resetods | Resets the ODS database with the specified school year. |
| [**SetInstanceIsDefault**](InstancesApi.md#setinstanceisdefault) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/default | Updates the isDefault property for an instance |
| [**TestConnectionDetailsByInstanceIdAsync**](InstancesApi.md#testconnectiondetailsbyinstanceidasync) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/test | Tests the connection by obtaining the details by Instance ID |
| [**TestCredentialsConnection**](InstancesApi.md#testcredentialsconnection) | **POST** /tenants/{tenantId}/edfiadmin/testconnection | Tests availability of provided connection metadata. |
| [**TestInstanceConnection**](InstancesApi.md#testinstanceconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/testconnection | Tests the connection of the Instance. |
| [**TestInstanceYearConnection**](InstancesApi.md#testinstanceyearconnection) | **POST** /tenants/{tenantId}/edfiadmin/instances/{instanceId}/years/{year}/testconnection | Tests the connection of the Instance. |
| [**TruncateInstance**](InstancesApi.md#truncateinstance) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/truncate | Truncates the Instance&#39;s database |
| [**UpdateInstance**](InstancesApi.md#updateinstance) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId} | Updates an Instance. |
| [**UpdateInstanceAsync**](InstancesApi.md#updateinstanceasync) | **PUT** /tenants/{tenantId}/edfiadmin/instances/{instanceId} | Updates an Instance. |
| [**ValidateCustomIdAvailable**](InstancesApi.md#validatecustomidavailable) | **GET** /tenants/{tenantId}/edfiadmin/instances/validatecustomidavailable/{customId} | Validate if instance is available |

<a id="addrelatedinstances"></a>
# **AddRelatedInstances**
> EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse AddRelatedInstances (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest = null)

Add related instances to root instance by Id

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddRelatedInstancesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest = new EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest(); // EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest |  (optional) 

            try
            {
                // Add related instances to root instance by Id
                EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse result = apiInstance.AddRelatedInstances(tenantId, instanceId, edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.AddRelatedInstances: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddRelatedInstancesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Add related instances to root instance by Id
    ApiResponse<EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse> response = apiInstance.AddRelatedInstancesWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.AddRelatedInstancesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1AddRelatedInstancesRequest** | [**EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest**](EdfiAdminApiEdfiAdminV1AddRelatedInstancesRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse**](EdfiAdminApiEdfiAdminV1AddRelatedInstancesResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addschoolyear"></a>
# **AddSchoolYear**
> void AddSchoolYear (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1AddSchoolYearRequest edfiAdminApiEdfiAdminV1AddSchoolYearRequest = null)

Adds an ODS database to an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddSchoolYearExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1AddSchoolYearRequest = new EdfiAdminApiEdfiAdminV1AddSchoolYearRequest(); // EdfiAdminApiEdfiAdminV1AddSchoolYearRequest |  (optional) 

            try
            {
                // Adds an ODS database to an Instance.
                apiInstance.AddSchoolYear(tenantId, instanceId, edfiAdminApiEdfiAdminV1AddSchoolYearRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.AddSchoolYear: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddSchoolYearWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds an ODS database to an Instance.
    apiInstance.AddSchoolYearWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1AddSchoolYearRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.AddSchoolYearWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1AddSchoolYearRequest** | [**EdfiAdminApiEdfiAdminV1AddSchoolYearRequest**](EdfiAdminApiEdfiAdminV1AddSchoolYearRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="addschoolyearrange"></a>
# **AddSchoolYearRange**
> void AddSchoolYearRange (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest = null)

Adds multiple ODS databases to an instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddSchoolYearRangeExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest = new EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest(); // EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest |  (optional) 

            try
            {
                // Adds multiple ODS databases to an instance.
                apiInstance.AddSchoolYearRange(tenantId, instanceId, edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.AddSchoolYearRange: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddSchoolYearRangeWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds multiple ODS databases to an instance.
    apiInstance.AddSchoolYearRangeWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.AddSchoolYearRangeWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest** | [**EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest**](EdfiAdminApiEdfiAdminV1AddSchoolYearRangeRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="changeinstancedatabasetierasync"></a>
# **ChangeInstanceDatabaseTierAsync**
> void ChangeInstanceDatabaseTierAsync (string tenantId, string instanceId, int year, EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest = null)

Changes the selected tier of an ODS database.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ChangeInstanceDatabaseTierAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 
            var edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest = new EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest(); // EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest |  (optional) 

            try
            {
                // Changes the selected tier of an ODS database.
                apiInstance.ChangeInstanceDatabaseTierAsync(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.ChangeInstanceDatabaseTierAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ChangeInstanceDatabaseTierAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Changes the selected tier of an ODS database.
    apiInstance.ChangeInstanceDatabaseTierAsyncWithHttpInfo(tenantId, instanceId, year, edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.ChangeInstanceDatabaseTierAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |
| **edfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest** | [**EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest**](EdfiAdminApiEdfiAdminV1ChangeDatabaseTierRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="cloneinstanceasync"></a>
# **CloneInstanceAsync**
> EdfiAdminApiEdfiAdminV1CloneInstanceResponse CloneInstanceAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1CloneInstanceRequest edfiAdminApiEdfiAdminV1CloneInstanceRequest = null)

Clones an instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CloneInstanceAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1CloneInstanceRequest = new EdfiAdminApiEdfiAdminV1CloneInstanceRequest(); // EdfiAdminApiEdfiAdminV1CloneInstanceRequest |  (optional) 

            try
            {
                // Clones an instance.
                EdfiAdminApiEdfiAdminV1CloneInstanceResponse result = apiInstance.CloneInstanceAsync(tenantId, instanceId, edfiAdminApiEdfiAdminV1CloneInstanceRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.CloneInstanceAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CloneInstanceAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Clones an instance.
    ApiResponse<EdfiAdminApiEdfiAdminV1CloneInstanceResponse> response = apiInstance.CloneInstanceAsyncWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1CloneInstanceRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.CloneInstanceAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CloneInstanceRequest** | [**EdfiAdminApiEdfiAdminV1CloneInstanceRequest**](EdfiAdminApiEdfiAdminV1CloneInstanceRequest.md) |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1CloneInstanceResponse**](EdfiAdminApiEdfiAdminV1CloneInstanceResponse.md)

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

<a id="createinstance"></a>
# **CreateInstance**
> void CreateInstance (string tenantId, IMSAdminApiV1InstancesCreateInstanceRequest iMSAdminApiV1InstancesCreateInstanceRequest = null)

Creates a new Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var iMSAdminApiV1InstancesCreateInstanceRequest = new IMSAdminApiV1InstancesCreateInstanceRequest(); // IMSAdminApiV1InstancesCreateInstanceRequest |  (optional) 

            try
            {
                // Creates a new Instance.
                apiInstance.CreateInstance(tenantId, iMSAdminApiV1InstancesCreateInstanceRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.CreateInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Instance.
    apiInstance.CreateInstanceWithHttpInfo(tenantId, iMSAdminApiV1InstancesCreateInstanceRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.CreateInstanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **iMSAdminApiV1InstancesCreateInstanceRequest** | [**IMSAdminApiV1InstancesCreateInstanceRequest**](IMSAdminApiV1InstancesCreateInstanceRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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

<a id="createinstanceasync"></a>
# **CreateInstanceAsync**
> void CreateInstanceAsync (string tenantId, EdfiAdminApiEdfiAdminV1CreateInstanceRequest edfiAdminApiEdfiAdminV1CreateInstanceRequest = null)

Creates a new Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class CreateInstanceAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edfiAdminApiEdfiAdminV1CreateInstanceRequest = new EdfiAdminApiEdfiAdminV1CreateInstanceRequest(); // EdfiAdminApiEdfiAdminV1CreateInstanceRequest |  (optional) 

            try
            {
                // Creates a new Instance.
                apiInstance.CreateInstanceAsync(tenantId, edfiAdminApiEdfiAdminV1CreateInstanceRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.CreateInstanceAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the CreateInstanceAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new Instance.
    apiInstance.CreateInstanceAsyncWithHttpInfo(tenantId, edfiAdminApiEdfiAdminV1CreateInstanceRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.CreateInstanceAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1CreateInstanceRequest** | [**EdfiAdminApiEdfiAdminV1CreateInstanceRequest**](EdfiAdminApiEdfiAdminV1CreateInstanceRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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

<a id="deleteinstance"></a>
# **DeleteInstance**
> void DeleteInstance (string tenantId, string instanceId)

Deletes an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Deletes an Instance.
                apiInstance.DeleteInstance(tenantId, instanceId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.DeleteInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an Instance.
    apiInstance.DeleteInstanceWithHttpInfo(tenantId, instanceId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.DeleteInstanceWithHttpInfo: " + e.Message);
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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteinstanceasync"></a>
# **DeleteInstanceAsync**
> void DeleteInstanceAsync (string tenantId, string instanceId)

Deletes an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteInstanceAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Deletes an Instance.
                apiInstance.DeleteInstanceAsync(tenantId, instanceId);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.DeleteInstanceAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteInstanceAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Deletes an Instance.
    apiInstance.DeleteInstanceAsyncWithHttpInfo(tenantId, instanceId);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.DeleteInstanceAsyncWithHttpInfo: " + e.Message);
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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deleteschoolyearasync"></a>
# **DeleteSchoolYearAsync**
> void DeleteSchoolYearAsync (string tenantId, string instanceId, int year)

Removes an ODS database from an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class DeleteSchoolYearAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 

            try
            {
                // Removes an ODS database from an Instance.
                apiInstance.DeleteSchoolYearAsync(tenantId, instanceId, year);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.DeleteSchoolYearAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the DeleteSchoolYearAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Removes an ODS database from an Instance.
    apiInstance.DeleteSchoolYearAsyncWithHttpInfo(tenantId, instanceId, year);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.DeleteSchoolYearAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

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
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="getedfiadmininstanceendpoints"></a>
# **GetEdFiAdminInstanceEndpoints**
> EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse GetEdFiAdminInstanceEndpoints (string tenantId, string instanceId)

Retrieves the Ed-Fi API endpoint URLs of an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEdFiAdminInstanceEndpointsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Retrieves the Ed-Fi API endpoint URLs of an Instance.
                EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse result = apiInstance.GetEdFiAdminInstanceEndpoints(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetEdFiAdminInstanceEndpoints: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEdFiAdminInstanceEndpointsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Ed-Fi API endpoint URLs of an Instance.
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse> response = apiInstance.GetEdFiAdminInstanceEndpointsWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetEdFiAdminInstanceEndpointsWithHttpInfo: " + e.Message);
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

[**EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse**](EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)

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

<a id="getedfiadmininstanceyearendpoints"></a>
# **GetEdFiAdminInstanceYearEndpoints**
> EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse GetEdFiAdminInstanceYearEndpoints (string tenantId, string instanceId, int year)

Retrieves the Ed-Fi API endpoint URLs of an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetEdFiAdminInstanceYearEndpointsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 

            try
            {
                // Retrieves the Ed-Fi API endpoint URLs of an Instance.
                EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse result = apiInstance.GetEdFiAdminInstanceYearEndpoints(tenantId, instanceId, year);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetEdFiAdminInstanceYearEndpoints: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetEdFiAdminInstanceYearEndpointsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the Ed-Fi API endpoint URLs of an Instance.
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse> response = apiInstance.GetEdFiAdminInstanceYearEndpointsWithHttpInfo(tenantId, instanceId, year);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetEdFiAdminInstanceYearEndpointsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse**](EdfiAdminApiEdfiAdminV1InstanceEndpointsResponse.md)

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

<a id="getinstancebyid"></a>
# **GetInstanceById**
> IMSAdminApiV1InstancesInstanceProfileResponse GetInstanceById (string tenantId, string instanceId)

Retrieves an Instance by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstanceByIdExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Retrieves an Instance by ID.
                IMSAdminApiV1InstancesInstanceProfileResponse result = apiInstance.GetInstanceById(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetInstanceById: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstanceByIdWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an Instance by ID.
    ApiResponse<IMSAdminApiV1InstancesInstanceProfileResponse> response = apiInstance.GetInstanceByIdWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetInstanceByIdWithHttpInfo: " + e.Message);
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

[**IMSAdminApiV1InstancesInstanceProfileResponse**](IMSAdminApiV1InstancesInstanceProfileResponse.md)

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

<a id="getinstancebyidasync"></a>
# **GetInstanceByIdAsync**
> EdfiAdminApiEdfiAdminV1Instance GetInstanceByIdAsync (string tenantId, string instanceId)

Retrieves an Instance by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstanceByIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Retrieves an Instance by ID.
                EdfiAdminApiEdfiAdminV1Instance result = apiInstance.GetInstanceByIdAsync(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetInstanceByIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstanceByIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an Instance by ID.
    ApiResponse<EdfiAdminApiEdfiAdminV1Instance> response = apiInstance.GetInstanceByIdAsyncWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetInstanceByIdAsyncWithHttpInfo: " + e.Message);
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

[**EdfiAdminApiEdfiAdminV1Instance**](EdfiAdminApiEdfiAdminV1Instance.md)

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

<a id="getinstancecsvexport"></a>
# **GetInstanceCsvExport**
> IMSAdminApiV1InstancesGetInstanceCsvExportResponse GetInstanceCsvExport (string tenantId, string instanceId)

Retrieves an Instance by ID.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstanceCsvExportExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Retrieves an Instance by ID.
                IMSAdminApiV1InstancesGetInstanceCsvExportResponse result = apiInstance.GetInstanceCsvExport(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetInstanceCsvExport: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstanceCsvExportWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves an Instance by ID.
    ApiResponse<IMSAdminApiV1InstancesGetInstanceCsvExportResponse> response = apiInstance.GetInstanceCsvExportWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetInstanceCsvExportWithHttpInfo: " + e.Message);
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

[**IMSAdminApiV1InstancesGetInstanceCsvExportResponse**](IMSAdminApiV1InstancesGetInstanceCsvExportResponse.md)

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

<a id="getinstancecsvexportv2"></a>
# **GetInstanceCsvExportV2**
> IMSAdminApiV1InstancesInstanceCsvExportedResponse GetInstanceCsvExportV2 (string tenantId, string instanceId)

Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstanceCsvExportV2Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format
                IMSAdminApiV1InstancesInstanceCsvExportedResponse result = apiInstance.GetInstanceCsvExportV2(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetInstanceCsvExportV2: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstanceCsvExportV2WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a ZIP bundle containing OneRoster Instance Database contents in CSV format
    ApiResponse<IMSAdminApiV1InstancesInstanceCsvExportedResponse> response = apiInstance.GetInstanceCsvExportV2WithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetInstanceCsvExportV2WithHttpInfo: " + e.Message);
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

[**IMSAdminApiV1InstancesInstanceCsvExportedResponse**](IMSAdminApiV1InstancesInstanceCsvExportedResponse.md)

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

<a id="getinstanceendpoints"></a>
# **GetInstanceEndpoints**
> IMSAdminApiV1InstancesInstanceEndpointsResponse GetInstanceEndpoints (string tenantId, string instanceId)

Retrieves the One Roster endpoint URLs of an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstanceEndpointsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Retrieves the One Roster endpoint URLs of an Instance.
                IMSAdminApiV1InstancesInstanceEndpointsResponse result = apiInstance.GetInstanceEndpoints(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetInstanceEndpoints: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstanceEndpointsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves the One Roster endpoint URLs of an Instance.
    ApiResponse<IMSAdminApiV1InstancesInstanceEndpointsResponse> response = apiInstance.GetInstanceEndpointsWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetInstanceEndpointsWithHttpInfo: " + e.Message);
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

[**IMSAdminApiV1InstancesInstanceEndpointsResponse**](IMSAdminApiV1InstancesInstanceEndpointsResponse.md)

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

<a id="getinstancesasync"></a>
# **GetInstancesAsync**
> EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel GetInstancesAsync (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null, bool deleted = null, string targetTenantId = null)

Retrieves a list of Instances.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetInstancesAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")
            var deleted = false;  // bool |  (optional)  (default to false)
            var targetTenantId = "targetTenantId_example";  // string |  (optional) 

            try
            {
                // Retrieves a list of Instances.
                EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel result = apiInstance.GetInstancesAsync(tenantId, pageSize, pageIndex, orderBy, filter, deleted, targetTenantId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetInstancesAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetInstancesAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Instances.
    ApiResponse<EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel> response = apiInstance.GetInstancesAsyncWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter, deleted, targetTenantId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetInstancesAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |
| **deleted** | **bool** |  | [optional] [default to false] |
| **targetTenantId** | **string** |  | [optional]  |

### Return type

[**EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel**](EdfiAdminApiEdfiAdminV1InstanceListModelPaginatedItemsViewModel.md)

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

<a id="getpagedinstances"></a>
# **GetPagedInstances**
> IMSAdminApiV1InstancesPagedInstancesResponse GetPagedInstances (string tenantId, int pageSize = null, int pageIndex = null, string orderBy = null, string filter = null)

Retrieves a list of Instances.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetPagedInstancesExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var orderBy = "\"\"";  // string |  (optional)  (default to "")
            var filter = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Retrieves a list of Instances.
                IMSAdminApiV1InstancesPagedInstancesResponse result = apiInstance.GetPagedInstances(tenantId, pageSize, pageIndex, orderBy, filter);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetPagedInstances: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetPagedInstancesWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Retrieves a list of Instances.
    ApiResponse<IMSAdminApiV1InstancesPagedInstancesResponse> response = apiInstance.GetPagedInstancesWithHttpInfo(tenantId, pageSize, pageIndex, orderBy, filter);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetPagedInstancesWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **orderBy** | **string** |  | [optional] [default to &quot;&quot;] |
| **filter** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**IMSAdminApiV1InstancesPagedInstancesResponse**](IMSAdminApiV1InstancesPagedInstancesResponse.md)

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

<a id="gettenantinstancesv2"></a>
# **GetTenantInstancesV2**
> EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel GetTenantInstancesV2 (string tenantId, int pageSize = null, int pageIndex = null, string searchTerm = null, string type = null)

Get list of all instances for a tenant - V2

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetTenantInstancesV2Example
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var pageSize = 10;  // int |  (optional)  (default to 10)
            var pageIndex = 0;  // int |  (optional)  (default to 0)
            var searchTerm = "\"\"";  // string |  (optional)  (default to "")
            var type = "\"\"";  // string |  (optional)  (default to "")

            try
            {
                // Get list of all instances for a tenant - V2
                EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel result = apiInstance.GetTenantInstancesV2(tenantId, pageSize, pageIndex, searchTerm, type);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.GetTenantInstancesV2: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetTenantInstancesV2WithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Get list of all instances for a tenant - V2
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel> response = apiInstance.GetTenantInstancesV2WithHttpInfo(tenantId, pageSize, pageIndex, searchTerm, type);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.GetTenantInstancesV2WithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **searchTerm** | **string** |  | [optional] [default to &quot;&quot;] |
| **type** | **string** |  | [optional] [default to &quot;&quot;] |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel**](EdGraphHttpAggregatorsTenantApiServicesInstancesInstanceResponsePaginatedItemsViewModel.md)

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

<a id="isinstancecustomidavailable"></a>
# **IsInstanceCustomIdAvailable**
> bool IsInstanceCustomIdAvailable (string tenantId, string customId)

Validate if instance is available

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class IsInstanceCustomIdAvailableExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var customId = "customId_example";  // string | 

            try
            {
                // Validate if instance is available
                bool result = apiInstance.IsInstanceCustomIdAvailable(tenantId, customId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.IsInstanceCustomIdAvailable: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the IsInstanceCustomIdAvailableWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate if instance is available
    ApiResponse<bool> response = apiInstance.IsInstanceCustomIdAvailableWithHttpInfo(tenantId, customId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.IsInstanceCustomIdAvailableWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **customId** | **string** |  |  |

### Return type

**bool**

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

<a id="loadapimetadata"></a>
# **LoadApiMetadata**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult LoadApiMetadata (string tenantId, EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest = null)

Loads connection metadata.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class LoadApiMetadataExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest = new EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest(); // EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest |  (optional) 

            try
            {
                // Loads connection metadata.
                EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult result = apiInstance.LoadApiMetadata(tenantId, edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.LoadApiMetadata: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the LoadApiMetadataWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Loads connection metadata.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult> response = apiInstance.LoadApiMetadataWithHttpInfo(tenantId, edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.LoadApiMetadataWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **edGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest** | [**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiMetadataRequest.md) |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsEdFiApiLoadEdFiApiMetadataResult.md)

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

<a id="resetinstance"></a>
# **ResetInstance**
> IMSAdminApiV1InstancesInstanceResetResponse ResetInstance (string tenantId, string instanceId)

Resets an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ResetInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Resets an Instance.
                IMSAdminApiV1InstancesInstanceResetResponse result = apiInstance.ResetInstance(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.ResetInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resets an Instance.
    ApiResponse<IMSAdminApiV1InstancesInstanceResetResponse> response = apiInstance.ResetInstanceWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.ResetInstanceWithHttpInfo: " + e.Message);
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

[**IMSAdminApiV1InstancesInstanceResetResponse**](IMSAdminApiV1InstancesInstanceResetResponse.md)

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

<a id="resetinstanceasync"></a>
# **ResetInstanceAsync**
> EdfiAdminApiEdfiAdminV1ResetInstanceResponse ResetInstanceAsync (string tenantId, string instanceId)

Resets an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ResetInstanceAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Resets an Instance.
                EdfiAdminApiEdfiAdminV1ResetInstanceResponse result = apiInstance.ResetInstanceAsync(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.ResetInstanceAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetInstanceAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resets an Instance.
    ApiResponse<EdfiAdminApiEdfiAdminV1ResetInstanceResponse> response = apiInstance.ResetInstanceAsyncWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.ResetInstanceAsyncWithHttpInfo: " + e.Message);
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

[**EdfiAdminApiEdfiAdminV1ResetInstanceResponse**](EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)

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

<a id="resetinstancecacheasync"></a>
# **ResetInstanceCacheAsync**
> EdfiAdminApiEdfiAdminV1ResetInstanceResponse ResetInstanceCacheAsync (string tenantId, string instanceId, int year)

Resets the cache of an Instance and the specified ODS database.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ResetInstanceCacheAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 

            try
            {
                // Resets the cache of an Instance and the specified ODS database.
                EdfiAdminApiEdfiAdminV1ResetInstanceResponse result = apiInstance.ResetInstanceCacheAsync(tenantId, instanceId, year);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.ResetInstanceCacheAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetInstanceCacheAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resets the cache of an Instance and the specified ODS database.
    ApiResponse<EdfiAdminApiEdfiAdminV1ResetInstanceResponse> response = apiInstance.ResetInstanceCacheAsyncWithHttpInfo(tenantId, instanceId, year);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.ResetInstanceCacheAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1ResetInstanceResponse**](EdfiAdminApiEdfiAdminV1ResetInstanceResponse.md)

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

<a id="resetschoolyearasync"></a>
# **ResetSchoolYearAsync**
> void ResetSchoolYearAsync (string tenantId, string instanceId, int year)

Resets the ODS database with the specified school year.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ResetSchoolYearAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 

            try
            {
                // Resets the ODS database with the specified school year.
                apiInstance.ResetSchoolYearAsync(tenantId, instanceId, year);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.ResetSchoolYearAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ResetSchoolYearAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Resets the ODS database with the specified school year.
    apiInstance.ResetSchoolYearAsyncWithHttpInfo(tenantId, instanceId, year);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.ResetSchoolYearAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

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
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="setinstanceisdefault"></a>
# **SetInstanceIsDefault**
> void SetInstanceIsDefault (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest = null)

Updates the isDefault property for an instance

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class SetInstanceIsDefaultExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest = new EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest(); // EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest |  (optional) 

            try
            {
                // Updates the isDefault property for an instance
                apiInstance.SetInstanceIsDefault(tenantId, instanceId, edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.SetInstanceIsDefault: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the SetInstanceIsDefaultWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates the isDefault property for an instance
    apiInstance.SetInstanceIsDefaultWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.SetInstanceIsDefaultWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest** | [**EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest**](EdfiAdminApiEdfiAdminV1SetInstanceIsDefaultRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="testconnectiondetailsbyinstanceidasync"></a>
# **TestConnectionDetailsByInstanceIdAsync**
> IMSAdminApiV1ConnectionsConnectionTestedResponse TestConnectionDetailsByInstanceIdAsync (Guid tenantId, Guid instanceId, IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest = null)

Tests the connection by obtaining the details by Instance ID

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestConnectionDetailsByInstanceIdAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 
            var iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest = new IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest(); // IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest |  (optional) 

            try
            {
                // Tests the connection by obtaining the details by Instance ID
                IMSAdminApiV1ConnectionsConnectionTestedResponse result = apiInstance.TestConnectionDetailsByInstanceIdAsync(tenantId, instanceId, iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.TestConnectionDetailsByInstanceIdAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestConnectionDetailsByInstanceIdAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests the connection by obtaining the details by Instance ID
    ApiResponse<IMSAdminApiV1ConnectionsConnectionTestedResponse> response = apiInstance.TestConnectionDetailsByInstanceIdAsyncWithHttpInfo(tenantId, instanceId, iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.TestConnectionDetailsByInstanceIdAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |
| **iMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest** | [**IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest**](IMSAdminApiV1ConnectionsTestConnectionDetailsByInstanceIdRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ConnectionsConnectionTestedResponse**](IMSAdminApiV1ConnectionsConnectionTestedResponse.md)

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

<a id="testcredentialsconnection"></a>
# **TestCredentialsConnection**
> EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse TestCredentialsConnection (string tenantId, Object body = null)

Tests availability of provided connection metadata.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestCredentialsConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var body = null;  // Object |  (optional) 

            try
            {
                // Tests availability of provided connection metadata.
                EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse result = apiInstance.TestCredentialsConnection(tenantId, body);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.TestCredentialsConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestCredentialsConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests availability of provided connection metadata.
    ApiResponse<EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse> response = apiInstance.TestCredentialsConnectionWithHttpInfo(tenantId, body);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.TestCredentialsConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **body** | **Object** |  | [optional]  |

### Return type

[**EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse**](EdGraphHttpAggregatorsTenantApiServicesOnboardingStepsTestConnectionResponse.md)

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
| **404** | The resource could not be found. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="testinstanceconnection"></a>
# **TestInstanceConnection**
> EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse TestInstanceConnection (string tenantId, string instanceId)

Tests the connection of the Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestInstanceConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 

            try
            {
                // Tests the connection of the Instance.
                EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse result = apiInstance.TestInstanceConnection(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.TestInstanceConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestInstanceConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests the connection of the Instance.
    ApiResponse<EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse> response = apiInstance.TestInstanceConnectionWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.TestInstanceConnectionWithHttpInfo: " + e.Message);
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

[**EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse**](EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)

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

<a id="testinstanceyearconnection"></a>
# **TestInstanceYearConnection**
> EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse TestInstanceYearConnection (string tenantId, string instanceId, int year)

Tests the connection of the Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TestInstanceYearConnectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var year = 56;  // int | 

            try
            {
                // Tests the connection of the Instance.
                EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse result = apiInstance.TestInstanceYearConnection(tenantId, instanceId, year);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.TestInstanceYearConnection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TestInstanceYearConnectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Tests the connection of the Instance.
    ApiResponse<EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse> response = apiInstance.TestInstanceYearConnectionWithHttpInfo(tenantId, instanceId, year);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.TestInstanceYearConnectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **year** | **int** |  |  |

### Return type

[**EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse**](EdfiAdminApiEdfiAdminV1TestInstanceConnectionResponse.md)

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

<a id="truncateinstance"></a>
# **TruncateInstance**
> IMSAdminApiV1InstancesInstanceTruncatedResponse TruncateInstance (Guid tenantId, Guid instanceId)

Truncates the Instance's database

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class TruncateInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var instanceId = "instanceId_example";  // Guid | 

            try
            {
                // Truncates the Instance's database
                IMSAdminApiV1InstancesInstanceTruncatedResponse result = apiInstance.TruncateInstance(tenantId, instanceId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.TruncateInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the TruncateInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Truncates the Instance's database
    ApiResponse<IMSAdminApiV1InstancesInstanceTruncatedResponse> response = apiInstance.TruncateInstanceWithHttpInfo(tenantId, instanceId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.TruncateInstanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **instanceId** | **Guid** |  |  |

### Return type

[**IMSAdminApiV1InstancesInstanceTruncatedResponse**](IMSAdminApiV1InstancesInstanceTruncatedResponse.md)

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

<a id="updateinstance"></a>
# **UpdateInstance**
> void UpdateInstance (string tenantId, string instanceId, IMSAdminApiV1InstancesUpdateInstanceRequest iMSAdminApiV1InstancesUpdateInstanceRequest = null)

Updates an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateInstanceExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var iMSAdminApiV1InstancesUpdateInstanceRequest = new IMSAdminApiV1InstancesUpdateInstanceRequest(); // IMSAdminApiV1InstancesUpdateInstanceRequest |  (optional) 

            try
            {
                // Updates an Instance.
                apiInstance.UpdateInstance(tenantId, instanceId, iMSAdminApiV1InstancesUpdateInstanceRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.UpdateInstance: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateInstanceWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Instance.
    apiInstance.UpdateInstanceWithHttpInfo(tenantId, instanceId, iMSAdminApiV1InstancesUpdateInstanceRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.UpdateInstanceWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **iMSAdminApiV1InstancesUpdateInstanceRequest** | [**IMSAdminApiV1InstancesUpdateInstanceRequest**](IMSAdminApiV1InstancesUpdateInstanceRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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

<a id="updateinstanceasync"></a>
# **UpdateInstanceAsync**
> void UpdateInstanceAsync (string tenantId, string instanceId, EdfiAdminApiEdfiAdminV1UpdateInstanceRequest edfiAdminApiEdfiAdminV1UpdateInstanceRequest = null)

Updates an Instance.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateInstanceAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var edfiAdminApiEdfiAdminV1UpdateInstanceRequest = new EdfiAdminApiEdfiAdminV1UpdateInstanceRequest(); // EdfiAdminApiEdfiAdminV1UpdateInstanceRequest |  (optional) 

            try
            {
                // Updates an Instance.
                apiInstance.UpdateInstanceAsync(tenantId, instanceId, edfiAdminApiEdfiAdminV1UpdateInstanceRequest);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.UpdateInstanceAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateInstanceAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates an Instance.
    apiInstance.UpdateInstanceAsyncWithHttpInfo(tenantId, instanceId, edfiAdminApiEdfiAdminV1UpdateInstanceRequest);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.UpdateInstanceAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **edfiAdminApiEdfiAdminV1UpdateInstanceRequest** | [**EdfiAdminApiEdfiAdminV1UpdateInstanceRequest**](EdfiAdminApiEdfiAdminV1UpdateInstanceRequest.md) |  | [optional]  |

### Return type

void (empty response body)

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

<a id="validatecustomidavailable"></a>
# **ValidateCustomIdAvailable**
> bool ValidateCustomIdAvailable (string tenantId, string customId)

Validate if instance is available

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class ValidateCustomIdAvailableExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new InstancesApi(config);
            var tenantId = "tenantId_example";  // string | 
            var customId = "customId_example";  // string | 

            try
            {
                // Validate if instance is available
                bool result = apiInstance.ValidateCustomIdAvailable(tenantId, customId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling InstancesApi.ValidateCustomIdAvailable: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the ValidateCustomIdAvailableWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Validate if instance is available
    ApiResponse<bool> response = apiInstance.ValidateCustomIdAvailableWithHttpInfo(tenantId, customId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling InstancesApi.ValidateCustomIdAvailableWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **customId** | **string** |  |  |

### Return type

**bool**

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

