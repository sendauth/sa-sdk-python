# api.ApprovalGroupsApi

All URIs are relative to *https://api.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_user_to_auth_group**](ApprovalGroupsApi.md#add_user_to_auth_group) | **POST** /api/v1/approval-groups/{id}/users/{userID} | Add user to approval group
[**create_auth_group**](ApprovalGroupsApi.md#create_auth_group) | **POST** /api/v1/approval-groups | Create approval group
[**delete_auth_group**](ApprovalGroupsApi.md#delete_auth_group) | **DELETE** /api/v1/approval-groups/{id} | Delete approval group
[**get_auth_group**](ApprovalGroupsApi.md#get_auth_group) | **GET** /api/v1/approval-groups/{id} | Get approval group
[**list_auth_groups**](ApprovalGroupsApi.md#list_auth_groups) | **GET** /api/v1/approval-groups | List approval groups
[**remove_user_from_auth_group**](ApprovalGroupsApi.md#remove_user_from_auth_group) | **DELETE** /api/v1/approval-groups/{id}/users/{userID} | Remove user from approval group
[**set_auth_group_tags**](ApprovalGroupsApi.md#set_auth_group_tags) | **PUT** /api/v1/approval-groups/{id}/tags | Set approval group tags
[**update_auth_group**](ApprovalGroupsApi.md#update_auth_group) | **PUT** /api/v1/approval-groups/{id} | Update approval group


# **add_user_to_auth_group**
> add_user_to_auth_group(id, user_id)

Add user to approval group

Add a user to an approval group by ID

### Example

* Basic Authentication (basic):

```python
import api
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)
    id = 'id_example' # str | Approval group ID
    user_id = 'user_id_example' # str | User ID

    try:
        # Add user to approval group
        api_instance.add_user_to_auth_group(id, user_id)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->add_user_to_auth_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Approval group ID | 
 **user_id** | **str**| User ID | 

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
**200** | User added to approval group |  -  |
**404** | Approval group or user not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_auth_group**
> AuthGroup create_auth_group(auth_group)

Create approval group

Create a new approval group

### Example

* Basic Authentication (basic):

```python
import api
from api.models.auth_group import AuthGroup
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)
    auth_group = api.AuthGroup() # AuthGroup | 

    try:
        # Create approval group
        api_response = api_instance.create_auth_group(auth_group)
        print("The response of ApprovalGroupsApi->create_auth_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->create_auth_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **auth_group** | [**AuthGroup**](AuthGroup.md)|  | 

### Return type

[**AuthGroup**](AuthGroup.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Approval group created |  -  |
**422** | Validation error |  -  |
**409** | Approval group already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_auth_group**
> delete_auth_group(id)

Delete approval group

Delete an approval group by ID

### Example

* Basic Authentication (basic):

```python
import api
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)
    id = 'id_example' # str | Approval group ID

    try:
        # Delete approval group
        api_instance.delete_auth_group(id)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->delete_auth_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Approval group ID | 

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
**200** | Approval group deleted |  -  |
**404** | Approval group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_auth_group**
> AuthGroup get_auth_group(id)

Get approval group

Get an approval group by ID

### Example

* Basic Authentication (basic):

```python
import api
from api.models.auth_group import AuthGroup
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)
    id = 'id_example' # str | Approval group ID

    try:
        # Get approval group
        api_response = api_instance.get_auth_group(id)
        print("The response of ApprovalGroupsApi->get_auth_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->get_auth_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Approval group ID | 

### Return type

[**AuthGroup**](AuthGroup.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Approval group |  -  |
**404** | Approval group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_auth_groups**
> List[AuthGroup] list_auth_groups()

List approval groups

Get list of all approval groups

### Example

* Basic Authentication (basic):

```python
import api
from api.models.auth_group import AuthGroup
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)

    try:
        # List approval groups
        api_response = api_instance.list_auth_groups()
        print("The response of ApprovalGroupsApi->list_auth_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->list_auth_groups: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[AuthGroup]**](AuthGroup.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of approval groups |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_user_from_auth_group**
> remove_user_from_auth_group(id, user_id)

Remove user from approval group

Remove a user from an approval group by ID

### Example

* Basic Authentication (basic):

```python
import api
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)
    id = 'id_example' # str | 
    user_id = 'user_id_example' # str | User ID

    try:
        # Remove user from approval group
        api_instance.remove_user_from_auth_group(id, user_id)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->remove_user_from_auth_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **user_id** | **str**| User ID | 

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
**200** | User removed from approval group |  -  |
**404** | Approval group or user not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_auth_group_tags**
> set_auth_group_tags(id, set_transaction_tags_request=set_transaction_tags_request)

Set approval group tags

Set tags for a specific approval group

### Example

* Basic Authentication (basic):

```python
import api
from api.models.set_transaction_tags_request import SetTransactionTagsRequest
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)
    id = 'id_example' # str | 
    set_transaction_tags_request = api.SetTransactionTagsRequest() # SetTransactionTagsRequest |  (optional)

    try:
        # Set approval group tags
        api_instance.set_auth_group_tags(id, set_transaction_tags_request=set_transaction_tags_request)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->set_auth_group_tags: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **set_transaction_tags_request** | [**SetTransactionTagsRequest**](SetTransactionTagsRequest.md)|  | [optional] 

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
**200** | Tags updated |  -  |
**404** | Approval group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_auth_group**
> update_auth_group(id, auth_group)

Update approval group

Update an approval group

### Example

* Basic Authentication (basic):

```python
import api
from api.models.auth_group import AuthGroup
from api.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.sendauth.com
# See configuration.py for a list of all supported configuration parameters.
configuration = api.Configuration(
    host = "https://api.sendauth.com"
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
    api_instance = api.ApprovalGroupsApi(api_client)
    id = 'id_example' # str | Approval group ID
    auth_group = api.AuthGroup() # AuthGroup | 

    try:
        # Update approval group
        api_instance.update_auth_group(id, auth_group)
    except Exception as e:
        print("Exception when calling ApprovalGroupsApi->update_auth_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Approval group ID | 
 **auth_group** | [**AuthGroup**](AuthGroup.md)|  | 

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
**200** | Approval group updated |  -  |
**422** | Validation error |  -  |
**409** | Approval group already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

