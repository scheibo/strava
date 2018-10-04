# \ActivitiesApi

All URIs are relative to *https://www.strava.com/api/v3*

Method | HTTP request | Description
------------- | ------------- | -------------
[**CreateActivity**](ActivitiesApi.md#CreateActivity) | **Post** /activities | Create an Activity
[**GetActivityById**](ActivitiesApi.md#GetActivityById) | **Get** /activities/{id} | Get Activity
[**GetCommentsByActivityId**](ActivitiesApi.md#GetCommentsByActivityId) | **Get** /activities/{id}/comments | List Activity Comments
[**GetKudoersByActivityId**](ActivitiesApi.md#GetKudoersByActivityId) | **Get** /activities/{id}/kudos | List Activity Kudoers
[**GetLapsByActivityId**](ActivitiesApi.md#GetLapsByActivityId) | **Get** /activities/{id}/laps | List Activity Laps
[**GetLoggedInAthleteActivities**](ActivitiesApi.md#GetLoggedInAthleteActivities) | **Get** /athlete/activities | List Athlete Activities
[**GetZonesByActivityId**](ActivitiesApi.md#GetZonesByActivityId) | **Get** /activities/{id}/zones | Get Activity Zones
[**UpdateActivityById**](ActivitiesApi.md#UpdateActivityById) | **Put** /activities/{id} | Update Activity


# **CreateActivity**
> DetailedActivity CreateActivity(ctx, name, type_, startDateLocal, elapsedTime, optional)
Create an Activity

Creates a manual activity for an athlete. Requires write permissions, as requested during the authorization process.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **name** | **string**| The name of the activity. | 
  **type_** | **string**| Type of activity. For example - Run, Ride etc. | 
  **startDateLocal** | **string**| ISO 8601 formatted date time. | 
  **elapsedTime** | **int32**| In seconds. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **name** | **string**| The name of the activity. | 
 **type_** | **string**| Type of activity. For example - Run, Ride etc. | 
 **startDateLocal** | **string**| ISO 8601 formatted date time. | 
 **elapsedTime** | **int32**| In seconds. | 
 **description** | **string**| Description of the activity. | 
 **distance** | **float32**| In meters. | 
 **private** | **int32**| set to 1 to mark the resulting activity as private, ‘view_private’ permissions will be necessary to view the activity. If not specified, set according to the athlete’s privacy setting (recommended). | 
 **trainer** | **int32**| Set to 1 to mark as a trainer activity. | 
 **photoIds** | **string**| List of native photo ids to attach to the activity. | 
 **commute** | **int32**| Set to 1 to mark as commute. | 

### Return type

[**DetailedActivity**](DetailedActivity.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetActivityById**
> DetailedActivity GetActivityById(ctx, id, optional)
Get Activity

Returns the given activity that is owned by the authenticated athlete.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the activity. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The identifier of the activity. | 
 **includeAllEfforts** | **bool**| To include all segments efforts. | 

### Return type

[**DetailedActivity**](DetailedActivity.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetCommentsByActivityId**
> []Comment GetCommentsByActivityId(ctx, id, optional)
List Activity Comments

Returns the comments on the given activity.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the activity. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The identifier of the activity. | 
 **page** | **int32**| Page number. | 
 **perPage** | **int32**| Number of items per page. Defaults to 30. | [default to 30]

### Return type

[**[]Comment**](Comment.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetKudoersByActivityId**
> []SummaryAthlete GetKudoersByActivityId(ctx, id, optional)
List Activity Kudoers

Returns the athletes who kudoed an activity identified by an identifier.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int32**| The identifier of the activity. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int32**| The identifier of the activity. | 
 **page** | **int32**| Page number. | 
 **perPage** | **int32**| Number of items per page. Defaults to 30. | [default to 30]

### Return type

[**[]SummaryAthlete**](SummaryAthlete.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetLapsByActivityId**
> []Lap GetLapsByActivityId(ctx, id)
List Activity Laps

Returns the laps of an activity identified by an identifier.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the activity. | 

### Return type

[**[]Lap**](Lap.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetLoggedInAthleteActivities**
> []SummaryActivity GetLoggedInAthleteActivities(ctx, optional)
List Athlete Activities

Returns the activities of an athlete for a specific identifier.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **before** | **int32**| An epoch timestamp to use for filtering activities that have taken place before a certain time. | 
 **after** | **int32**| An epoch timestamp to use for filtering activities that have taken place after a certain time. | 
 **page** | **int32**| Page number. | 
 **perPage** | **int32**| Number of items per page. Defaults to 30. | [default to 30]

### Return type

[**[]SummaryActivity**](SummaryActivity.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetZonesByActivityId**
> []ActivityZone GetZonesByActivityId(ctx, id)
Get Activity Zones

Summit Feature. Returns the zones of a given activity.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int32**| The identifier of the activity. | 

### Return type

[**[]ActivityZone**](ActivityZone.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **UpdateActivityById**
> DetailedActivity UpdateActivityById(ctx, id, optional)
Update Activity

Updates the given activity that is owned by the authenticated athlete.

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for logging, tracing, authentication, etc.
  **id** | **int64**| The identifier of the activity. | 
 **optional** | **map[string]interface{}** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a map[string]interface{}.

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **int64**| The identifier of the activity. | 
 **body** | [**UpdatableActivity**](UpdatableActivity.md)|  | 

### Return type

[**DetailedActivity**](DetailedActivity.md)

### Authorization

[strava_oauth](../README.md#strava_oauth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

