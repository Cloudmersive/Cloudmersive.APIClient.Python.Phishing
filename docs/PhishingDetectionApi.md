# cloudmersive_phishing_api_client.PhishingDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**phishing_detect_email_advanced_post**](PhishingDetectionApi.md#phishing_detect_email_advanced_post) | **POST** /phishing/detect/email/advanced | Perform advanced AI phishing detection and classification against input email.  Analyzes input email as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
[**phishing_detect_file_advanced_post**](PhishingDetectionApi.md#phishing_detect_file_advanced_post) | **POST** /phishing/detect/file/advanced | Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
[**phishing_detect_file_post**](PhishingDetectionApi.md#phishing_detect_file_post) | **POST** /phishing/detect/file | Perform AI phishing detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.
[**phishing_detect_text_string_advanced_post**](PhishingDetectionApi.md#phishing_detect_text_string_advanced_post) | **POST** /phishing/detect/text-string/advanced | Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
[**phishing_detect_text_string_post**](PhishingDetectionApi.md#phishing_detect_text_string_post) | **POST** /phishing/detect/text-string | Perform AI phishing detection against input text string.  Returns a clean/not-clean result with confidence level and optional rationale.
[**phishing_detect_url_advanced_post**](PhishingDetectionApi.md#phishing_detect_url_advanced_post) | **POST** /phishing/detect/url/advanced | Perform advanced AI phishing detection and classification against an input URL.  Retrieves the URL content, checks for SSRF threats, and analyzes the page with AI deep learning to detect phishing and other unsafe content.  Uses 100-125 API calls.


# **phishing_detect_email_advanced_post**
> PhishingDetectionEmailAdvancedResponse phishing_detect_email_advanced_post(body=body)

Perform advanced AI phishing detection and classification against input email.  Analyzes input email as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_phishing_api_client
from cloudmersive_phishing_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_phishing_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_phishing_api_client.PhishingDetectionApi(cloudmersive_phishing_api_client.ApiClient(configuration))
body = cloudmersive_phishing_api_client.AdvancedEmailDetectionRequest() # AdvancedEmailDetectionRequest | Phishing detection request (optional)

try:
    # Perform advanced AI phishing detection and classification against input email.  Analyzes input email as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
    api_response = api_instance.phishing_detect_email_advanced_post(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PhishingDetectionApi->phishing_detect_email_advanced_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AdvancedEmailDetectionRequest**](AdvancedEmailDetectionRequest.md)| Phishing detection request | [optional] 

### Return type

[**PhishingDetectionEmailAdvancedResponse**](PhishingDetectionEmailAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **phishing_detect_file_advanced_post**
> PhishingDetectionAdvancedResponse phishing_detect_file_advanced_post(model=model, custom_policy_id=custom_policy_id, input_file=input_file)

Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_phishing_api_client
from cloudmersive_phishing_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_phishing_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_phishing_api_client.PhishingDetectionApi(cloudmersive_phishing_api_client.ApiClient(configuration))
model = 'Advanced' # str |  (optional) (default to Advanced)
custom_policy_id = 'custom_policy_id_example' # str |  (optional)
input_file = '/path/to/file.txt' # file |  (optional)

try:
    # Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learning to detect phishing, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
    api_response = api_instance.phishing_detect_file_advanced_post(model=model, custom_policy_id=custom_policy_id, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PhishingDetectionApi->phishing_detect_file_advanced_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **str**|  | [optional] [default to Advanced]
 **custom_policy_id** | **str**|  | [optional] 
 **input_file** | **file**|  | [optional] 

### Return type

[**PhishingDetectionAdvancedResponse**](PhishingDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **phishing_detect_file_post**
> PhishingDetectionResponse phishing_detect_file_post(model=model, input_file=input_file)

Perform AI phishing detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_phishing_api_client
from cloudmersive_phishing_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_phishing_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_phishing_api_client.PhishingDetectionApi(cloudmersive_phishing_api_client.ApiClient(configuration))
model = 'Advanced' # str | Model to use; default setting is Advanced (optional) (default to Advanced)
input_file = '/path/to/file.txt' # file |  (optional)

try:
    # Perform AI phishing detection and classification on an input image or document (PDF or DOCX).  Analyzes input content as well as embedded URLs with AI deep learnign to detect phishing and other unsafe content.  Uses 100-125 API calls depending on model selected.
    api_response = api_instance.phishing_detect_file_post(model=model, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PhishingDetectionApi->phishing_detect_file_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **model** | **str**| Model to use; default setting is Advanced | [optional] [default to Advanced]
 **input_file** | **file**|  | [optional] 

### Return type

[**PhishingDetectionResponse**](PhishingDetectionResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **phishing_detect_text_string_advanced_post**
> PhishingDetectionAdvancedResponse phishing_detect_text_string_advanced_post(body=body)

Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_phishing_api_client
from cloudmersive_phishing_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_phishing_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_phishing_api_client.PhishingDetectionApi(cloudmersive_phishing_api_client.ApiClient(configuration))
body = cloudmersive_phishing_api_client.PhishingDetectionAdvancedRequest() # PhishingDetectionAdvancedRequest | Phishing detection request (optional)

try:
    # Perform advanced AI phishing detection and classification against input text string.  Analyzes input content as well as embedded URLs with AI deep learnign to detect spam, phishing and other unsafe content.  Uses 25-100 API calls depending on model selected.
    api_response = api_instance.phishing_detect_text_string_advanced_post(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PhishingDetectionApi->phishing_detect_text_string_advanced_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhishingDetectionAdvancedRequest**](PhishingDetectionAdvancedRequest.md)| Phishing detection request | [optional] 

### Return type

[**PhishingDetectionAdvancedResponse**](PhishingDetectionAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **phishing_detect_text_string_post**
> PhishingDetectionTextStringResponse phishing_detect_text_string_post(body=body)

Perform AI phishing detection against input text string.  Returns a clean/not-clean result with confidence level and optional rationale.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_phishing_api_client
from cloudmersive_phishing_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_phishing_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_phishing_api_client.PhishingDetectionApi(cloudmersive_phishing_api_client.ApiClient(configuration))
body = cloudmersive_phishing_api_client.PhishingDetectionTextStringRequest() # PhishingDetectionTextStringRequest | Phishing detection request (optional)

try:
    # Perform AI phishing detection against input text string.  Returns a clean/not-clean result with confidence level and optional rationale.
    api_response = api_instance.phishing_detect_text_string_post(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PhishingDetectionApi->phishing_detect_text_string_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**PhishingDetectionTextStringRequest**](PhishingDetectionTextStringRequest.md)| Phishing detection request | [optional] 

### Return type

[**PhishingDetectionTextStringResponse**](PhishingDetectionTextStringResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **phishing_detect_url_advanced_post**
> PhishingDetectionUrlAdvancedResponse phishing_detect_url_advanced_post(body=body)

Perform advanced AI phishing detection and classification against an input URL.  Retrieves the URL content, checks for SSRF threats, and analyzes the page with AI deep learning to detect phishing and other unsafe content.  Uses 100-125 API calls.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_phishing_api_client
from cloudmersive_phishing_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_phishing_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_phishing_api_client.PhishingDetectionApi(cloudmersive_phishing_api_client.ApiClient(configuration))
body = cloudmersive_phishing_api_client.AdvancedUrlDetectionRequest() # AdvancedUrlDetectionRequest | URL phishing detection request (optional)

try:
    # Perform advanced AI phishing detection and classification against an input URL.  Retrieves the URL content, checks for SSRF threats, and analyzes the page with AI deep learning to detect phishing and other unsafe content.  Uses 100-125 API calls.
    api_response = api_instance.phishing_detect_url_advanced_post(body=body)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling PhishingDetectionApi->phishing_detect_url_advanced_post: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**AdvancedUrlDetectionRequest**](AdvancedUrlDetectionRequest.md)| URL phishing detection request | [optional] 

### Return type

[**PhishingDetectionUrlAdvancedResponse**](PhishingDetectionUrlAdvancedResponse.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

