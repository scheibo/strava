# \SegmentEffortsApi

All URIs are relative to *https://www.strava.com/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetEffortsBySegmentId**](SegmentEffortsApi.md#GetEffortsBySegmentId) | **Get** /segments/{id}/all_efforts | List Segment Efforts
[**GetSegmentEffortById**](SegmentEffortsApi.md#GetSegmentEffortById) | **Get** /segment_efforts/{id} | Get Segment Effort


# **GetEffortsBySegmentId**
> []DetailedSegmentEffort GetEffortsBySegmentId(ctx, id, optional)
List Segment Efforts

Returns a set of the authenticated athlete's segment efforts for a given segment.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int32**| The identifier of the segment. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int32**| The identifier of the segment. | 
 **page** | **int32**| Page number. | 
 **perPage** | **int32**| Number of items per page. Defaults to 30. | [default to 30]

### Return type

[**[]DetailedSegmentEffort**](DetailedSegmentEffort.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetSegmentEffortById**
> DetailedSegmentEffort GetSegmentEffortById(ctx, id)
Get Segment Effort

Returns a segment effort from an activity that is owned by the authenticated athlete.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the segment effort. | 

### Return type

[**DetailedSegmentEffort**](DetailedSegmentEffort.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

