# OfferPolicyInfo

Offer metadata with optional validity window.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**offer_text** | **str** |  | 
**offer_end_date** | **datetime** |  | [optional] 
**terms** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.offer_policy_info import OfferPolicyInfo

# TODO update the JSON string below
json = "{}"
# create an instance of OfferPolicyInfo from a JSON string
offer_policy_info_instance = OfferPolicyInfo.from_json(json)
# print the JSON string representation of the object
print(OfferPolicyInfo.to_json())

# convert the object into a dict
offer_policy_info_dict = offer_policy_info_instance.to_dict()
# create an instance of OfferPolicyInfo from a dict
offer_policy_info_from_dict = OfferPolicyInfo.from_dict(offer_policy_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


