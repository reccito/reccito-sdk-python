# PaginationInfo

Pagination information for list responses.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** | Current page number | 
**limit** | **int** | Items per page | 
**total** | **int** | Total number of items | 
**has_next** | **bool** | Whether there is a next page | 

## Example

```python
from reccito_sdk.models.pagination_info import PaginationInfo

# TODO update the JSON string below
json = "{}"
# create an instance of PaginationInfo from a JSON string
pagination_info_instance = PaginationInfo.from_json(json)
# print the JSON string representation of the object
print(PaginationInfo.to_json())

# convert the object into a dict
pagination_info_dict = pagination_info_instance.to_dict()
# create an instance of PaginationInfo from a dict
pagination_info_from_dict = PaginationInfo.from_dict(pagination_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


