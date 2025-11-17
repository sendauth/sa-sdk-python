# PaginatedAudits


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rows** | [**List[Audit]**](Audit.md) |  | [optional] 
**total** | **int** | Total number of items | [optional] 

## Example

```python
from api.models.paginated_audits import PaginatedAudits

# TODO update the JSON string below
json = "{}"
# create an instance of PaginatedAudits from a JSON string
paginated_audits_instance = PaginatedAudits.from_json(json)
# print the JSON string representation of the object
print(PaginatedAudits.to_json())

# convert the object into a dict
paginated_audits_dict = paginated_audits_instance.to_dict()
# create an instance of PaginatedAudits from a dict
paginated_audits_from_dict = PaginatedAudits.from_dict(paginated_audits_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


