# ApiResponse

Standard API response format.  All API responses should follow this format for consistency. The 'data' field contains the response payload, while 'error' is populated when an error occurs. Pagination is included for list endpoints.  Example:     Success response:     {         \"data\": {\"id\": \"123\", \"name\": \"Logo\"},         \"pagination\": {\"page\": 1, \"limit\": 10, \"total\": 100, \"has_next\": true}     }      Error response:     {         \"error\": {             \"code\": \"VALIDATION_ERROR\",             \"message\": \"File size exceeds 5MB limit\",             \"details\": {\"max_size\": \"5242880\"}         }     }

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | **Dict[str, object]** | Response payload data | [optional] 
**error** | [**ErrorDetail**](ErrorDetail.md) | Error information | [optional] 
**pagination** | [**PaginationInfo**](PaginationInfo.md) | Pagination information for list responses | [optional] 

## Example

```python
from reccito_sdk.models.api_response import ApiResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ApiResponse from a JSON string
api_response_instance = ApiResponse.from_json(json)
# print the JSON string representation of the object
print(ApiResponse.to_json())

# convert the object into a dict
api_response_dict = api_response_instance.to_dict()
# create an instance of ApiResponse from a dict
api_response_from_dict = ApiResponse.from_dict(api_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


