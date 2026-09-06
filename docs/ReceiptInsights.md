# ReceiptInsights

Actionable insights derived from receipt text.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**return_window_days** | **int** |  | [optional] 
**return_deadline** | **datetime** |  | [optional] 
**refund_eligible** | **bool** |  | [optional] 
**warranty_items** | [**List[WarrantyInfo]**](WarrantyInfo.md) |  | [optional] 

## Example

```python
from reccito_sdk.models.receipt_insights import ReceiptInsights

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptInsights from a JSON string
receipt_insights_instance = ReceiptInsights.from_json(json)
# print the JSON string representation of the object
print(ReceiptInsights.to_json())

# convert the object into a dict
receipt_insights_dict = receipt_insights_instance.to_dict()
# create an instance of ReceiptInsights from a dict
receipt_insights_from_dict = ReceiptInsights.from_dict(receipt_insights_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


