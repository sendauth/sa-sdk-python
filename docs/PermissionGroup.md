# PermissionGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Permission group identifier | [optional] 
**name** | **str** | Permission group name | 
**permissions** | **List[str]** | Permissions in this group | [optional] 

## Example

```python
from api.models.permission_group import PermissionGroup

# TODO update the JSON string below
json = "{}"
# create an instance of PermissionGroup from a JSON string
permission_group_instance = PermissionGroup.from_json(json)
# print the JSON string representation of the object
print(PermissionGroup.to_json())

# convert the object into a dict
permission_group_dict = permission_group_instance.to_dict()
# create an instance of PermissionGroup from a dict
permission_group_from_dict = PermissionGroup.from_dict(permission_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


