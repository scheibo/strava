# \SegmentsApi

All URIs are relative to *https://www.strava.com/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ExploreSegments**](SegmentsApi.md#ExploreSegments) | **Get** /segments/explore | Explore segments
[**GetLeaderboardBySegmentId**](SegmentsApi.md#GetLeaderboardBySegmentId) | **Get** /segments/{id}/leaderboard | Get Segment Leaderboard
[**GetLoggedInAthleteStarredSegments**](SegmentsApi.md#GetLoggedInAthleteStarredSegments) | **Get** /segments/starred | List Starred Segments
[**GetSegmentById**](SegmentsApi.md#GetSegmentById) | **Get** /segments/{id} | Get Segment
[**StarSegment**](SegmentsApi.md#StarSegment) | **Put** /segments/{id}/starred | Star Segment


# **ExploreSegments**
> ExplorerResponse ExploreSegments(ctx, bounds, optional)
Explore segments

Returns the top 10 segments matching a specified query.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **bounds** | [**[]float32**](float32.md)| The latitude and longitude for two points describing a rectangular boundary for the search: [southwest corner latitutde, southwest corner longitude, northeast corner latitude, northeast corner longitude] | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bounds** | [**[]float32**](float32.md)| The latitude and longitude for two points describing a rectangular boundary for the search: [southwest corner latitutde, southwest corner longitude, northeast corner latitude, northeast corner longitude] | 
 **activityType** | **string**| Desired activity type. | 
 **minCat** | **int32**| The minimum climbing category. | 
 **maxCat** | **int32**| The maximum climbing category. | 

### Return type

[**ExplorerResponse**](ExplorerResponse.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetLeaderboardBySegmentId**
> SegmentLeaderboard GetLeaderboardBySegmentId(ctx, id, optional)
Get Segment Leaderboard

Returns the specified segment leaderboard.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the segment leaderboard. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The identifier of the segment leaderboard. | 
 **gender** | **string**| Filter by gender. | 
 **ageGroup** | **string**| Summit Feature. Filter by age group. | 
 **weightClass** | **string**| Summit Feature. Filter by weight class. | 
 **following** | **bool**| Filter by friends of the authenticated athlete. | 
 **clubId** | **int64**| Filter by club. | 
 **dateRange** | **string**| Filter by date range. | 
 **contextEntries** | **int32**|  | 
 **page** | **int32**| Page number. | 
 **perPage** | **int32**| Number of items per page. Defaults to 30. | [default to 30]

### Return type

[**SegmentLeaderboard**](SegmentLeaderboard.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetLoggedInAthleteStarredSegments**
> []SummarySegment GetLoggedInAthleteStarredSegments(ctx, optional)
List Starred Segments

List of the authenticated athlete's starred segments.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **int32**| Page number. | 
 **perPage** | **int32**| Number of items per page. Defaults to 30. | [default to 30]

### Return type

[**[]SummarySegment**](SummarySegment.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetSegmentById**
> DetailedSegment GetSegmentById(ctx, id)
Get Segment

Returns the specified segment.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the segment. | 

### Return type

[**DetailedSegment**](DetailedSegment.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **StarSegment**
> DetailedSegment StarSegment(ctx, id, starred)
Star Segment

Stars/Unstars the given segment for the authenticated athlete.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the segment to star. | 
  **starred** | **bool**| If true, star the segment; if false, unstar the segment. | [default to false]

### Return type

[**DetailedSegment**](DetailedSegment.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

