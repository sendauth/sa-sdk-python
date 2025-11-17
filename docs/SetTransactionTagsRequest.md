# SetTransactionTagsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tags** | **Dict[str, str]** | Map of tag names to values | [optional] 

## Example

```python
from api.models.set_transaction_tags_request import SetTransactionTagsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SetTransactionTagsRequest from a JSON string
set_transaction_tags_request_instance = SetTransactionTagsRequest.from_json(json)
# print the JSON string representation of the object
print(SetTransactionTagsRequest.to_json())

# convert the object into a dict
set_transaction_tags_request_dict = set_transaction_tags_request_instance.to_dict()
# create an instance of SetTransactionTagsRequest from a dict
set_transaction_tags_request_from_dict = SetTransactionTagsRequest.from_dict(set_transaction_tags_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


