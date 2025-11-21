# api.PermissionGroupsApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_permission_group**](PermissionGroupsApi.md#create_permission_group) | **POST** /api/v1/permission-groups | Create permission group
[**delete_permission_group**](PermissionGroupsApi.md#delete_permission_group) | **DELETE** /api/v1/permission-groups/{id} | Delete permission group
[**list_permission_groups**](PermissionGroupsApi.md#list_permission_groups) | **GET** /api/v1/permission-groups | List permission groups
[**rename_permission_group**](PermissionGroupsApi.md#rename_permission_group) | **PUT** /api/v1/permission-groups/{id} | Rename permission group
[**set_permission_group_permissions**](PermissionGroupsApi.md#set_permission_group_permissions) | **PUT** /api/v1/permission-groups/{id}/permissions | Set permission group permissions


# **create_permission_group**
> PermissionGroup create_permission_group(permission_group)

Create permission group

Create a new permission group

### Example

* Basic Authentication (basic):

```python
import api
from api.models.permission_group import PermissionGroup
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
    api_instance = api.PermissionGroupsApi(api_client)
    permission_group = api.PermissionGroup() # PermissionGroup | 

    try:
        # Create permission group
        api_response = api_instance.create_permission_group(permission_group)
        print("The response of PermissionGroupsApi->create_permission_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PermissionGroupsApi->create_permission_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **permission_group** | [**PermissionGroup**](PermissionGroup.md)|  | 

### Return type

[**PermissionGroup**](PermissionGroup.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Permission group created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_permission_group**
> delete_permission_group(id)

Delete permission group

Delete a permission group

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
    api_instance = api.PermissionGroupsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete permission group
        api_instance.delete_permission_group(id)
    except Exception as e:
        print("Exception when calling PermissionGroupsApi->delete_permission_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

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
**200** | Permission group deleted |  -  |
**404** | Permission group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_permission_groups**
> PermissionGroupsReply list_permission_groups()

List permission groups

Get list of all permission groups

### Example

* Basic Authentication (basic):

```python
import api
from api.models.permission_groups_reply import PermissionGroupsReply
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
    api_instance = api.PermissionGroupsApi(api_client)

    try:
        # List permission groups
        api_response = api_instance.list_permission_groups()
        print("The response of PermissionGroupsApi->list_permission_groups:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PermissionGroupsApi->list_permission_groups: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**PermissionGroupsReply**](PermissionGroupsReply.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of permission groups |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **rename_permission_group**
> PermissionGroup rename_permission_group(id, permission_group)

Rename permission group

Rename an existing permission group

### Example

* Basic Authentication (basic):

```python
import api
from api.models.permission_group import PermissionGroup
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
    api_instance = api.PermissionGroupsApi(api_client)
    id = 'id_example' # str | 
    permission_group = api.PermissionGroup() # PermissionGroup | 

    try:
        # Rename permission group
        api_response = api_instance.rename_permission_group(id, permission_group)
        print("The response of PermissionGroupsApi->rename_permission_group:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PermissionGroupsApi->rename_permission_group: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **permission_group** | [**PermissionGroup**](PermissionGroup.md)|  | 

### Return type

[**PermissionGroup**](PermissionGroup.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Permission group renamed |  -  |
**404** | Permission group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_permission_group_permissions**
> set_permission_group_permissions(id, set_permission_group_permissions_request)

Set permission group permissions

Set the permissions for a permission group

### Example

* Basic Authentication (basic):

```python
import api
from api.models.set_permission_group_permissions_request import SetPermissionGroupPermissionsRequest
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
    api_instance = api.PermissionGroupsApi(api_client)
    id = 'id_example' # str | 
    set_permission_group_permissions_request = api.SetPermissionGroupPermissionsRequest() # SetPermissionGroupPermissionsRequest | 

    try:
        # Set permission group permissions
        api_instance.set_permission_group_permissions(id, set_permission_group_permissions_request)
    except Exception as e:
        print("Exception when calling PermissionGroupsApi->set_permission_group_permissions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **set_permission_group_permissions_request** | [**SetPermissionGroupPermissionsRequest**](SetPermissionGroupPermissionsRequest.md)|  | 

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
**200** | Permissions updated |  -  |
**404** | Permission group not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

