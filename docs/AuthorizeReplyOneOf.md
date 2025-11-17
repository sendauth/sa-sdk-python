# AuthorizeReplyOneOf

Transaction response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tx_id** | **str** | Transaction ID for the transaction that&#39;s been sent to a user | [optional] 

## Example

```python
from api.models.authorize_reply_one_of import AuthorizeReplyOneOf

# TODO update the JSON string below
json = "{}"
# create an instance of AuthorizeReplyOneOf from a JSON string
authorize_reply_one_of_instance = AuthorizeReplyOneOf.from_json(json)
# print the JSON string representation of the object
print(AuthorizeReplyOneOf.to_json())

# convert the object into a dict
authorize_reply_one_of_dict = authorize_reply_one_of_instance.to_dict()
# create an instance of AuthorizeReplyOneOf from a dict
authorize_reply_one_of_from_dict = AuthorizeReplyOneOf.from_dict(authorize_reply_one_of_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


