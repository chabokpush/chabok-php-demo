# SegmentPush

## Properties
Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**target** | **object** | Segment query you can use many parameters | 
**channel** | **string** | Channel name to send push to | [optional] [default to 'default']
**content** | **string** | Text of the message | 
**data** | **object** | Data of the message in JSON | [optional] 
**track_id** | **string** | TrackId to track public pushes | [optional] 
**in_app** | **bool** | If push should be provided in-app to the user | [optional] [default to false]
**live** | **bool** | If the message should only be pushed to users currently online | [optional] [default to false]
**use_as_alert** | **bool** | Use the message text as the notification text | [optional] [default to false]
**alert_text** | **string** | Use separate text for the notification of this message | [optional] 
**ttl** | **double** | Expiry of the message, in seconds from the request time | [optional] 
**id** | **double** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


