# EdGraph.Platform.Client.Api.CollectionsApi

All URIs are relative to *https://api.dev.edgraph.com/tenant*

| Method | HTTP request | Description |
|--------|--------------|-------------|
| [**CreateCollection**](CollectionsApi.md#createcollection) | **POST** /tenants/{tenantId}/validations/collections | Creates a Collection. |
| [**CreateContainer**](CollectionsApi.md#createcontainer) | **POST** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Creates a Container. |
| [**DeleteCollection**](CollectionsApi.md#deletecollection) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId} | Deletes a Collection. |
| [**DeleteContainer**](CollectionsApi.md#deletecontainer) | **DELETE** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Deletes a Container. |
| [**GetCollectionById**](CollectionsApi.md#getcollectionbyid) | **GET** /tenants/{tenantId}/validations/collections/{collectionId} | Retrieves a Collection by ID. |
| [**GetCollectionJson**](CollectionsApi.md#getcollectionjson) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/export | Retrieves the JSON representation of a Collection. Useful for exporting into other systems. |
| [**GetCollections**](CollectionsApi.md#getcollections) | **GET** /tenants/{tenantId}/validations/collections | Retrieves a list of Collections. |
| [**GetCollectionsTree**](CollectionsApi.md#getcollectionstree) | **GET** /tenants/{tenantId}/validations/categories/tree | Retrieves a list of Collections. |
| [**GetContainerById**](CollectionsApi.md#getcontainerbyid) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Retrieves a Container by ID. |
| [**GetContainers**](CollectionsApi.md#getcontainers) | **GET** /tenants/{tenantId}/validations/collections/{collectionId}/containers | Retrieves a list of Containers. |
| [**UpdateCollection**](CollectionsApi.md#updatecollection) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId} | Updates a Collection. |
| [**UpdateContainer**](CollectionsApi.md#updatecontainer) | **PUT** /tenants/{tenantId}/validations/collections/{collectionId}/containers/{containerId} | Updates a Container. |
| [**UploadCollectionJson**](CollectionsApi.md#uploadcollectionjson) | **POST** /tenants/{tenantId}/validations/collections/import | Uploads a Collection JSON. Useful for importing from another system. |

<a id="createcollection"></a>
# **CreateCollection**
> ValidationsApiCoreV1CreatedResponse CreateCollection (string tenantId, ValidationsApiContainersV1CreateCollectionRequest validationsApiContainersV1CreateCollectionRequest = null)

Creates a Collection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **validationsApiContainersV1CreateCollectionRequest** | [**ValidationsApiContainersV1CreateCollectionRequest**](ValidationsApiContainersV1CreateCollectionRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiCoreV1CreatedResponse**](ValidationsApiCoreV1CreatedResponse.md)

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="createcontainer"></a>
# **CreateContainer**
> ValidationsApiCoreV1CreatedResponse CreateContainer (string tenantId, string collectionId, ValidationsApiContainersV1CreateContainerRequest validationsApiContainersV1CreateContainerRequest = null)

Creates a Container.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |
| **validationsApiContainersV1CreateContainerRequest** | [**ValidationsApiContainersV1CreateContainerRequest**](ValidationsApiContainersV1CreateContainerRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiCoreV1CreatedResponse**](ValidationsApiCoreV1CreatedResponse.md)

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

<a id="deletecollection"></a>
# **DeleteCollection**
> void DeleteCollection (string tenantId, string collectionId)

Deletes a Collection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |

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

<a id="deletecontainer"></a>
# **DeleteContainer**
> void DeleteContainer (string tenantId, string collectionId, string containerId)

Deletes a Container.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |
| **containerId** | **string** |  |  |

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

<a id="getcollectionbyid"></a>
# **GetCollectionById**
> ValidationsApiContainersV1ContainerDto GetCollectionById (string tenantId, string collectionId)

Retrieves a Collection by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |

### Return type

[**ValidationsApiContainersV1ContainerDto**](ValidationsApiContainersV1ContainerDto.md)

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

<a id="getcollectionjson"></a>
# **GetCollectionJson**
> ValidationsApiContainersV1GetJsonResponse GetCollectionJson (string tenantId, string collectionId)

Retrieves the JSON representation of a Collection. Useful for exporting into other systems.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |

### Return type

[**ValidationsApiContainersV1GetJsonResponse**](ValidationsApiContainersV1GetJsonResponse.md)

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

<a id="getcollections"></a>
# **GetCollections**
> ValidationsApiContainersV1PaginatedContainers GetCollections (string tenantId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Collections.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

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

<a id="getcollectionstree"></a>
# **GetCollectionsTree**
> ValidationsApiContainersV1PaginatedCategoryTreeResponse GetCollectionsTree (string tenantId, int pageIndex = null, int pageSize = null, string orderBy = null, string categoryId = null, string categoryName = null, string subCategoryId = null, string subCategoryName = null)

Retrieves a list of Collections.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **orderBy** | **string** |  | [optional]  |
| **categoryId** | **string** |  | [optional]  |
| **categoryName** | **string** |  | [optional]  |
| **subCategoryId** | **string** |  | [optional]  |
| **subCategoryName** | **string** |  | [optional]  |

### Return type

[**ValidationsApiContainersV1PaginatedCategoryTreeResponse**](ValidationsApiContainersV1PaginatedCategoryTreeResponse.md)

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

<a id="getcontainerbyid"></a>
# **GetContainerById**
> ValidationsApiContainersV1ContainerDto GetContainerById (string tenantId, string collectionId, string containerId)

Retrieves a Container by ID.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |
| **containerId** | **string** |  |  |

### Return type

[**ValidationsApiContainersV1ContainerDto**](ValidationsApiContainersV1ContainerDto.md)

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

<a id="getcontainers"></a>
# **GetContainers**
> ValidationsApiContainersV1PaginatedContainers GetContainers (string tenantId, string collectionId, int pageIndex = null, int pageSize = null, string filter = null, string orderBy = null)

Retrieves a list of Containers.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |
| **pageIndex** | **int** |  | [optional] [default to 0] |
| **pageSize** | **int** |  | [optional] [default to 10] |
| **filter** | **string** |  | [optional]  |
| **orderBy** | **string** |  | [optional]  |

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

<a id="updatecollection"></a>
# **UpdateCollection**
> void UpdateCollection (string tenantId, string collectionId, ValidationsApiContainersV1UpdateCollectionRequest validationsApiContainersV1UpdateCollectionRequest = null)

Updates a Collection.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |
| **validationsApiContainersV1UpdateCollectionRequest** | [**ValidationsApiContainersV1UpdateCollectionRequest**](ValidationsApiContainersV1UpdateCollectionRequest.md) |  | [optional]  |

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

<a id="updatecontainer"></a>
# **UpdateContainer**
> void UpdateContainer (string tenantId, string collectionId, string containerId, ValidationsApiContainersV1UpdateContainerRequest validationsApiContainersV1UpdateContainerRequest = null)

Updates a Container.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **collectionId** | **string** |  |  |
| **containerId** | **string** |  |  |
| **validationsApiContainersV1UpdateContainerRequest** | [**ValidationsApiContainersV1UpdateContainerRequest**](ValidationsApiContainersV1UpdateContainerRequest.md) |  | [optional]  |

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

<a id="uploadcollectionjson"></a>
# **UploadCollectionJson**
> ValidationsApiContainersV1CollectionUploadedResponse UploadCollectionJson (string tenantId, ValidationsApiContainersV1UploadCollectionRequest validationsApiContainersV1UploadCollectionRequest = null)

Uploads a Collection JSON. Useful for importing from another system.


### Parameters

| Name | Type | Description | Notes |
|------|------|-------------|-------|
| **tenantId** | **string** |  |  |
| **validationsApiContainersV1UploadCollectionRequest** | [**ValidationsApiContainersV1UploadCollectionRequest**](ValidationsApiContainersV1UploadCollectionRequest.md) |  | [optional]  |

### Return type

[**ValidationsApiContainersV1CollectionUploadedResponse**](ValidationsApiContainersV1CollectionUploadedResponse.md)

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
| **201** | The resource was created. The location of the resource is available in the Location header of the response. |  -  |
| **400** | Bad Request. The request was invalid and cannot be completed. See the response body for specific validation errors. This will typically be an issue with the query parameters or the request body values. |  -  |

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

