# Approval


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Approval ID | [optional] 
**state** | **str** | Approval state | [optional] 
**completed_at** | **datetime** | Approval completion timestamp | [optional] 
**requestor** | **str** | Approval requestor | [optional] 
**context** | **str** | Approval context | [optional] 
**created_at** | **datetime** | Approval creation timestamp | [optional] 
**message** | **str** | Approval message | [optional] 
**tags** | **Dict[str, str]** |  | [optional] 
**on_behalf_of** | **str** | If requesting authorization on a user&#39;s behalf, provide the email to let the approvers know. | [optional] 
**payload** | **Dict[str, object]** | Arbitrary JSON data that gets passed to webhooks | [optional] 
**transactions** | [**List[Transaction]**](Transaction.md) |  | [optional] 

## Example

```python
from api.models.approval import Approval

# TODO update the JSON string below
json = "{}"
# create an instance of Approval from a JSON string
approval_instance = Approval.from_json(json)
# print the JSON string representation of the object
print(Approval.to_json())

# convert the object into a dict
approval_dict = approval_instance.to_dict()
# create an instance of Approval from a dict
approval_from_dict = Approval.from_dict(approval_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


