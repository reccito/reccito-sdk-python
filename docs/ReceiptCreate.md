# ReceiptCreate

Receipt creation request.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**merchant_receipt_id** | **str** |  | [optional] 
**dedupe_key** | **str** |  | [optional] 
**barcode** | [**Barcode**](Barcode.md) |  | [optional] 
**store_id** | **str** |  | [optional] 
**transaction_date** | **datetime** |  | 
**order_number** | **str** |  | [optional] 
**cashier** | **str** |  | [optional] 
**items** | [**List[ReceiptItemCreate]**](ReceiptItemCreate.md) |  | 
**subtotal** | **str** |  | 
**tax_amount** | **str** |  | 
**discount_amount** | **str** |  | [optional] [default to '0']
**tip_amount** | **str** |  | [optional] [default to '0']
**total_amount** | **str** |  | 
**currency** | **str** |  | 
**payment_info** | [**List[PaymentInfoCreate]**](PaymentInfoCreate.md) |  | 
**notes** | **str** |  | [optional] 
**return_policy** | **str** |  | [optional] 
**offers** | **List[str]** |  | [optional] 
**offer_policies** | [**List[OfferPolicyInfo]**](OfferPolicyInfo.md) |  | [optional] 
**feedback_url** | **str** |  | [optional] 
**loyalty_info** | **str** |  | [optional] 
**merchant_details** | [**MerchantDetails**](MerchantDetails.md) |  | [optional] 
**adjustments** | [**List[ReceiptAdjustment]**](ReceiptAdjustment.md) |  | [optional] 
**transaction_references** | [**List[TransactionReference]**](TransactionReference.md) |  | [optional] 
**warranties** | [**List[WarrantyInfo]**](WarrantyInfo.md) |  | [optional] 
**insights** | [**ReceiptInsights**](ReceiptInsights.md) |  | [optional] 
**return_insights** | [**ReturnInsights**](ReturnInsights.md) |  | [optional] 
**qr_expiry_minutes** | **int** |  | [optional] 

## Example

```python
from reccito_sdk.models.receipt_create import ReceiptCreate

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptCreate from a JSON string
receipt_create_instance = ReceiptCreate.from_json(json)
# print the JSON string representation of the object
print(ReceiptCreate.to_json())

# convert the object into a dict
receipt_create_dict = receipt_create_instance.to_dict()
# create an instance of ReceiptCreate from a dict
receipt_create_from_dict = ReceiptCreate.from_dict(receipt_create_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


