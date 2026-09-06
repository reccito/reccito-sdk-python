# StoreUpdate

Store update request.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**address_line_1** | **str** |  | [optional] 
**address_line_2** | **str** |  | [optional] 
**city** | **str** |  | [optional] 
**state** | **str** |  | [optional] 
**postal_code** | **str** |  | [optional] 
**country** | **str** |  | [optional] 
**latitude** | **str** |  | [optional] 
**longitude** | **str** |  | [optional] 
**phone** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**manager_name** | **str** |  | [optional] 
**timezone** | **str** |  | [optional] 
**default_qr_expiry_minutes** | **int** |  | [optional] 
**logo_url** | **str** |  | [optional] 
**primary_color** | **str** |  | [optional] 
**is_active** | **bool** |  | [optional] 
**opening_hours** | **Dict[str, object]** |  | [optional] 
**custom_metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from reccito_sdk.models.store_update import StoreUpdate

# TODO update the JSON string below
json = "{}"
# create an instance of StoreUpdate from a JSON string
store_update_instance = StoreUpdate.from_json(json)
# print the JSON string representation of the object
print(StoreUpdate.to_json())

# convert the object into a dict
store_update_dict = store_update_instance.to_dict()
# create an instance of StoreUpdate from a dict
store_update_from_dict = StoreUpdate.from_dict(store_update_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


