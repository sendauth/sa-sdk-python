# RoutingRule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**tag_name** | **str** | Name of tag associated with the routing rule | 
**tag_value** | **str** | Tag value that must match for this rule to fire | 
**description** | **str** |  | [optional] 
**target_type** | **str** | The type of target for the routing rule | 
**target_id** | **str** | The ID of the target (approval group or user) | 
**target_email** | **str** | The email of the target | [optional] 
**target_name** | **str** | The name of the target | [optional] 

## Example

```python
from api.models.routing_rule import RoutingRule

# TODO update the JSON string below
json = "{}"
# create an instance of RoutingRule from a JSON string
routing_rule_instance = RoutingRule.from_json(json)
# print the JSON string representation of the object
print(RoutingRule.to_json())

# convert the object into a dict
routing_rule_dict = routing_rule_instance.to_dict()
# create an instance of RoutingRule from a dict
routing_rule_from_dict = RoutingRule.from_dict(routing_rule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


