# reccito_sdk.MerchantReceiptsApi

All URIs are relative to *https://api.reccito.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_receipt**](MerchantReceiptsApi.md#create_receipt) | **POST** /api/v1/merchant/receipts | Create Receipt
[**get_receipt**](MerchantReceiptsApi.md#get_receipt) | **GET** /api/v1/merchant/receipts/{receipt_id} | Get Receipt
[**list_receipts**](MerchantReceiptsApi.md#list_receipts) | **GET** /api/v1/merchant/receipts | List Receipts
[**refresh_receipt_qr**](MerchantReceiptsApi.md#refresh_receipt_qr) | **PUT** /api/v1/merchant/receipts/{receipt_id}/refresh-qr | Refresh Qr Code


# **create_receipt**
> ReceiptImmediateResponse create_receipt(receipt_create)

Create Receipt

Create a new receipt. Synchronous: the receipt is durably persisted
before this returns (see ReceiptService.create_receipt_synchronously).
A retry with the same dedupe_key returns the original receipt with 200,
not an error (idempotent replay, Stripe-style).

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.receipt_create import ReceiptCreate
from reccito_sdk.models.receipt_immediate_response import ReceiptImmediateResponse
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
    api_instance = reccito_sdk.MerchantReceiptsApi(api_client)
    receipt_create = reccito_sdk.ReceiptCreate() # ReceiptCreate | 

    try:
        # Create Receipt
        api_response = api_instance.create_receipt(receipt_create)
        print("The response of MerchantReceiptsApi->create_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantReceiptsApi->create_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **receipt_create** | [**ReceiptCreate**](ReceiptCreate.md)|  | 

### Return type

[**ReceiptImmediateResponse**](ReceiptImmediateResponse.md)

### Authorization

[ApiKeyAuth](../README.md#ApiKeyAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Successful Response |  -  |
**200** | Idempotent replay: a receipt with this organisation + dedupe_key already existed. Returns the original receipt unchanged, not an error. |  -  |
**422** | Validation Error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_receipt**
> MerchantReceiptResponse get_receipt(receipt_id)

Get Receipt

Get receipt by ID.

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.merchant_receipt_response import MerchantReceiptResponse
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
    api_instance = reccito_sdk.MerchantReceiptsApi(api_client)
    receipt_id = 'receipt_id_example' # str | 

    try:
        # Get Receipt
        api_response = api_instance.get_receipt(receipt_id)
        print("The response of MerchantReceiptsApi->get_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantReceiptsApi->get_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **receipt_id** | **str**|  | 

### Return type

[**MerchantReceiptResponse**](MerchantReceiptResponse.md)

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

# **list_receipts**
> ReceiptListResponse list_receipts(page=page, limit=limit, store_id=store_id, status=status, search=search, sort_by=sort_by, sort_order=sort_order)

List Receipts

List receipts with filters and pagination.

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.receipt_list_response import ReceiptListResponse
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
    api_instance = reccito_sdk.MerchantReceiptsApi(api_client)
    page = 1 # int |  (optional) (default to 1)
    limit = 50 # int |  (optional) (default to 50)
    store_id = 'store_id_example' # str |  (optional)
    status = 'status_example' # str |  (optional)
    search = 'search_example' # str |  (optional)
    sort_by = 'created_at' # str |  (optional) (default to 'created_at')
    sort_order = 'desc' # str |  (optional) (default to 'desc')

    try:
        # List Receipts
        api_response = api_instance.list_receipts(page=page, limit=limit, store_id=store_id, status=status, search=search, sort_by=sort_by, sort_order=sort_order)
        print("The response of MerchantReceiptsApi->list_receipts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantReceiptsApi->list_receipts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] [default to 1]
 **limit** | **int**|  | [optional] [default to 50]
 **store_id** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 
 **search** | **str**|  | [optional] 
 **sort_by** | **str**|  | [optional] [default to &#39;created_at&#39;]
 **sort_order** | **str**|  | [optional] [default to &#39;desc&#39;]

### Return type

[**ReceiptListResponse**](ReceiptListResponse.md)

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

# **refresh_receipt_qr**
> QRRefreshResponse refresh_receipt_qr(receipt_id)

Refresh Qr Code

Refresh QR code for a receipt.

### Example

* Bearer (API Key) Authentication (ApiKeyAuth):

```python
import reccito_sdk
from reccito_sdk.models.qr_refresh_response import QRRefreshResponse
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
    api_instance = reccito_sdk.MerchantReceiptsApi(api_client)
    receipt_id = 'receipt_id_example' # str | 

    try:
        # Refresh Qr Code
        api_response = api_instance.refresh_receipt_qr(receipt_id)
        print("The response of MerchantReceiptsApi->refresh_receipt_qr:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MerchantReceiptsApi->refresh_receipt_qr: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **receipt_id** | **str**|  | 

### Return type

[**QRRefreshResponse**](QRRefreshResponse.md)

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

