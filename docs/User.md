# User


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Unique user identifier | [optional] [readonly] 
**role** | **str** | User role | [optional] 
**username** | **str** | Display username | [optional] [readonly] 
**first_name** | **str** | User first name | 
**last_name** | **str** | User last name | 
**email** | **str** | User email address | [optional] 
**phone** | **str** | User phone number | [optional] 
**company** | [**Company**](Company.md) |  | [optional] 
**permissions** | **List[str]** | User direct permissions | [optional] 
**group_permissions** | **List[str]** | Permissions from groups | [optional] 
**permission_groups** | **List[str]** | Permission group IDs | [optional] 
**messaging_preference** | **str** | User messaging preference | [optional] 
**has_passkeys** | **bool** | Whether user has passkeys configured | [optional] [readonly] 
**created_at** | **datetime** | User creation timestamp | [optional] [readonly] 
**last_authenticated** | **datetime** | Last authentication timestamp | [optional] [readonly] 

## Example

```python
from api.models.user import User

# TODO update the JSON string below
json = "{}"
# create an instance of User from a JSON string
user_instance = User.from_json(json)
# print the JSON string representation of the object
print(User.to_json())

# convert the object into a dict
user_dict = user_instance.to_dict()
# create an instance of User from a dict
user_from_dict = User.from_dict(user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


