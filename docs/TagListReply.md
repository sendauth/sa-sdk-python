# TagListReply


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tags** | [**List[Tag]**](Tag.md) |  | [optional] 

## Example

```python
from api.models.tag_list_reply import TagListReply

# TODO update the JSON string below
json = "{}"
# create an instance of TagListReply from a JSON string
tag_list_reply_instance = TagListReply.from_json(json)
# print the JSON string representation of the object
print(TagListReply.to_json())

# convert the object into a dict
tag_list_reply_dict = tag_list_reply_instance.to_dict()
# create an instance of TagListReply from a dict
tag_list_reply_from_dict = TagListReply.from_dict(tag_list_reply_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


