# MerchantDetails

Merchant details parsed from receipt.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**address** | **str** |  | [optional] 
**tax_id** | **str** |  | [optional] 
**contact_phone** | **str** |  | [optional] 
**contact_email** | **str** |  | [optional] 
**website** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.merchant_details import MerchantDetails

# TODO update the JSON string below
json = "{}"
# create an instance of MerchantDetails from a JSON string
merchant_details_instance = MerchantDetails.from_json(json)
# print the JSON string representation of the object
print(MerchantDetails.to_json())

# convert the object into a dict
merchant_details_dict = merchant_details_instance.to_dict()
# create an instance of MerchantDetails from a dict
merchant_details_from_dict = MerchantDetails.from_dict(merchant_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


