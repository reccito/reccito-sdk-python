# reccito_sdk.MerchantStoresApi

All URIs are relative to *https://api.reccito.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_store**](MerchantStoresApi.md#create_store) | **POST** /api/v1/merchant/stores | Create Store
[**get_store**](MerchantStoresApi.md#get_store) | **GET** /api/v1/merchant/stores/{store_id} | Get Store
[**get_store_stats**](MerchantStoresApi.md#get_store_stats) | **GET** /api/v1/merchant/stores/{store_id}/stats | Get Store Stats
[**list_stores**](MerchantStoresApi.md#list_stores) | **GET** /api/v1/merchant/stores | List Stores
[**update_store**](MerchantStoresApi.md#update_store) | **PUT** /api/v1/merchant/stores/{store_id} | Update Store


# **create_store**
> StoreResponse create_store(store_create)

Create Store

Create a new store for the organisation.

**Authentication:** Required (Organisation bearer token)

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.store_create import StoreCreate
from reccito_sdk.models.store_response import StoreResponse
from reccito_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.reccito.com
# See configuration.py for a list of all supported configuration parameters.
configuration = reccito_sdk.Configuration(
    host = "https://api.reccito.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (API Key): ApiKeyAuth
configuration = reccito_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with reccito_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = reccito_sdk.MerchantStoresApi(api_client)
    store_create = reccito_sdk.StoreCreate() # StoreCreate | 

    try:
        # Create Store
        api_response = api_instance.create_store(store_create)
        print("The response of MerchantStoresApi->create_store:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantStoresApi->create_store: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_create** | [**StoreCreate**](StoreCreate.md)|  | 

### Return type

[**StoreResponse**](StoreResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_store**
> StoreResponse get_store(store_id)

Get Store

Get a specific store by ID.

**Authentication:** Required (Organisation bearer token)

**Path Parameters:**
- `store_id`: UUID of the store

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.store_response import StoreResponse
from reccito_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.reccito.com
# See configuration.py for a list of all supported configuration parameters.
configuration = reccito_sdk.Configuration(
    host = "https://api.reccito.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (API Key): ApiKeyAuth
configuration = reccito_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with reccito_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = reccito_sdk.MerchantStoresApi(api_client)
    store_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 

    try:
        # Get Store
        api_response = api_instance.get_store(store_id)
        print("The response of MerchantStoresApi->get_store:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantStoresApi->get_store: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_id** | **UUID**|  | 

### Return type

[**StoreResponse**](StoreResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_store_stats**
> StoreStatsResponse get_store_stats(store_id)

Get Store Stats

Get statistics for a store.

**Authentication:** Required (Organisation bearer token)

**Path Parameters:**
- `store_id`: UUID of the store

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.store_stats_response import StoreStatsResponse
from reccito_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.reccito.com
# See configuration.py for a list of all supported configuration parameters.
configuration = reccito_sdk.Configuration(
    host = "https://api.reccito.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (API Key): ApiKeyAuth
configuration = reccito_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with reccito_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = reccito_sdk.MerchantStoresApi(api_client)
    store_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 

    try:
        # Get Store Stats
        api_response = api_instance.get_store_stats(store_id)
        print("The response of MerchantStoresApi->get_store_stats:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantStoresApi->get_store_stats: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_id** | **UUID**|  | 

### Return type

[**StoreStatsResponse**](StoreStatsResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_stores**
> StoreListResponse list_stores(skip=skip, limit=limit, is_active=is_active, q=q)

List Stores

List all stores for the organisation.

**Authentication:** Required (Organisation bearer token)

**Query Parameters:**
- `skip`: Number of stores to skip (default: 0)
- `limit`: Number of stores to return (default: 100, max: 1000)
- `is_active`: Filter by active status (optional)
- `q`: Search by store name/code/city/email/phone (optional)

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.store_list_response import StoreListResponse
from reccito_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.reccito.com
# See configuration.py for a list of all supported configuration parameters.
configuration = reccito_sdk.Configuration(
    host = "https://api.reccito.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (API Key): ApiKeyAuth
configuration = reccito_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with reccito_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = reccito_sdk.MerchantStoresApi(api_client)
    skip = 0 # int |  (optional) (default to 0)
    limit = 100 # int |  (optional) (default to 100)
    is_active = True # bool |  (optional)
    q = 'q_example' # str |  (optional)

    try:
        # List Stores
        api_response = api_instance.list_stores(skip=skip, limit=limit, is_active=is_active, q=q)
        print("The response of MerchantStoresApi->list_stores:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantStoresApi->list_stores: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **skip** | **int**|  | [optional] [default to 0]
 **limit** | **int**|  | [optional] [default to 100]
 **is_active** | **bool**|  | [optional] 
 **q** | **str**|  | [optional] 

### Return type

[**StoreListResponse**](StoreListResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_store**
> StoreResponse update_store(store_id, store_update)

Update Store

Update a store.

**Authentication:** Required (Organisation bearer token)

**Path Parameters:**
- `store_id`: UUID of the store

**Request Body:** Updated store fields (all optional)

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.store_response import StoreResponse
from reccito_sdk.models.store_update import StoreUpdate
from reccito_sdk.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.reccito.com
# See configuration.py for a list of all supported configuration parameters.
configuration = reccito_sdk.Configuration(
    host = "https://api.reccito.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (API Key): ApiKeyAuth
configuration = reccito_sdk.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with reccito_sdk.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = reccito_sdk.MerchantStoresApi(api_client)
    store_id = UUID('38400000-8cf0-11bd-b23e-10b96e4ef00d') # UUID | 
    store_update = reccito_sdk.StoreUpdate() # StoreUpdate | 

    try:
        # Update Store
        api_response = api_instance.update_store(store_id, store_update)
        print("The response of MerchantStoresApi->update_store:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantStoresApi->update_store: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_id** | **UUID**|  | 
 **store_update** | [**StoreUpdate**](StoreUpdate.md)|  | 

### Return type

[**StoreResponse**](StoreResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

