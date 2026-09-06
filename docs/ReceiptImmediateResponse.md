# ReceiptImmediateResponse

Immediate receipt response for fast QR code generation.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**public_token** | **str** |  | 
**barcode** | [**Barcode**](Barcode.md) |  | [optional] 
**merchant_receipt_id** | **str** |  | [optional] 
**store_id** | **str** |  | 
**organisation_id** | **str** |  | 
**qr_code_url** | **str** |  | 
**qr_token** | **str** |  | 
**qr_expires_at** | **datetime** |  | 
**receipt_url** | **str** |  | 
**transaction_date** | **datetime** |  | 
**total_amount** | **str** |  | 
**currency** | **str** |  | 
**processing_status** | **str** |  | [optional] [default to 'processing']
**created_at** | **datetime** |  | 

## Example

```python
from reccito_sdk.models.receipt_immediate_response import ReceiptImmediateResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptImmediateResponse from a JSON string
receipt_immediate_response_instance = ReceiptImmediateResponse.from_json(json)
# print the JSON string representation of the object
print(ReceiptImmediateResponse.to_json())

# convert the object into a dict
receipt_immediate_response_dict = receipt_immediate_response_instance.to_dict()
# create an instance of ReceiptImmediateResponse from a dict
receipt_immediate_response_from_dict = ReceiptImmediateResponse.from_dict(receipt_immediate_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


