# StoreListResponse

Store list response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stores** | [**List[StoreResponse]**](StoreResponse.md) |  | 
**total** | **int** |  | 

## Example

```python
from reccito_sdk.models.store_list_response import StoreListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of StoreListResponse from a JSON string
store_list_response_instance = StoreListResponse.from_json(json)
# print the JSON string representation of the object
print(StoreListResponse.to_json())

# convert the object into a dict
store_list_response_dict = store_list_response_instance.to_dict()
# create an instance of StoreListResponse from a dict
store_list_response_from_dict = StoreListResponse.from_dict(store_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


