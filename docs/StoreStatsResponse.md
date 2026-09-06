# StoreStatsResponse

Store statistics.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**store_id** | **str** |  | 
**store_name** | **str** |  | 
**receipts_created_count** | **int** |  | 
**receipts_created_today** | **int** |  | 
**receipts_created_this_month** | **int** |  | 
**qr_scans_count** | **int** |  | 
**qr_scans_today** | **int** |  | 
**qr_scans_this_month** | **int** |  | 
**total_amount_this_month** | **str** |  | 
**average_receipt_amount** | **str** |  | 
**last_receipt_created** | **datetime** |  | [optional] 
**busiest_hour** | **str** |  | [optional] 
**busiest_day** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.store_stats_response import StoreStatsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of StoreStatsResponse from a JSON string
store_stats_response_instance = StoreStatsResponse.from_json(json)
# print the JSON string representation of the object
print(StoreStatsResponse.to_json())

# convert the object into a dict
store_stats_response_dict = store_stats_response_instance.to_dict()
# create an instance of StoreStatsResponse from a dict
store_stats_response_from_dict = StoreStatsResponse.from_dict(store_stats_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


