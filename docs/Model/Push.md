# Push

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | **string** | Registered UserId, Use * to push to a public channel | 
**channel** | **string** | Channel name to send push to | [optional] [default to 'default']
**content** | **string** | Text of the message | 
**data** | **object** | Data of the message in JSON | [optional] 
**track_id** | **string** | TrackId to track public pushes | [optional] 
**in_app** | **bool** | If push should be provided in-app to the user | [optional] [default to false]
**live** | **bool** | If the message should only be pushed to users currently online | [optional] [default to false]
**use_as_alert** | **bool** | Use the message text as the notification text | [optional] [default to false]
**alert_text** | **string** | Use separate text for the notification of this message | [optional] 
**ttl** | **double** | Expiry of the message, in seconds from the request time | [optional] 
**fallback** | **object** | Fallback message config for SMS | [optional] 
**client_id** | **string** | assign an ID of yours to track this message in your app | [optional] 
**notification** | **object** |  | [optional] 
**idr** | **bool** |  | [optional] 
**silent** | **bool** | If this message should not show a notification on user device | [optional] 
**content_binary** | **string** |  | [optional] 
**content_type** | **string** |  | [optional] 
**id** | **double** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


