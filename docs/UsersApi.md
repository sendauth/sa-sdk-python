# api.UsersApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**authenticate_user**](UsersApi.md#authenticate_user) | **POST** /api/v1/users/{userID}/authenticate | Authenticate user
[**create_user**](UsersApi.md#create_user) | **POST** /api/v1/users | Create user
[**delete_user**](UsersApi.md#delete_user) | **DELETE** /api/v1/users/{userID} | Delete user
[**destroy_user**](UsersApi.md#destroy_user) | **DELETE** /api/v1/users/deleted/{userID} | Permanently delete user
[**get_user**](UsersApi.md#get_user) | **GET** /api/v1/users/{userID} | Get user
[**get_user_audits**](UsersApi.md#get_user_audits) | **GET** /api/v1/users/{userID}/audits | Get user audits
[**get_user_transactions**](UsersApi.md#get_user_transactions) | **GET** /api/v1/users/{userID}/transactions | Get user transactions
[**list_deleted_users**](UsersApi.md#list_deleted_users) | **GET** /api/v1/users/deleted | List deleted users
[**list_users**](UsersApi.md#list_users) | **GET** /api/v1/users | List users
[**register_user**](UsersApi.md#register_user) | **POST** /api/v1/users/{userID}/register | Register user
[**remove_user_passkey**](UsersApi.md#remove_user_passkey) | **DELETE** /api/v1/users/{userID}/passkey | Remove user passkey
[**restore_user**](UsersApi.md#restore_user) | **PUT** /api/v1/users/deleted/{userID} | Restore deleted user
[**set_user_tags**](UsersApi.md#set_user_tags) | **PUT** /api/v1/users/{userID}/tags | Set user tags
[**update_user**](UsersApi.md#update_user) | **PUT** /api/v1/users/{userID} | Update user


# **authenticate_user**
> TX authenticate_user(user_id, web_tx=web_tx)

Authenticate user

Create an authentication transaction for a user

### Example

* Basic Authentication (basic):

```python
import api
from api.models.tx import TX
from api.models.web_tx import WebTX
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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 
    web_tx = api.WebTX() # WebTX |  (optional)

    try:
        # Authenticate user
        api_response = api_instance.authenticate_user(user_id, web_tx=web_tx)
        print("The response of UsersApi->authenticate_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->authenticate_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 
 **web_tx** | [**WebTX**](WebTX.md)|  | [optional] 

### Return type

[**TX**](TX.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Authentication transaction created |  -  |
**404** | User not found |  -  |
**406** | User has no passkeys |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_user**
> User create_user(user)

Create user

Create a new user

### Example

* Basic Authentication (basic):

```python
import api
from api.models.user import User
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
    api_instance = api.UsersApi(api_client)
    user = api.User() # User | 

    try:
        # Create user
        api_response = api_instance.create_user(user)
        print("The response of UsersApi->create_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->create_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user** | [**User**](User.md)|  | 

### Return type

[**User**](User.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | User created |  -  |
**403** | Insufficient permissions |  -  |
**422** | User already exists |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_user**
> delete_user(user_id)

Delete user

Soft delete a user

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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Delete user
        api_instance.delete_user(user_id)
    except Exception as e:
        print("Exception when calling UsersApi->delete_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

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
**200** | User deleted |  -  |
**403** | Cannot delete own account |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **destroy_user**
> destroy_user(user_id)

Permanently delete user

Permanently delete a soft-deleted user

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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Permanently delete user
        api_instance.destroy_user(user_id)
    except Exception as e:
        print("Exception when calling UsersApi->destroy_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

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
**200** | User permanently deleted |  -  |
**404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user**
> User get_user(user_id)

Get user

Get user details by ID

### Example

* Basic Authentication (basic):

```python
import api
from api.models.user import User
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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Get user
        api_response = api_instance.get_user(user_id)
        print("The response of UsersApi->get_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->get_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

### Return type

[**User**](User.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User details |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user_audits**
> PaginatedAudits get_user_audits(user_id, page=page, per_page=per_page, q=q)

Get user audits

Get paginated list of audit logs for a user

### Example

* Basic Authentication (basic):

```python
import api
from api.models.paginated_audits import PaginatedAudits
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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 
    page = 56 # int |  (optional)
    per_page = 56 # int |  (optional)
    q = 'q_example' # str |  (optional)

    try:
        # Get user audits
        api_response = api_instance.get_user_audits(user_id, page=page, per_page=per_page, q=q)
        print("The response of UsersApi->get_user_audits:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->get_user_audits: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 
 **page** | **int**|  | [optional] 
 **per_page** | **int**|  | [optional] 
 **q** | **str**|  | [optional] 

### Return type

[**PaginatedAudits**](PaginatedAudits.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of user audits |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user_transactions**
> PaginatedTransactions get_user_transactions(user_id, page=page, per_page=per_page, q=q)

Get user transactions

Get paginated list of transactions for a user

### Example

* Basic Authentication (basic):

```python
import api
from api.models.paginated_transactions import PaginatedTransactions
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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 
    page = 56 # int |  (optional)
    per_page = 56 # int |  (optional)
    q = 'q_example' # str |  (optional)

    try:
        # Get user transactions
        api_response = api_instance.get_user_transactions(user_id, page=page, per_page=per_page, q=q)
        print("The response of UsersApi->get_user_transactions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->get_user_transactions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 
 **page** | **int**|  | [optional] 
 **per_page** | **int**|  | [optional] 
 **q** | **str**|  | [optional] 

### Return type

[**PaginatedTransactions**](PaginatedTransactions.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of user transactions |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_deleted_users**
> PaginatedUsers list_deleted_users(page=page, per_page=per_page, q=q, permission=permission)

List deleted users

Get paginated list of deleted users

### Example

* Basic Authentication (basic):

```python
import api
from api.models.paginated_users import PaginatedUsers
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
    api_instance = api.UsersApi(api_client)
    page = 56 # int |  (optional)
    per_page = 56 # int |  (optional)
    q = 'q_example' # str |  (optional)
    permission = 'permission_example' # str |  (optional)

    try:
        # List deleted users
        api_response = api_instance.list_deleted_users(page=page, per_page=per_page, q=q, permission=permission)
        print("The response of UsersApi->list_deleted_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->list_deleted_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **per_page** | **int**|  | [optional] 
 **q** | **str**|  | [optional] 
 **permission** | **str**|  | [optional] 

### Return type

[**PaginatedUsers**](PaginatedUsers.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of deleted users |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_users**
> PaginatedUsers list_users(page=page, per_page=per_page, q=q, permission=permission, sort_by=sort_by, sort_dir=sort_dir)

List users

Get paginated list of users

### Example

* Basic Authentication (basic):

```python
import api
from api.models.paginated_users import PaginatedUsers
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
    api_instance = api.UsersApi(api_client)
    page = 56 # int |  (optional)
    per_page = 56 # int |  (optional)
    q = 'q_example' # str |  (optional)
    permission = 'permission_example' # str |  (optional)
    sort_by = 'sort_by_example' # str |  (optional)
    sort_dir = 'sort_dir_example' # str |  (optional)

    try:
        # List users
        api_response = api_instance.list_users(page=page, per_page=per_page, q=q, permission=permission, sort_by=sort_by, sort_dir=sort_dir)
        print("The response of UsersApi->list_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->list_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int**|  | [optional] 
 **per_page** | **int**|  | [optional] 
 **q** | **str**|  | [optional] 
 **permission** | **str**|  | [optional] 
 **sort_by** | **str**|  | [optional] 
 **sort_dir** | **str**|  | [optional] 

### Return type

[**PaginatedUsers**](PaginatedUsers.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of users |  -  |
**500** | Internal server error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_user**
> TX register_user(user_id)

Register user

Create a registration transaction for a user

### Example

* Basic Authentication (basic):

```python
import api
from api.models.tx import TX
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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Register user
        api_response = api_instance.register_user(user_id)
        print("The response of UsersApi->register_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->register_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

### Return type

[**TX**](TX.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Registration transaction created |  -  |
**404** | User not found |  -  |
**406** | User already has passkeys |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_user_passkey**
> remove_user_passkey(user_id)

Remove user passkey

Remove all passkeys for a user

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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Remove user passkey
        api_instance.remove_user_passkey(user_id)
    except Exception as e:
        print("Exception when calling UsersApi->remove_user_passkey: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

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
**200** | Passkey removed |  -  |
**404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **restore_user**
> restore_user(user_id)

Restore deleted user

Restore a soft-deleted user

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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 

    try:
        # Restore deleted user
        api_instance.restore_user(user_id)
    except Exception as e:
        print("Exception when calling UsersApi->restore_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 

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
**200** | User restored |  -  |
**404** | User not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_user_tags**
> set_user_tags(user_id, tags_request=tags_request)

Set user tags

Set user tags for a specific user

### Example

* Basic Authentication (basic):

```python
import api
from api.models.tags_request import TagsRequest
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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 
    tags_request = api.TagsRequest() # TagsRequest |  (optional)

    try:
        # Set user tags
        api_instance.set_user_tags(user_id, tags_request=tags_request)
    except Exception as e:
        print("Exception when calling UsersApi->set_user_tags: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 
 **tags_request** | [**TagsRequest**](TagsRequest.md)|  | [optional] 

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
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_user**
> User update_user(user_id, user)

Update user

Update user details

### Example

* Basic Authentication (basic):

```python
import api
from api.models.user import User
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
    api_instance = api.UsersApi(api_client)
    user_id = 'user_id_example' # str | 
    user = api.User() # User | 

    try:
        # Update user
        api_response = api_instance.update_user(user_id, user)
        print("The response of UsersApi->update_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling UsersApi->update_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **str**|  | 
 **user** | [**User**](User.md)|  | 

### Return type

[**User**](User.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User updated |  -  |
**403** | Insufficient permissions |  -  |
**404** | Not found |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

