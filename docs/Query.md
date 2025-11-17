# Query


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | **int** | Page number | [optional] 
**per_page** | **int** | Items per page | [optional] 
**q** | **str** | Search query | [optional] 
**permission** | **str** | Filter by permission | [optional] 
**sort_by** | **str** | Sort field | [optional] 
**sort_dir** | **str** | Sort direction | [optional] 

## Example

```python
from api.models.query import Query

# TODO update the JSON string below
json = "{}"
# create an instance of Query from a JSON string
query_instance = Query.from_json(json)
# print the JSON string representation of the object
print(Query.to_json())

# convert the object into a dict
query_dict = query_instance.to_dict()
# create an instance of Query from a dict
query_from_dict = Query.from_dict(query_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


