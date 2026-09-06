# Barcode

Barcode. Used both as the request shape (ReceiptCreate.barcode) and the response shape (see MerchantReceiptResponse/CustomerReceiptDetailResponse/ ReceiptImmediateResponse.barcode). `code` is required: a Barcode object with no code is meaningless.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** |  | 
**format** | **str** |  | [optional] 

## Example

```python
from reccito_sdk.models.barcode import Barcode

# TODO update the JSON string below
json = "{}"
# create an instance of Barcode from a JSON string
barcode_instance = Barcode.from_json(json)
# print the JSON string representation of the object
print(Barcode.to_json())

# convert the object into a dict
barcode_dict = barcode_instance.to_dict()
# create an instance of Barcode from a dict
barcode_from_dict = Barcode.from_dict(barcode_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


