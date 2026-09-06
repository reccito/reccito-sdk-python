# PaymentInfoCreate

Payment information.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **str** |  | 
**amount** | **str** |  | 
**card_last_four** | **str** |  | [optional] 
**reference** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.payment_info_create import PaymentInfoCreate

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentInfoCreate from a JSON string
payment_info_create_instance = PaymentInfoCreate.from_json(json)
# print the JSON string representation of the object
print(PaymentInfoCreate.to_json())

# convert the object into a dict
payment_info_create_dict = payment_info_create_instance.to_dict()
# create an instance of PaymentInfoCreate from a dict
payment_info_create_from_dict = PaymentInfoCreate.from_dict(payment_info_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


