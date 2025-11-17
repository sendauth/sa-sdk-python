# WebhookInput

Input schema for creating or updating a webhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | **str** |  | 
**secret** | **str** | Optional secret used to sign webhook payloads (HMAC-SHA256). If a secret is already set, omitting this will preserve the existing secret. | [optional] 
**auth_group_id** | **str** | Optional approval group ID to associate with the webhook | [optional] 
**events** | [**WebhookEvents**](WebhookEvents.md) |  | 

## Example

```python
from api.models.webhook_input import WebhookInput

# TODO update the JSON string below
json = "{}"
# create an instance of WebhookInput from a JSON string
webhook_input_instance = WebhookInput.from_json(json)
# print the JSON string representation of the object
print(WebhookInput.to_json())

# convert the object into a dict
webhook_input_dict = webhook_input_instance.to_dict()
# create an instance of WebhookInput from a dict
webhook_input_from_dict = WebhookInput.from_dict(webhook_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


