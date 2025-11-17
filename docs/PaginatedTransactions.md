# PaginatedTransactions


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rows** | [**List[Transaction]**](Transaction.md) |  | [optional] 
**total** | **int** | Total number of items | [optional] 

## Example

```python
from api.models.paginated_transactions import PaginatedTransactions

# TODO update the JSON string below
json = "{}"
# create an instance of PaginatedTransactions from a JSON string
paginated_transactions_instance = PaginatedTransactions.from_json(json)
# print the JSON string representation of the object
print(PaginatedTransactions.to_json())

# convert the object into a dict
paginated_transactions_dict = paginated_transactions_instance.to_dict()
# create an instance of PaginatedTransactions from a dict
paginated_transactions_from_dict = PaginatedTransactions.from_dict(paginated_transactions_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


