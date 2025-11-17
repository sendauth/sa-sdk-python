# SetPermissionGroupPermissionsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**permissions** | **List[str]** |  | [optional] 

## Example

```python
from api.models.set_permission_group_permissions_request import SetPermissionGroupPermissionsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SetPermissionGroupPermissionsRequest from a JSON string
set_permission_group_permissions_request_instance = SetPermissionGroupPermissionsRequest.from_json(json)
# print the JSON string representation of the object
print(SetPermissionGroupPermissionsRequest.to_json())

# convert the object into a dict
set_permission_group_permissions_request_dict = set_permission_group_permissions_request_instance.to_dict()
# create an instance of SetPermissionGroupPermissionsRequest from a dict
set_permission_group_permissions_request_from_dict = SetPermissionGroupPermissionsRequest.from_dict(set_permission_group_permissions_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


