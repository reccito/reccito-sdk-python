# ReceiptItemResponse

Receipt line item response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**quantity** | **int** |  | 
**unit_price** | **str** |  | 
**total_price** | **str** |  | 
**description** | **str** |  | [optional] 
**sku** | **str** |  | [optional] 
**category** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.receipt_item_response import ReceiptItemResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptItemResponse from a JSON string
receipt_item_response_instance = ReceiptItemResponse.from_json(json)
# print the JSON string representation of the object
print(ReceiptItemResponse.to_json())

# convert the object into a dict
receipt_item_response_dict = receipt_item_response_instance.to_dict()
# create an instance of ReceiptItemResponse from a dict
receipt_item_response_from_dict = ReceiptItemResponse.from_dict(receipt_item_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


