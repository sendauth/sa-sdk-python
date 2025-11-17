# AuthGroupMember


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The unique identifier of the user | [optional] 
**email** | **str** | The email address of the user | [optional] 
**first_name** | **str** | The first name of the user | [optional] 
**last_name** | **str** | The last name of the user | [optional] 

## Example

```python
from api.models.auth_group_member import AuthGroupMember

# TODO update the JSON string below
json = "{}"
# create an instance of AuthGroupMember from a JSON string
auth_group_member_instance = AuthGroupMember.from_json(json)
# print the JSON string representation of the object
print(AuthGroupMember.to_json())

# convert the object into a dict
auth_group_member_dict = auth_group_member_instance.to_dict()
# create an instance of AuthGroupMember from a dict
auth_group_member_from_dict = AuthGroupMember.from_dict(auth_group_member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


