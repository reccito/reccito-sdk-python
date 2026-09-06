# QRRefreshResponse

QR code refresh response.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**receipt_id** | **str** |  | 
**new_qr_token** | **str** |  | 
**new_qr_code_url** | **str** |  | 
**expires_at** | **datetime** |  | 

## Example

```python
from reccito_sdk.models.qr_refresh_response import QRRefreshResponse

# TODO update the JSON string below
json = "{}"
# create an instance of QRRefreshResponse from a JSON string
qr_refresh_response_instance = QRRefreshResponse.from_json(json)
# print the JSON string representation of the object
print(QRRefreshResponse.to_json())

# convert the object into a dict
qr_refresh_response_dict = qr_refresh_response_instance.to_dict()
# create an instance of QRRefreshResponse from a dict
qr_refresh_response_from_dict = QRRefreshResponse.from_dict(qr_refresh_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


