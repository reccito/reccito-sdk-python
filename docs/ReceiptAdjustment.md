# ReceiptAdjustment

Price adjustment on line-item or receipt total.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scope** | **str** |  | [optional] [default to 'receipt']
**kind** | **str** |  | 
**label** | **str** |  | [optional] 
**amount** | **str** |  | 
**item_name** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.receipt_adjustment import ReceiptAdjustment

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptAdjustment from a JSON string
receipt_adjustment_instance = ReceiptAdjustment.from_json(json)
# print the JSON string representation of the object
print(ReceiptAdjustment.to_json())

# convert the object into a dict
receipt_adjustment_dict = receipt_adjustment_instance.to_dict()
# create an instance of ReceiptAdjustment from a dict
receipt_adjustment_from_dict = ReceiptAdjustment.from_dict(receipt_adjustment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


