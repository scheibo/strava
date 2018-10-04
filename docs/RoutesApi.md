# \RoutesApi

All URIs are relative to *https://www.strava.com/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetRouteAsGPX**](RoutesApi.md#GetRouteAsGPX) | **Get** /routes/{id}/export_gpx | Export Route GPX
[**GetRouteAsTCX**](RoutesApi.md#GetRouteAsTCX) | **Get** /routes/{id}/export_tcx | Export Route TCX
[**GetRouteById**](RoutesApi.md#GetRouteById) | **Get** /routes/{id} | Get Route
[**GetRoutesByAthleteId**](RoutesApi.md#GetRoutesByAthleteId) | **Get** /athletes/{id}/routes | List Athlete Routes


# **GetRouteAsGPX**
> GetRouteAsGPX(ctx, id)
Export Route GPX

Returns a GPX file of the route.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int32**| The identifier of the route. | 

### Return type

 (empty response body)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetRouteAsTCX**
> GetRouteAsTCX(ctx, id)
Export Route TCX

Returns a TCX file of the route.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int32**| The identifier of the route. | 

### Return type

 (empty response body)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetRouteById**
> Route GetRouteById(ctx, id)
Get Route

Returns a route using its identifier.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int32**| The identifier of the route. | 

### Return type

[**Route**](Route.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetRoutesByAthleteId**
> []Route GetRoutesByAthleteId(ctx, id, optional)
List Athlete Routes

Returns a list of the routes created by the authenticated athlete using their athlete ID.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int32**| The identifier of the athlete. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int32**| The identifier of the athlete. | 
 **page** | **int32**| Page number. | 
 **perPage** | **int32**| Number of items per page. Defaults to 30. | [default to 30]

### Return type

[**[]Route**](Route.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

