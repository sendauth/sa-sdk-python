# api.ApprovalsApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authorize**](ApprovalsApi.md#authorize) | **POST** /api/v1/authorize | Authorize a request
[**get_approval**](ApprovalsApi.md#get_approval) | **GET** /api/v1/approvals/{id} | Get an approval request


# **authorize**
> AuthorizeReply authorize(authorize_request)

Authorize a request

Authorize a request by tag. The provided tag will be used to find the matching routing rule  and initiate an authentication for that target.


### Example

* Basic Authentication (basic):

```python
import api
from api.models.authorize_reply import AuthorizeReply
from api.models.authorize_request import AuthorizeRequest
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
    api_instance = api.ApprovalsApi(api_client)
    authorize_request = api.AuthorizeRequest() # AuthorizeRequest | 

    try:
        # Authorize a request
        api_response = api_instance.authorize(authorize_request)
        print("The response of ApprovalsApi->authorize:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApprovalsApi->authorize: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **authorize_request** | [**AuthorizeRequest**](AuthorizeRequest.md)|  | 

### Return type

[**AuthorizeReply**](AuthorizeReply.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Authorization request created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_approval**
> Approval get_approval(id)

Get an approval request

Get detailed information about an approval request

### Example

* Basic Authentication (basic):

```python
import api
from api.models.approval import Approval
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
    api_instance = api.ApprovalsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Get an approval request
        api_response = api_instance.get_approval(id)
        print("The response of ApprovalsApi->get_approval:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApprovalsApi->get_approval: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**Approval**](Approval.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Approval |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

