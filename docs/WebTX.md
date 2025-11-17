# WebTX


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** | Transaction message | [optional] 
**connectwise** | **str** | ConnectWise reference | [optional] 

## Example

```python
from api.models.web_tx import WebTX

# TODO update the JSON string below
json = "{}"
# create an instance of WebTX from a JSON string
web_tx_instance = WebTX.from_json(json)
# print the JSON string representation of the object
print(WebTX.to_json())

# convert the object into a dict
web_tx_dict = web_tx_instance.to_dict()
# create an instance of WebTX from a dict
web_tx_from_dict = WebTX.from_dict(web_tx_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


