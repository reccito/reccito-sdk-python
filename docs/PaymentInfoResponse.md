# PaymentInfoResponse

Payment information response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | **str** |  | 
**amount** | **str** |  | 
**card_last_four** | **str** |  | [optional] 
**reference** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.payment_info_response import PaymentInfoResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PaymentInfoResponse from a JSON string
payment_info_response_instance = PaymentInfoResponse.from_json(json)
# print the JSON string representation of the object
print(PaymentInfoResponse.to_json())

# convert the object into a dict
payment_info_response_dict = payment_info_response_instance.to_dict()
# create an instance of PaymentInfoResponse from a dict
payment_info_response_from_dict = PaymentInfoResponse.from_dict(payment_info_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


