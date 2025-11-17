# PermissionsReply


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**permissions** | [**List[Permission]**](Permission.md) |  | [optional] 

## Example

```python
from api.models.permissions_reply import PermissionsReply

# TODO update the JSON string below
json = "{}"
# create an instance of PermissionsReply from a JSON string
permissions_reply_instance = PermissionsReply.from_json(json)
# print the JSON string representation of the object
print(PermissionsReply.to_json())

# convert the object into a dict
permissions_reply_dict = permissions_reply_instance.to_dict()
# create an instance of PermissionsReply from a dict
permissions_reply_from_dict = PermissionsReply.from_dict(permissions_reply_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


