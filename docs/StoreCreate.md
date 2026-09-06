# StoreCreate

Store creation request.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**code** | **str** |  | 
**description** | **str** |  | [optional] 
**address_line_1** | **str** |  | [optional] 
**address_line_2** | **str** |  | [optional] 
**city** | **str** |  | [optional] 
**state** | **str** |  | [optional] 
**postal_code** | **str** |  | [optional] 
**country** | **str** |  | [optional] [default to 'US']
**latitude** | **str** |  | [optional] 
**longitude** | **str** |  | [optional] 
**phone** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**manager_name** | **str** |  | [optional] 
**timezone** | **str** |  | [optional] 
**default_qr_expiry_minutes** | **int** |  | [optional] 
**logo_url** | **str** |  | [optional] 
**primary_color** | **str** |  | [optional] 
**opening_hours** | **Dict[str, object]** |  | [optional] 
**custom_metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from reccito_sdk.models.store_create import StoreCreate

# TODO update the JSON string below
json = "{}"
# create an instance of StoreCreate from a JSON string
store_create_instance = StoreCreate.from_json(json)
# print the JSON string representation of the object
print(StoreCreate.to_json())

# convert the object into a dict
store_create_dict = store_create_instance.to_dict()
# create an instance of StoreCreate from a dict
store_create_from_dict = StoreCreate.from_dict(store_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


