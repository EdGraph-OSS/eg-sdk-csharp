# EdGraph.Platform.Client.Api.ClientsSecretsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**AddClientSecret**](ClientsSecretsApi.md#addclientsecret) | **POST** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/secrets | Creates a new secret for an OpenId client |
| [**RegenerateOneRosterApiClientSecretAsync**](ClientsSecretsApi.md#regenerateonerosterapiclientsecretasync) | **PUT** /tenants/{tenantId}/oneroster/instances/{instanceId}/clients/{clientId}/regeneratesecret | Regenerate Client Secret |

<a id="addclientsecret"></a>
# **AddClientSecret**
> IMSAdminApiV1ClientsClientSecretAddedResponse AddClientSecret (string tenantId, string instanceId, string clientId, IMSAdminApiV1ClientsAddClientSecretRequest iMSAdminApiV1ClientsAddClientSecretRequest = null)

Creates a new secret for an OpenId client

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class AddClientSecretExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ClientsSecretsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var clientId = "clientId_example";  // string | 
            var iMSAdminApiV1ClientsAddClientSecretRequest = new IMSAdminApiV1ClientsAddClientSecretRequest(); // IMSAdminApiV1ClientsAddClientSecretRequest |  (optional) 

            try
            {
                // Creates a new secret for an OpenId client
                IMSAdminApiV1ClientsClientSecretAddedResponse result = apiInstance.AddClientSecret(tenantId, instanceId, clientId, iMSAdminApiV1ClientsAddClientSecretRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ClientsSecretsApi.AddClientSecret: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the AddClientSecretWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Creates a new secret for an OpenId client
    ApiResponse<IMSAdminApiV1ClientsClientSecretAddedResponse> response = apiInstance.AddClientSecretWithHttpInfo(tenantId, instanceId, clientId, iMSAdminApiV1ClientsAddClientSecretRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ClientsSecretsApi.AddClientSecretWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **iMSAdminApiV1ClientsAddClientSecretRequest** | [**IMSAdminApiV1ClientsAddClientSecretRequest**](IMSAdminApiV1ClientsAddClientSecretRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientSecretAddedResponse**](IMSAdminApiV1ClientsClientSecretAddedResponse.md)

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

<a id="regenerateonerosterapiclientsecretasync"></a>
# **RegenerateOneRosterApiClientSecretAsync**
> IMSAdminApiV1ClientsClientSecretRegeneratedResponse RegenerateOneRosterApiClientSecretAsync (string tenantId, string instanceId, string clientId, IMSAdminApiV1ClientsRegenerateClientSecretRequest iMSAdminApiV1ClientsRegenerateClientSecretRequest = null)

Regenerate Client Secret

### Example
```csharp
using System.Collections.Generic;
using System.Diagnostics;
using EdGraph.Platform.Client.Api;
using EdGraph.Platform.Client.Client;
using EdGraph.Platform.Client.Model;

namespace Example
{
    public class RegenerateOneRosterApiClientSecretAsyncExample
    {
        public static void Main()
        {
            Configuration config = new Configuration();
            config.BasePath = "https://api.dev.edgraph.com/tenant";
            // Configure OAuth2 access token for authorization: oauth2
            config.AccessToken = "YOUR_ACCESS_TOKEN";

            var apiInstance = new ClientsSecretsApi(config);
            var tenantId = "tenantId_example";  // string | 
            var instanceId = "instanceId_example";  // string | 
            var clientId = "clientId_example";  // string | 
            var iMSAdminApiV1ClientsRegenerateClientSecretRequest = new IMSAdminApiV1ClientsRegenerateClientSecretRequest(); // IMSAdminApiV1ClientsRegenerateClientSecretRequest |  (optional) 

            try
            {
                // Regenerate Client Secret
                IMSAdminApiV1ClientsClientSecretRegeneratedResponse result = apiInstance.RegenerateOneRosterApiClientSecretAsync(tenantId, instanceId, clientId, iMSAdminApiV1ClientsRegenerateClientSecretRequest);
                Debug.WriteLine(result);
            }
            catch (ApiException  e)
            {
                Debug.Print("Exception when calling ClientsSecretsApi.RegenerateOneRosterApiClientSecretAsync: " + e.Message);
                Debug.Print("Status Code: " + e.ErrorCode);
                Debug.Print(e.StackTrace);
            }
        }
    }
}
```

#### Using the RegenerateOneRosterApiClientSecretAsyncWithHttpInfo variant
This returns an ApiResponse object which contains the response data, status code and headers.

```csharp
try
{
    // Regenerate Client Secret
    ApiResponse<IMSAdminApiV1ClientsClientSecretRegeneratedResponse> response = apiInstance.RegenerateOneRosterApiClientSecretAsyncWithHttpInfo(tenantId, instanceId, clientId, iMSAdminApiV1ClientsRegenerateClientSecretRequest);
    Debug.Write("Status Code: " + response.StatusCode);
    Debug.Write("Response Headers: " + response.Headers);
    Debug.Write("Response Body: " + response.Data);
}
catch (ApiException e)
{
    Debug.Print("Exception when calling ClientsSecretsApi.RegenerateOneRosterApiClientSecretAsyncWithHttpInfo: " + e.Message);
    Debug.Print("Status Code: " + e.ErrorCode);
    Debug.Print(e.StackTrace);
}
```

### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **instanceId** | **string** |  |  |
| **clientId** | **string** |  |  |
| **iMSAdminApiV1ClientsRegenerateClientSecretRequest** | [**IMSAdminApiV1ClientsRegenerateClientSecretRequest**](IMSAdminApiV1ClientsRegenerateClientSecretRequest.md) |  | [optional]  |

### Return type

[**IMSAdminApiV1ClientsClientSecretRegeneratedResponse**](IMSAdminApiV1ClientsClientSecretRegeneratedResponse.md)

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

