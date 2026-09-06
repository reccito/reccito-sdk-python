# ReceiptListResponse

Receipt list response with pagination (merchant audience).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**receipts** | [**List[ReceiptSummary]**](ReceiptSummary.md) |  | 
**total** | **int** |  | 
**page** | **int** |  | 
**limit** | **int** |  | 
**has_next** | **bool** |  | 
**has_prev** | **bool** |  | 

## Example

```python
from reccito_sdk.models.receipt_list_response import ReceiptListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptListResponse from a JSON string
receipt_list_response_instance = ReceiptListResponse.from_json(json)
# print the JSON string representation of the object
print(ReceiptListResponse.to_json())

# convert the object into a dict
receipt_list_response_dict = receipt_list_response_instance.to_dict()
# create an instance of ReceiptListResponse from a dict
receipt_list_response_from_dict = ReceiptListResponse.from_dict(receipt_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


