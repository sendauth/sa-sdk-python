# OpenID


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**issuer** | **str** | OpenID Connect issuer URL | [optional] 
**client_id** | **str** | OpenID Connect client ID | [optional] 
**client_secret** | **str** | OpenID Connect client secret | [optional] 

## Example

```python
from api.models.open_id import OpenID

# TODO update the JSON string below
json = "{}"
# create an instance of OpenID from a JSON string
open_id_instance = OpenID.from_json(json)
# print the JSON string representation of the object
print(OpenID.to_json())

# convert the object into a dict
open_id_dict = open_id_instance.to_dict()
# create an instance of OpenID from a dict
open_id_from_dict = OpenID.from_dict(open_id_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


