# api.SettingsApi

All URIs are relative to *https://api.sendauth.com*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_settings**](SettingsApi.md#get_settings) | **GET** /api/v1/settings | Get organization settings
[**update_settings**](SettingsApi.md#update_settings) | **PUT** /api/v1/settings | Update organization settings


# **get_settings**
> Settings get_settings()

Get organization settings

Get current organization settings

### Example

* Basic Authentication (basic):

```python
import api
from api.models.settings import Settings
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
    api_instance = api.SettingsApi(api_client)

    try:
        # Get organization settings
        api_response = api_instance.get_settings()
        print("The response of SettingsApi->get_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->get_settings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**Settings**](Settings.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Organization settings |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_settings**
> Settings update_settings(settings)

Update organization settings

Update organization settings

### Example

* Basic Authentication (basic):

```python
import api
from api.models.settings import Settings
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
    api_instance = api.SettingsApi(api_client)
    settings = api.Settings() # Settings | 

    try:
        # Update organization settings
        api_response = api_instance.update_settings(settings)
        print("The response of SettingsApi->update_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SettingsApi->update_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **settings** | [**Settings**](Settings.md)|  | 

### Return type

[**Settings**](Settings.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Settings updated |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

