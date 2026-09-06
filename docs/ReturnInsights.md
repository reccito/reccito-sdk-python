# ReturnInsights

Return-centric actionable insights.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**returnable** | **bool** |  | [optional] 
**return_window_days** | **int** |  | [optional] 
**return_deadline** | **datetime** |  | [optional] 
**days_left** | **int** |  | [optional] 
**policy_summary** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.return_insights import ReturnInsights

# TODO update the JSON string below
json = "{}"
# create an instance of ReturnInsights from a JSON string
return_insights_instance = ReturnInsights.from_json(json)
# print the JSON string representation of the object
print(ReturnInsights.to_json())

# convert the object into a dict
return_insights_dict = return_insights_instance.to_dict()
# create an instance of ReturnInsights from a dict
return_insights_from_dict = ReturnInsights.from_dict(return_insights_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


