# EdGraph.Platform.Client.Api.UsersSectionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddUserSection**](UsersSectionsApi.md#addusersection) | **POST** /tenants/{tenantId}/users/{userId}/sections | Adds a Section to a user. |
| [**AddUserSectionBulk**](UsersSectionsApi.md#addusersectionbulk) | **POST** /tenants/{tenantId}/users/{userId}/sections/bulk | Adds Sections to a user in bulk. |
| [**GetUserSections**](UsersSectionsApi.md#getusersections) | **GET** /tenants/{tenantId}/users/{userId}/sections | Gets the Sections of a user. |
| [**RemoveUserSection**](UsersSectionsApi.md#removeusersection) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Removes a Section from a user. |
| [**RemoveUserSectionBulk**](UsersSectionsApi.md#removeusersectionbulk) | **DELETE** /tenants/{tenantId}/users/{userId}/sections/bulk | Removes Sections from a user in bulk. |
| [**UpdateUserSection**](UsersSectionsApi.md#updateusersection) | **PUT** /tenants/{tenantId}/users/{userId}/sections/{userSectionId} | Updates the Section of a user. |
| [**UpdateUserSectionBulk**](UsersSectionsApi.md#updateusersectionbulk) | **PUT** /tenants/{tenantId}/users/{userId}/sections/bulk | Updates the Section of a user in bulk. |

<a id="addusersection"></a>
# **AddUserSection**
> IdentityApiUserV1SectionAddedResponse AddUserSection (Guid tenantId, Guid userId, IdentityApiUserV1AddSectionRequest identityApiUserV1AddSectionRequest = null)

Adds a Section to a user.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddUserSectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSectionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var identityApiUserV1AddSectionRequest = new IdentityApiUserV1AddSectionRequest(); // IdentityApiUserV1AddSectionRequest |  (optional) 

            try
            {
                // Adds a Section to a user.
                IdentityApiUserV1SectionAddedResponse result = apiInstance.AddUserSection(tenantId, userId, identityApiUserV1AddSectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSectionsApi.AddUserSection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddUserSectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds a Section to a user.
    ApiResponse<IdentityApiUserV1SectionAddedResponse> response = apiInstance.AddUserSectionWithHttpInfo(tenantId, userId, identityApiUserV1AddSectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSectionsApi.AddUserSectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1AddSectionRequest** | [**IdentityApiUserV1AddSectionRequest**](IdentityApiUserV1AddSectionRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionAddedResponse**](IdentityApiUserV1SectionAddedResponse.md)

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

<a id="addusersectionbulk"></a>
# **AddUserSectionBulk**
> IdentityApiUserV1SectionAddedBulkResponse AddUserSectionBulk (Guid tenantId, Guid userId, IdentityApiUserV1AddSectionBulkRequest identityApiUserV1AddSectionBulkRequest = null)

Adds Sections to a user in bulk.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddUserSectionBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSectionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var identityApiUserV1AddSectionBulkRequest = new IdentityApiUserV1AddSectionBulkRequest(); // IdentityApiUserV1AddSectionBulkRequest |  (optional) 

            try
            {
                // Adds Sections to a user in bulk.
                IdentityApiUserV1SectionAddedBulkResponse result = apiInstance.AddUserSectionBulk(tenantId, userId, identityApiUserV1AddSectionBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSectionsApi.AddUserSectionBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddUserSectionBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Adds Sections to a user in bulk.
    ApiResponse<IdentityApiUserV1SectionAddedBulkResponse> response = apiInstance.AddUserSectionBulkWithHttpInfo(tenantId, userId, identityApiUserV1AddSectionBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSectionsApi.AddUserSectionBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1AddSectionBulkRequest** | [**IdentityApiUserV1AddSectionBulkRequest**](IdentityApiUserV1AddSectionBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionAddedBulkResponse**](IdentityApiUserV1SectionAddedBulkResponse.md)

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

<a id="getusersections"></a>
# **GetUserSections**
> IdentityApiUserV1GetSectionsResponse GetUserSections (Guid tenantId, Guid userId)

Gets the Sections of a user.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class GetUserSectionsExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSectionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 

            try
            {
                // Gets the Sections of a user.
                IdentityApiUserV1GetSectionsResponse result = apiInstance.GetUserSections(tenantId, userId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSectionsApi.GetUserSections: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the GetUserSectionsWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Gets the Sections of a user.
    ApiResponse<IdentityApiUserV1GetSectionsResponse> response = apiInstance.GetUserSectionsWithHttpInfo(tenantId, userId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSectionsApi.GetUserSectionsWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |

### Return type

[**IdentityApiUserV1GetSectionsResponse**](IdentityApiUserV1GetSectionsResponse.md)

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

<a id="removeusersection"></a>
# **RemoveUserSection**
> IdentityApiUserV1SectionRemovedResponse RemoveUserSection (Guid tenantId, Guid userId, Guid userSectionId)

Removes a Section from a user.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RemoveUserSectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSectionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var userSectionId = "userSectionId_example";  // Guid | 

            try
            {
                // Removes a Section from a user.
                IdentityApiUserV1SectionRemovedResponse result = apiInstance.RemoveUserSection(tenantId, userId, userSectionId);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSectionsApi.RemoveUserSection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveUserSectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Removes a Section from a user.
    ApiResponse<IdentityApiUserV1SectionRemovedResponse> response = apiInstance.RemoveUserSectionWithHttpInfo(tenantId, userId, userSectionId);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSectionsApi.RemoveUserSectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **userSectionId** | **Guid** |  |  |

### Return type

[**IdentityApiUserV1SectionRemovedResponse**](IdentityApiUserV1SectionRemovedResponse.md)

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

<a id="removeusersectionbulk"></a>
# **RemoveUserSectionBulk**
> IdentityApiUserV1SectionRemovedBulkResponse RemoveUserSectionBulk (Guid tenantId, Guid userId, IdentityApiUserV1RemoveSectionBulkRequest identityApiUserV1RemoveSectionBulkRequest = null)

Removes Sections from a user in bulk.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RemoveUserSectionBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSectionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var identityApiUserV1RemoveSectionBulkRequest = new IdentityApiUserV1RemoveSectionBulkRequest(); // IdentityApiUserV1RemoveSectionBulkRequest |  (optional) 

            try
            {
                // Removes Sections from a user in bulk.
                IdentityApiUserV1SectionRemovedBulkResponse result = apiInstance.RemoveUserSectionBulk(tenantId, userId, identityApiUserV1RemoveSectionBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSectionsApi.RemoveUserSectionBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RemoveUserSectionBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Removes Sections from a user in bulk.
    ApiResponse<IdentityApiUserV1SectionRemovedBulkResponse> response = apiInstance.RemoveUserSectionBulkWithHttpInfo(tenantId, userId, identityApiUserV1RemoveSectionBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSectionsApi.RemoveUserSectionBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1RemoveSectionBulkRequest** | [**IdentityApiUserV1RemoveSectionBulkRequest**](IdentityApiUserV1RemoveSectionBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionRemovedBulkResponse**](IdentityApiUserV1SectionRemovedBulkResponse.md)

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

<a id="updateusersection"></a>
# **UpdateUserSection**
> IdentityApiUserV1SectionUpdatedResponse UpdateUserSection (Guid tenantId, Guid userId, Guid userSectionId, IdentityApiUserV1UpdateSectionRequest identityApiUserV1UpdateSectionRequest = null)

Updates the Section of a user.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateUserSectionExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSectionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var userSectionId = "userSectionId_example";  // Guid | 
            var identityApiUserV1UpdateSectionRequest = new IdentityApiUserV1UpdateSectionRequest(); // IdentityApiUserV1UpdateSectionRequest |  (optional) 

            try
            {
                // Updates the Section of a user.
                IdentityApiUserV1SectionUpdatedResponse result = apiInstance.UpdateUserSection(tenantId, userId, userSectionId, identityApiUserV1UpdateSectionRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSectionsApi.UpdateUserSection: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateUserSectionWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates the Section of a user.
    ApiResponse<IdentityApiUserV1SectionUpdatedResponse> response = apiInstance.UpdateUserSectionWithHttpInfo(tenantId, userId, userSectionId, identityApiUserV1UpdateSectionRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSectionsApi.UpdateUserSectionWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **userSectionId** | **Guid** |  |  |
| **identityApiUserV1UpdateSectionRequest** | [**IdentityApiUserV1UpdateSectionRequest**](IdentityApiUserV1UpdateSectionRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionUpdatedResponse**](IdentityApiUserV1SectionUpdatedResponse.md)

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

<a id="updateusersectionbulk"></a>
# **UpdateUserSectionBulk**
> IdentityApiUserV1SectionUpdatedBulkResponse UpdateUserSectionBulk (Guid tenantId, Guid userId, IdentityApiUserV1UpdateSectionBulkRequest identityApiUserV1UpdateSectionBulkRequest = null)

Updates the Section of a user in bulk.

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class UpdateUserSectionBulkExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new UsersSectionsApi(config);
            var tenantId = "tenantId_example";  // Guid | 
            var userId = "userId_example";  // Guid | 
            var identityApiUserV1UpdateSectionBulkRequest = new IdentityApiUserV1UpdateSectionBulkRequest(); // IdentityApiUserV1UpdateSectionBulkRequest |  (optional) 

            try
            {
                // Updates the Section of a user in bulk.
                IdentityApiUserV1SectionUpdatedBulkResponse result = apiInstance.UpdateUserSectionBulk(tenantId, userId, identityApiUserV1UpdateSectionBulkRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling UsersSectionsApi.UpdateUserSectionBulk: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the UpdateUserSectionBulkWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Updates the Section of a user in bulk.
    ApiResponse<IdentityApiUserV1SectionUpdatedBulkResponse> response = apiInstance.UpdateUserSectionBulkWithHttpInfo(tenantId, userId, identityApiUserV1UpdateSectionBulkRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling UsersSectionsApi.UpdateUserSectionBulkWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **Guid** |  |  |
| **userId** | **Guid** |  |  |
| **identityApiUserV1UpdateSectionBulkRequest** | [**IdentityApiUserV1UpdateSectionBulkRequest**](IdentityApiUserV1UpdateSectionBulkRequest.md) |  | [optional]  |

### Return type

[**IdentityApiUserV1SectionUpdatedBulkResponse**](IdentityApiUserV1SectionUpdatedBulkResponse.md)

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

