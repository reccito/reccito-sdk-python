# reccito_sdk.MerchantAssetsApi

All URIs are relative to *https://api.reccito.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_organisation_assets**](MerchantAssetsApi.md#list_organisation_assets) | **GET** /api/v1/merchant/assets/list | List organisation assets
[**upload_organisation_banner**](MerchantAssetsApi.md#upload_organisation_banner) | **POST** /api/v1/merchant/assets/upload/banner | Upload organisation banner
[**upload_organisation_logo**](MerchantAssetsApi.md#upload_organisation_logo) | **POST** /api/v1/merchant/assets/upload/logo | Upload organisation logo
[**upload_store_logo**](MerchantAssetsApi.md#upload_store_logo) | **POST** /api/v1/merchant/assets/upload/store/logo | Upload store logo


# **list_organisation_assets**
> ApiResponse list_organisation_assets(asset_type=asset_type)

List organisation assets

List all branding assets uploaded for the organisation.

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.api_response import ApiResponse
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
    api_instance = reccito_sdk.MerchantAssetsApi(api_client)
    asset_type = 'asset_type_example' # str |  (optional)

    try:
        # List organisation assets
        api_response = api_instance.list_organisation_assets(asset_type=asset_type)
        print("The response of MerchantAssetsApi->list_organisation_assets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantAssetsApi->list_organisation_assets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **asset_type** | **str**|  | [optional] 

### Return type

[**ApiResponse**](ApiResponse.md)

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

# **upload_organisation_banner**
> ApiResponse upload_organisation_banner(file)

Upload organisation banner

Upload a banner file for the organisation. Supported formats: JPEG, PNG, WebP. Max 5MB.

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.api_response import ApiResponse
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
    api_instance = reccito_sdk.MerchantAssetsApi(api_client)
    file = None # bytes | Banner file to upload

    try:
        # Upload organisation banner
        api_response = api_instance.upload_organisation_banner(file)
        print("The response of MerchantAssetsApi->upload_organisation_banner:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantAssetsApi->upload_organisation_banner: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **bytes**| Banner file to upload | 

### Return type

[**ApiResponse**](ApiResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_organisation_logo**
> ApiResponse upload_organisation_logo(file)

Upload organisation logo

Upload a logo file for the organisation. Supported formats: JPEG, PNG, WebP, SVG. Max 5MB.

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.api_response import ApiResponse
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
    api_instance = reccito_sdk.MerchantAssetsApi(api_client)
    file = None # bytes | Logo file to upload

    try:
        # Upload organisation logo
        api_response = api_instance.upload_organisation_logo(file)
        print("The response of MerchantAssetsApi->upload_organisation_logo:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantAssetsApi->upload_organisation_logo: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **bytes**| Logo file to upload | 

### Return type

[**ApiResponse**](ApiResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_store_logo**
> ApiResponse upload_store_logo(store_id, file)

Upload store logo

Upload a logo file for a specific store. Supported formats: JPEG, PNG, WebP, SVG. Max 5MB.

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.api_response import ApiResponse
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
    api_instance = reccito_sdk.MerchantAssetsApi(api_client)
    store_id = 'store_id_example' # str | 
    file = None # bytes | Store logo file to upload

    try:
        # Upload store logo
        api_response = api_instance.upload_store_logo(store_id, file)
        print("The response of MerchantAssetsApi->upload_store_logo:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantAssetsApi->upload_store_logo: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **store_id** | **str**|  | 
 **file** | **bytes**| Store logo file to upload | 

### Return type

[**ApiResponse**](ApiResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful Response |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

