# ReceiptItemCreate

Receipt line item creation.

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
from reccito_sdk.models.receipt_item_create import ReceiptItemCreate

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptItemCreate from a JSON string
receipt_item_create_instance = ReceiptItemCreate.from_json(json)
# print the JSON string representation of the object
print(ReceiptItemCreate.to_json())

# convert the object into a dict
receipt_item_create_dict = receipt_item_create_instance.to_dict()
# create an instance of ReceiptItemCreate from a dict
receipt_item_create_from_dict = ReceiptItemCreate.from_dict(receipt_item_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


