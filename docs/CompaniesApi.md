# api.CompaniesApi

All URIs are relative to *https://app.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_company**](CompaniesApi.md#create_company) | **POST** /api/v1/companies | Create company
[**delete_company**](CompaniesApi.md#delete_company) | **DELETE** /api/v1/companies/{id} | Delete company
[**list_companies**](CompaniesApi.md#list_companies) | **GET** /api/v1/companies | List companies
[**update_company**](CompaniesApi.md#update_company) | **PUT** /api/v1/companies/{id} | Update company


# **create_company**
> Company create_company(company)

Create company

Create a new company

### Example

* Basic Authentication (basic):

```python
import api
from api.models.company import Company
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
    api_instance = api.CompaniesApi(api_client)
    company = api.Company() # Company | 

    try:
        # Create company
        api_response = api_instance.create_company(company)
        print("The response of CompaniesApi->create_company:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompaniesApi->create_company: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **company** | [**Company**](Company.md)|  | 

### Return type

[**Company**](Company.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Company created |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_company**
> delete_company(id)

Delete company

Delete a company

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
    api_instance = api.CompaniesApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete company
        api_instance.delete_company(id)
    except Exception as e:
        print("Exception when calling CompaniesApi->delete_company: %s\n" % e)
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
**200** | Company deleted |  -  |
**404** | Company not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_companies**
> List[Company] list_companies()

List companies

Get paginated list of companies

### Example

* Basic Authentication (basic):

```python
import api
from api.models.company import Company
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
    api_instance = api.CompaniesApi(api_client)

    try:
        # List companies
        api_response = api_instance.list_companies()
        print("The response of CompaniesApi->list_companies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompaniesApi->list_companies: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[Company]**](Company.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of companies |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_company**
> Company update_company(id, company)

Update company

Update company details

### Example

* Basic Authentication (basic):

```python
import api
from api.models.company import Company
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
    api_instance = api.CompaniesApi(api_client)
    id = 'id_example' # str | 
    company = api.Company() # Company | 

    try:
        # Update company
        api_response = api_instance.update_company(id, company)
        print("The response of CompaniesApi->update_company:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CompaniesApi->update_company: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **company** | [**Company**](Company.md)|  | 

### Return type

[**Company**](Company.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Company updated |  -  |
**404** | Company not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

