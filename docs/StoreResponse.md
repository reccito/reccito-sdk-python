# StoreResponse

Store response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**code** | **str** |  | 
**description** | **str** |  | [optional] 
**organisation_id** | **str** |  | 
**address_line_1** | **str** |  | [optional] 
**address_line_2** | **str** |  | [optional] 
**city** | **str** |  | [optional] 
**state** | **str** |  | [optional] 
**postal_code** | **str** |  | [optional] 
**country** | **str** |  | 
**full_address** | **str** |  | 
**latitude** | **str** |  | [optional] 
**longitude** | **str** |  | [optional] 
**phone** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**manager_name** | **str** |  | [optional] 
**timezone** | **str** |  | [optional] 
**default_qr_expiry_minutes** | **int** |  | [optional] 
**effective_qr_expiry** | **int** |  | 
**logo_url** | **str** |  | [optional] 
**primary_color** | **str** |  | [optional] 
**effective_logo_url** | **str** |  | [optional] 
**effective_primary_color** | **str** |  | [optional] 
**is_active** | **bool** |  | 
**opening_hours** | **Dict[str, object]** |  | [optional] 
**receipts_created_count** | **int** |  | 
**last_receipt_created** | **datetime** |  | [optional] 
**custom_metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from reccito_sdk.models.store_response import StoreResponse

# TODO update the JSON string below
json = "{}"
# create an instance of StoreResponse from a JSON string
store_response_instance = StoreResponse.from_json(json)
# print the JSON string representation of the object
print(StoreResponse.to_json())

# convert the object into a dict
store_response_dict = store_response_instance.to_dict()
# create an instance of StoreResponse from a dict
store_response_from_dict = StoreResponse.from_dict(store_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


