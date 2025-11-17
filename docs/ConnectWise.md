# ConnectWise


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether ConnectWise integration is enabled | [optional] 
**server_url** | **str** | ConnectWise server URL | [optional] 
**company_id** | **str** | ConnectWise company ID | [optional] 
**public_key** | **str** | ConnectWise public key | [optional] 
**private_key** | **str** | ConnectWise private key | [optional] 
**api_version** | **str** | ConnectWise API version | [optional] 

## Example

```python
from api.models.connect_wise import ConnectWise

# TODO update the JSON string below
json = "{}"
# create an instance of ConnectWise from a JSON string
connect_wise_instance = ConnectWise.from_json(json)
# print the JSON string representation of the object
print(ConnectWise.to_json())

# convert the object into a dict
connect_wise_dict = connect_wise_instance.to_dict()
# create an instance of ConnectWise from a dict
connect_wise_from_dict = ConnectWise.from_dict(connect_wise_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


