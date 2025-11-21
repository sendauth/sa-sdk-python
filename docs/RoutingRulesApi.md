# api.RoutingRulesApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_routing_rule**](RoutingRulesApi.md#create_routing_rule) | **POST** /api/v1/tag-routing-rules | Create routing rule
[**delete_routing_rule**](RoutingRulesApi.md#delete_routing_rule) | **DELETE** /api/v1/tag-routing-rules/{id} | Delete routing rule
[**get_routing_rule**](RoutingRulesApi.md#get_routing_rule) | **GET** /api/v1/tag-routing-rules/{id} | Get routing rules
[**list_routing_rules**](RoutingRulesApi.md#list_routing_rules) | **GET** /api/v1/tag-routing-rules | Get routing rules
[**update_routing_rule**](RoutingRulesApi.md#update_routing_rule) | **PUT** /api/v1/tag-routing-rules/{id} | Update routing rule


# **create_routing_rule**
> IDReply create_routing_rule(routing_rule)

Create routing rule

Create a new routing rule

### Example

* Basic Authentication (basic):

```python
import api
from api.models.id_reply import IDReply
from api.models.routing_rule import RoutingRule
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
    api_instance = api.RoutingRulesApi(api_client)
    routing_rule = api.RoutingRule() # RoutingRule | 

    try:
        # Create routing rule
        api_response = api_instance.create_routing_rule(routing_rule)
        print("The response of RoutingRulesApi->create_routing_rule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutingRulesApi->create_routing_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **routing_rule** | [**RoutingRule**](RoutingRule.md)|  | 

### Return type

[**IDReply**](IDReply.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Routing rule created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_routing_rule**
> delete_routing_rule(id)

Delete routing rule

Delete a routing rule by ID

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
    api_instance = api.RoutingRulesApi(api_client)
    id = 'id_example' # str | Routing rule ID

    try:
        # Delete routing rule
        api_instance.delete_routing_rule(id)
    except Exception as e:
        print("Exception when calling RoutingRulesApi->delete_routing_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Routing rule ID | 

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
**204** | Routing rule deleted |  -  |
**404** | Routing rule not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_routing_rule**
> RoutingRule get_routing_rule(id)

Get routing rules

Get all routing rules

### Example

* Basic Authentication (basic):

```python
import api
from api.models.routing_rule import RoutingRule
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
    api_instance = api.RoutingRulesApi(api_client)
    id = 'id_example' # str | Routing rule ID

    try:
        # Get routing rules
        api_response = api_instance.get_routing_rule(id)
        print("The response of RoutingRulesApi->get_routing_rule:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutingRulesApi->get_routing_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Routing rule ID | 

### Return type

[**RoutingRule**](RoutingRule.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Routing rule |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_routing_rules**
> List[RoutingRule] list_routing_rules()

Get routing rules

Get all routing rules

### Example

* Basic Authentication (basic):

```python
import api
from api.models.routing_rule import RoutingRule
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
    api_instance = api.RoutingRulesApi(api_client)

    try:
        # Get routing rules
        api_response = api_instance.list_routing_rules()
        print("The response of RoutingRulesApi->list_routing_rules:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutingRulesApi->list_routing_rules: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[RoutingRule]**](RoutingRule.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of routing rules |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_routing_rule**
> update_routing_rule(id, routing_rule)

Update routing rule

Update a routing rule by ID

### Example

* Basic Authentication (basic):

```python
import api
from api.models.routing_rule import RoutingRule
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
    api_instance = api.RoutingRulesApi(api_client)
    id = 'id_example' # str | Routing rule ID
    routing_rule = api.RoutingRule() # RoutingRule | 

    try:
        # Update routing rule
        api_instance.update_routing_rule(id, routing_rule)
    except Exception as e:
        print("Exception when calling RoutingRulesApi->update_routing_rule: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Routing rule ID | 
 **routing_rule** | [**RoutingRule**](RoutingRule.md)|  | 

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
**200** | Routing rule updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

