# api.WebhooksApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_webhook**](WebhooksApi.md#create_webhook) | **POST** /api/v1/webhooks | Create a new webhook
[**delete_webhook**](WebhooksApi.md#delete_webhook) | **DELETE** /api/v1/webhooks/{id} | Delete a webhook
[**list_webhooks**](WebhooksApi.md#list_webhooks) | **GET** /api/v1/webhooks | List all webhooks
[**update_webhook**](WebhooksApi.md#update_webhook) | **PUT** /api/v1/webhooks/{id} | Update a webhook


# **create_webhook**
> Webhook create_webhook(webhook_input)

Create a new webhook

Create a new webhook configuration for the authenticated organization

### Example

* Basic Authentication (basic):

```python
import api
from api.models.webhook import Webhook
from api.models.webhook_input import WebhookInput
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://app.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://app.sendauth.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure HTTP basic authorization: basic
configuration = api.Configuration(
    username = os.environ["USERNAME"],
    password = os.environ["PASSWORD"]
)

# Enter a context with an instance of the API client
with api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = api.WebhooksApi(api_client)
    webhook_input = {"url":"https://example.com/webhook","secret":"my-webhook-secret","events":{"verify":true,"deny":false}} # WebhookInput | 

    try:
        # Create a new webhook
        api_response = api_instance.create_webhook(webhook_input)
        print("The response of WebhooksApi->create_webhook:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->create_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **webhook_input** | [**WebhookInput**](WebhookInput.md)|  | 

### Return type

[**Webhook**](Webhook.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Webhook created successfully |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**422** | Validation error |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_webhook**
> delete_webhook(id)

Delete a webhook

Delete an existing webhook configuration

### Example

* Basic Authentication (basic):

```python
import api
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://app.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://app.sendauth.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure HTTP basic authorization: basic
configuration = api.Configuration(
    username = os.environ["USERNAME"],
    password = os.environ["PASSWORD"]
)

# Enter a context with an instance of the API client
with api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = api.WebhooksApi(api_client)
    id = '01234567-89ab-cdef-0123-456789abcdef' # str | The unique identifier of the webhook

    try:
        # Delete a webhook
        api_instance.delete_webhook(id)
    except Exception as e:
        print("Exception when calling WebhooksApi->delete_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| The unique identifier of the webhook | 

### Return type

void (empty response body)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook deleted successfully |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_webhooks**
> List[Webhook] list_webhooks()

List all webhooks

Retrieve all webhooks configured for the authenticated organization

### Example

* Basic Authentication (basic):

```python
import api
from api.models.webhook import Webhook
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://app.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://app.sendauth.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure HTTP basic authorization: basic
configuration = api.Configuration(
    username = os.environ["USERNAME"],
    password = os.environ["PASSWORD"]
)

# Enter a context with an instance of the API client
with api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = api.WebhooksApi(api_client)

    try:
        # List all webhooks
        api_response = api_instance.list_webhooks()
        print("The response of WebhooksApi->list_webhooks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling WebhooksApi->list_webhooks: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[Webhook]**](Webhook.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Successful response |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_webhook**
> update_webhook(id, webhook_input)

Update a webhook

Update an existing webhook configuration

### Example

* Basic Authentication (basic):

```python
import api
from api.models.webhook_input import WebhookInput
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://app.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://app.sendauth.com"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure HTTP basic authorization: basic
configuration = api.Configuration(
    username = os.environ["USERNAME"],
    password = os.environ["PASSWORD"]
)

# Enter a context with an instance of the API client
with api.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = api.WebhooksApi(api_client)
    id = '01234567-89ab-cdef-0123-456789abcdef' # str | The unique identifier of the webhook
    webhook_input = {"url":"https://example.com/updated-webhook","secret":"updated-secret","events":{"verify":true,"deny":true}} # WebhookInput | 

    try:
        # Update a webhook
        api_instance.update_webhook(id, webhook_input)
    except Exception as e:
        print("Exception when calling WebhooksApi->update_webhook: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| The unique identifier of the webhook | 
 **webhook_input** | [**WebhookInput**](WebhookInput.md)|  | 

### Return type

void (empty response body)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Webhook updated successfully |  -  |
**400** | Bad request |  -  |
**401** | Unauthorized |  -  |
**403** | Forbidden |  -  |
**404** | Not found |  -  |
**422** | Validation error |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

