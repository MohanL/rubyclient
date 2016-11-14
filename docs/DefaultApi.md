# SwaggerClient::DefaultApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**contracts_post**](DefaultApi.md#contracts_post) | **POST** /Contracts | Contract page returns contracts
[**root_post**](DefaultApi.md#root_post) | **POST** / | Home page returns recent contracts and recent tours for homepage


# **contracts_post**
> InlineResponse200 contracts_post(contract_status)

Contract page returns contracts

Contracts are returned based on the contract status value from {unassigned, active, completed} 

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::DefaultApi.new

contract_status = "contract_status_example" # String | contract_status value that need to be considered for filter


begin
  #Contract page returns contracts
  result = api_instance.contracts_post(contract_status)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling DefaultApi->contracts_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **contract_status** | **String**| contract_status value that need to be considered for filter | 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml



# **root_post**
> InlineResponse200 root_post(user_id)

Home page returns recent contracts and recent tours for homepage

Recent Contracts show the 5 most recently created and unassigned contracts. The contracts shown will be filtered according to the user's role and location.  Recent Tours shows the status of the 5 most recent tours the user has visited. It's likely the most frequently tours are the ones actively being worked on. 

### Example
```ruby
# load the gem
require 'swagger_client'

api_instance = SwaggerClient::DefaultApi.new

user_id = 3.4 # Float | user_id value that need to be considered for filter


begin
  #Home page returns recent contracts and recent tours for homepage
  result = api_instance.root_post(user_id)
  p result
rescue SwaggerClient::ApiError => e
  puts "Exception when calling DefaultApi->root_post: #{e}"
end
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_id** | **Float**| user_id value that need to be considered for filter | 

### Return type

[**InlineResponse200**](InlineResponse200.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json, application/xml



