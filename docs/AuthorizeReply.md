# AuthorizeReply


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tx_id** | **str** | Transaction ID for the transaction that&#39;s been sent to a user | [optional] 
**approval_id** | **str** | Approval ID for the approval that&#39;s been sent to an approval group | [optional] 

## Example

```python
from api.models.authorize_reply import AuthorizeReply

# TODO update the JSON string below
json = "{}"
# create an instance of AuthorizeReply from a JSON string
authorize_reply_instance = AuthorizeReply.from_json(json)
# print the JSON string representation of the object
print(AuthorizeReply.to_json())

# convert the object into a dict
authorize_reply_dict = authorize_reply_instance.to_dict()
# create an instance of AuthorizeReply from a dict
authorize_reply_from_dict = AuthorizeReply.from_dict(authorize_reply_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


