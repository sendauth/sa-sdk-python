# AuthorizeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | 
**tag** | **Dict[str, str]** |  | 
**context** | **str** |  | [optional] 
**payload** | **Dict[str, object]** | Arbitrary JSON data that gets passed to webhooks | [optional] 

## Example

```python
from api.models.authorize_request import AuthorizeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AuthorizeRequest from a JSON string
authorize_request_instance = AuthorizeRequest.from_json(json)
# print the JSON string representation of the object
print(AuthorizeRequest.to_json())

# convert the object into a dict
authorize_request_dict = authorize_request_instance.to_dict()
# create an instance of AuthorizeRequest from a dict
authorize_request_from_dict = AuthorizeRequest.from_dict(authorize_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


