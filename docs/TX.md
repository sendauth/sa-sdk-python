# TX


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tx** | **str** | Transaction ID | [optional] 

## Example

```python
from api.models.tx import TX

# TODO update the JSON string below
json = "{}"
# create an instance of TX from a JSON string
tx_instance = TX.from_json(json)
# print the JSON string representation of the object
print(TX.to_json())

# convert the object into a dict
tx_dict = tx_instance.to_dict()
# create an instance of TX from a dict
tx_from_dict = TX.from_dict(tx_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


