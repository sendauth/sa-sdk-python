# AuthorizeReplyOneOf1

Approval response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**approval_id** | **str** | Approval ID for the approval that&#39;s been sent to an approval group | [optional] 

## Example

```python
from api.models.authorize_reply_one_of1 import AuthorizeReplyOneOf1

# TODO update the JSON string below
json = "{}"
# create an instance of AuthorizeReplyOneOf1 from a JSON string
authorize_reply_one_of1_instance = AuthorizeReplyOneOf1.from_json(json)
# print the JSON string representation of the object
print(AuthorizeReplyOneOf1.to_json())

# convert the object into a dict
authorize_reply_one_of1_dict = authorize_reply_one_of1_instance.to_dict()
# create an instance of AuthorizeReplyOneOf1 from a dict
authorize_reply_one_of1_from_dict = AuthorizeReplyOneOf1.from_dict(authorize_reply_one_of1_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


