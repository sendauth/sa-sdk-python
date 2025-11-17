# WebhookEvents


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**verify** | **bool** | When true, transaction verifications will invoke the webhook | [optional] 
**deny** | **bool** | When true, transaction denials will invoke the webhook | [optional] 

## Example

```python
from api.models.webhook_events import WebhookEvents

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookEvents from a JSON string
webhook_events_instance = WebhookEvents.from_json(json)
# print the JSON string representation of the object
print(WebhookEvents.to_json())

# convert the object into a dict
webhook_events_dict = webhook_events_instance.to_dict()
# create an instance of WebhookEvents from a dict
webhook_events_from_dict = WebhookEvents.from_dict(webhook_events_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


