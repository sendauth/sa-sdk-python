# AuthGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The unique identifier of the approval group | [optional] 
**name** | **str** | The name of the approval group | 
**threshold** | **str** | The threshold for the approval group | 
**description** | **str** |  | [optional] 
**users** | [**List[AuthGroupMember]**](AuthGroupMember.md) |  | [optional] 

## Example

```python
from api.models.auth_group import AuthGroup

# TODO update the JSON string below
json = "{}"
# create an instance of AuthGroup from a JSON string
auth_group_instance = AuthGroup.from_json(json)
# print the JSON string representation of the object
print(AuthGroup.to_json())

# convert the object into a dict
auth_group_dict = auth_group_instance.to_dict()
# create an instance of AuthGroup from a dict
auth_group_from_dict = AuthGroup.from_dict(auth_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


