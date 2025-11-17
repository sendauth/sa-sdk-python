# UpdateTagValueRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** | New value for the tag | [optional] 

## Example

```python
from api.models.update_tag_value_request import UpdateTagValueRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateTagValueRequest from a JSON string
update_tag_value_request_instance = UpdateTagValueRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateTagValueRequest.to_json())

# convert the object into a dict
update_tag_value_request_dict = update_tag_value_request_instance.to_dict()
# create an instance of UpdateTagValueRequest from a dict
update_tag_value_request_from_dict = UpdateTagValueRequest.from_dict(update_tag_value_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


