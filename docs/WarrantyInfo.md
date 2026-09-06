# WarrantyInfo

Warranty metadata for line-items/receipt.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**item_name** | **str** |  | [optional] 
**warranty_terms** | **str** |  | [optional] 
**warranty_end_date** | **datetime** |  | [optional] 
**reference** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.warranty_info import WarrantyInfo

# TODO update the JSON string below
json = "{}"
# create an instance of WarrantyInfo from a JSON string
warranty_info_instance = WarrantyInfo.from_json(json)
# print the JSON string representation of the object
print(WarrantyInfo.to_json())

# convert the object into a dict
warranty_info_dict = warranty_info_instance.to_dict()
# create an instance of WarrantyInfo from a dict
warranty_info_from_dict = WarrantyInfo.from_dict(warranty_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


