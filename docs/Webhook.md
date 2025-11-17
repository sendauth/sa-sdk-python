# Webhook

A webhook configuration object

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | The unique identifier of the webhook | 
**url** | **str** | The URL where webhook events will be sent | 
**secret** | **str** | Optional secret used to sign webhook payloads (HMAC-SHA256) | [optional] 
**auth_group_id** | **str** | Optional approval group ID to associate with the webhook | [optional] 
**events** | [**WebhookEvents**](WebhookEvents.md) |  | 
**created_at** | **datetime** | When the webhook was created | [optional] 

## Example

```python
from api.models.webhook import Webhook

# TODO update the JSON string below
json = "{}"
# create an instance of Webhook from a JSON string
webhook_instance = Webhook.from_json(json)
# print the JSON string representation of the object
print(Webhook.to_json())

# convert the object into a dict
webhook_dict = webhook_instance.to_dict()
# create an instance of Webhook from a dict
webhook_from_dict = Webhook.from_dict(webhook_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


