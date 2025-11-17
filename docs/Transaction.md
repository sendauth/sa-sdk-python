# Transaction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Transaction identifier | [optional] 
**subject** | **str** | Subject user ID | [optional] 
**subject_name** | **str** | Subject user name | [optional] 
**state** | **str** | Transaction state | [optional] 
**completed_at** | **datetime** | Transaction completion timestamp | [optional] 
**requestor** | **str** | Transaction requestor | [optional] 
**context** | **str** | Transaction context | [optional] 
**created_at** | **datetime** | Transaction creation timestamp | [optional] 
**expires_at** | **datetime** | Transaction expiration timestamp | [optional] 
**message** | **str** | Transaction message | [optional] 
**user_message** | **str** | User-provided message | [optional] 

## Example

```python
from api.models.transaction import Transaction

# TODO update the JSON string below
json = "{}"
# create an instance of Transaction from a JSON string
transaction_instance = Transaction.from_json(json)
# print the JSON string representation of the object
print(Transaction.to_json())

# convert the object into a dict
transaction_dict = transaction_instance.to_dict()
# create an instance of Transaction from a dict
transaction_from_dict = Transaction.from_dict(transaction_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


