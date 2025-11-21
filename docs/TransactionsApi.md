# api.TransactionsApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_transaction**](TransactionsApi.md#cancel_transaction) | **DELETE** /api/v1/transactions/{txID}/cancel | Cancel transaction
[**check_transaction_status**](TransactionsApi.md#check_transaction_status) | **GET** /api/v1/transactions/{txID}/check | Check transaction status
[**get_transaction_history**](TransactionsApi.md#get_transaction_history) | **GET** /api/v1/transactions/{txID}/history | Get transaction history
[**list_transactions**](TransactionsApi.md#list_transactions) | **GET** /api/v1/transactions | List transactions
[**set_transaction_tags**](TransactionsApi.md#set_transaction_tags) | **PUT** /api/v1/transactions/{txID}/tags | Set transaction tags


# **cancel_transaction**
> cancel_transaction(tx_id)

Cancel transaction

Cancel a pending transaction

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
    api_instance = api.TransactionsApi(api_client)
    tx_id = 'tx_id_example' # str | 

    try:
        # Cancel transaction
        api_instance.cancel_transaction(tx_id)
    except Exception as e:
        print("Exception when calling TransactionsApi->cancel_transaction: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tx_id** | **str**|  | 

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
**200** | Transaction cancelled |  -  |
**400** | Cannot cancel transaction in current state |  -  |
**403** | Forbidden |  -  |
**404** | Transaction not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **check_transaction_status**
> CheckTransactionStatus200Response check_transaction_status(tx_id)

Check transaction status

Get the current status of a transaction

### Example

* Basic Authentication (basic):

```python
import api
from api.models.check_transaction_status200_response import CheckTransactionStatus200Response
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
    api_instance = api.TransactionsApi(api_client)
    tx_id = 'tx_id_example' # str | 

    try:
        # Check transaction status
        api_response = api_instance.check_transaction_status(tx_id)
        print("The response of TransactionsApi->check_transaction_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransactionsApi->check_transaction_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tx_id** | **str**|  | 

### Return type

[**CheckTransactionStatus200Response**](CheckTransactionStatus200Response.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Transaction status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_transaction_history**
> Transaction get_transaction_history(tx_id)

Get transaction history

Get historical transaction details (including expired)

### Example

* Basic Authentication (basic):

```python
import api
from api.models.transaction import Transaction
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
    api_instance = api.TransactionsApi(api_client)
    tx_id = 'tx_id_example' # str | 

    try:
        # Get transaction history
        api_response = api_instance.get_transaction_history(tx_id)
        print("The response of TransactionsApi->get_transaction_history:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransactionsApi->get_transaction_history: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tx_id** | **str**|  | 

### Return type

[**Transaction**](Transaction.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Transaction history |  -  |
**404** | Transaction not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_transactions**
> PaginatedTransactions list_transactions(page=page, per_page=per_page, q=q)

List transactions

Get paginated list of all transactions

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
    api_instance = api.TransactionsApi(api_client)
    page = 56 # int |  (optional)
    per_page = 56 # int |  (optional)
    q = 'q_example' # str |  (optional)

    try:
        # List transactions
        api_response = api_instance.list_transactions(page=page, per_page=per_page, q=q)
        print("The response of TransactionsApi->list_transactions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TransactionsApi->list_transactions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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
**200** | List of transactions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_transaction_tags**
> set_transaction_tags(tx_id, set_transaction_tags_request)

Set transaction tags

Set tags for a specific transaction

### Example

* Basic Authentication (basic):

```python
import api
from api.models.set_transaction_tags_request import SetTransactionTagsRequest
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
    api_instance = api.TransactionsApi(api_client)
    tx_id = 'tx_id_example' # str | 
    set_transaction_tags_request = api.SetTransactionTagsRequest() # SetTransactionTagsRequest | 

    try:
        # Set transaction tags
        api_instance.set_transaction_tags(tx_id, set_transaction_tags_request)
    except Exception as e:
        print("Exception when calling TransactionsApi->set_transaction_tags: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **tx_id** | **str**|  | 
 **set_transaction_tags_request** | [**SetTransactionTagsRequest**](SetTransactionTagsRequest.md)|  | 

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
**404** | Transaction not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

