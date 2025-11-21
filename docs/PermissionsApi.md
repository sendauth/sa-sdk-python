# api.PermissionsApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_permission**](PermissionsApi.md#create_permission) | **POST** /api/v1/permissions | Create permission
[**delete_permission**](PermissionsApi.md#delete_permission) | **DELETE** /api/v1/permissions/{name} | Delete permission
[**list_permissions**](PermissionsApi.md#list_permissions) | **GET** /api/v1/permissions | List permissions
[**rename_permission**](PermissionsApi.md#rename_permission) | **PUT** /api/v1/permissions/{name} | Rename permission


# **create_permission**
> Permission create_permission(permission)

Create permission

Create a new permission

### Example

* Basic Authentication (basic):

```python
import api
from api.models.permission import Permission
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
    api_instance = api.PermissionsApi(api_client)
    permission = api.Permission() # Permission | 

    try:
        # Create permission
        api_response = api_instance.create_permission(permission)
        print("The response of PermissionsApi->create_permission:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PermissionsApi->create_permission: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **permission** | [**Permission**](Permission.md)|  | 

### Return type

[**Permission**](Permission.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Permission created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_permission**
> delete_permission(name)

Delete permission

Delete a permission

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
    api_instance = api.PermissionsApi(api_client)
    name = 'name_example' # str | 

    try:
        # Delete permission
        api_instance.delete_permission(name)
    except Exception as e:
        print("Exception when calling PermissionsApi->delete_permission: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**|  | 

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
**200** | Permission deleted |  -  |
**404** | Permission not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_permissions**
> PermissionsReply list_permissions()

List permissions

Get list of all permissions

### Example

* Basic Authentication (basic):

```python
import api
from api.models.permissions_reply import PermissionsReply
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
    api_instance = api.PermissionsApi(api_client)

    try:
        # List permissions
        api_response = api_instance.list_permissions()
        print("The response of PermissionsApi->list_permissions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PermissionsApi->list_permissions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**PermissionsReply**](PermissionsReply.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of permissions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **rename_permission**
> Permission rename_permission(name, permission)

Rename permission

Rename an existing permission

### Example

* Basic Authentication (basic):

```python
import api
from api.models.permission import Permission
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
    api_instance = api.PermissionsApi(api_client)
    name = 'name_example' # str | 
    permission = api.Permission() # Permission | 

    try:
        # Rename permission
        api_response = api_instance.rename_permission(name, permission)
        print("The response of PermissionsApi->rename_permission:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling PermissionsApi->rename_permission: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **str**|  | 
 **permission** | [**Permission**](Permission.md)|  | 

### Return type

[**Permission**](Permission.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Permission renamed |  -  |
**404** | Permission not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

