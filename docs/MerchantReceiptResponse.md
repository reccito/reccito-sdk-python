# MerchantReceiptResponse

Receipt response for the merchant audience (dashboard, merchant API keys).  Excludes customer-upload-pipeline fields (uploaded_file_url, file_size, file_type, original_filename, extraction_status/confidence/method/ completed_at, receipt_source, uploaded_by_customer_id), which are always null for merchant-issued receipts and belong to the separate customer-audience response shape instead.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**public_token** | **str** |  | 
**barcode** | [**Barcode**](Barcode.md) |  | [optional] 
**merchant_receipt_id** | **str** |  | [optional] 
**merchant_name** | **str** |  | [optional] 
**merchant_logo** | **str** |  | [optional] 
**store_id** | **str** |  | 
**organisation_id** | **str** |  | 
**transaction_date** | **datetime** |  | 
**order_number** | **str** |  | [optional] 
**cashier** | **str** |  | [optional] 
**items** | [**List[ReceiptItemResponse]**](ReceiptItemResponse.md) |  | 
**subtotal** | **str** |  | 
**tax_amount** | **str** |  | 
**discount_amount** | **str** |  | 
**tip_amount** | **str** |  | 
**total_amount** | **str** |  | 
**currency** | **str** |  | 
**payment_info** | [**List[PaymentInfoResponse]**](PaymentInfoResponse.md) |  | 
**qr_code_url** | **str** |  | 
**qr_token** | **str** |  | 
**qr_expires_at** | **datetime** |  | 
**receipt_url** | **str** |  | 
**pdf_url** | **str** |  | [optional] 
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
**access_count** | **int** |  | 
**last_accessed** | **datetime** |  | [optional] 
**status** | **str** |  | 
**expires_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from reccito_sdk.models.merchant_receipt_response import MerchantReceiptResponse

# TODO update the JSON string below
json = "{}"
# create an instance of MerchantReceiptResponse from a JSON string
merchant_receipt_response_instance = MerchantReceiptResponse.from_json(json)
# print the JSON string representation of the object
print(MerchantReceiptResponse.to_json())

# convert the object into a dict
merchant_receipt_response_dict = merchant_receipt_response_instance.to_dict()
# create an instance of MerchantReceiptResponse from a dict
merchant_receipt_response_from_dict = MerchantReceiptResponse.from_dict(merchant_receipt_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


