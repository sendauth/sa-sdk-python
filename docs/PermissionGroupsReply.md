# PermissionGroupsReply


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**groups** | [**List[PermissionGroup]**](PermissionGroup.md) |  | [optional] 

## Example

```python
from api.models.permission_groups_reply import PermissionGroupsReply

# TODO update the JSON string below
json = "{}"
# create an instance of PermissionGroupsReply from a JSON string
permission_groups_reply_instance = PermissionGroupsReply.from_json(json)
# print the JSON string representation of the object
print(PermissionGroupsReply.to_json())

# convert the object into a dict
permission_groups_reply_dict = permission_groups_reply_instance.to_dict()
# create an instance of PermissionGroupsReply from a dict
permission_groups_reply_from_dict = PermissionGroupsReply.from_dict(permission_groups_reply_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


