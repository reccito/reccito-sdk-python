# ReceiptSummary

Slim receipt shape for the paginated merchant list endpoint -- omits qr_code_url, items, payment_info, adjustments, warranties, and insights to keep list responses lightweight. Fetch GET /merchant/receipts/{id} for the full detail (QR code included) when a single receipt is opened.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**public_token** | **str** |  | 
**merchant_receipt_id** | **str** |  | [optional] 
**store_id** | **str** |  | 
**organisation_id** | **str** |  | 
**transaction_date** | **datetime** |  | 
**total_amount** | **str** |  | 
**currency** | **str** |  | 
**item_count** | **int** |  | 
**status** | **str** |  | 
**access_count** | **int** |  | 
**receipt_url** | **str** |  | 
**created_at** | **datetime** |  | 

## Example

```python
from reccito_sdk.models.receipt_summary import ReceiptSummary

# TODO update the JSON string below
json = "{}"
# create an instance of ReceiptSummary from a JSON string
receipt_summary_instance = ReceiptSummary.from_json(json)
# print the JSON string representation of the object
print(ReceiptSummary.to_json())

# convert the object into a dict
receipt_summary_dict = receipt_summary_instance.to_dict()
# create an instance of ReceiptSummary from a dict
receipt_summary_from_dict = ReceiptSummary.from_dict(receipt_summary_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


