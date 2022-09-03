---
description: Here you can find the endpoints related to Notifications on Controlly
---

# 🔔 Notification

## Creating a notification

{% swagger method="post" path="/notification" baseUrl="https://your-ip-address:4083/api/v1" summary="Create Notification" %}
{% swagger-description %}
This will create a notification and show the notification to active panel users.
{% endswagger-description %}

{% swagger-parameter in="body" name="name" required="true" type="String" %}
The name/text of the notification
{% endswagger-parameter %}

{% swagger-parameter in="body" name="url" required="false" type="String" %}
Where to send the user upon clicking the notification
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Notification Created" %}
```javascript
{
    "status": "success",
    "message": "The notification has been submitted successfully"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Not Authenticated" %}
```javascript
{
    "status": "error",
    "message": "You are not authorised to access this"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error creating a notification. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}

## Retrieving notifications

{% swagger method="get" path="/notification" baseUrl="https://your-ip-address:4083/api/v1" summary="Retrive Active Notifications" %}
{% swagger-description %}
Retrieve all active notifications that have not been dismissed
{% endswagger-description %}

{% swagger-response status="200: OK" description="Retrieved Notifications. Array of notification objects" %}
```javascript
[
    {
        "id": 1,
        "name": "Someone is at your front door",
        "timestamp": "2022-08-28T00:00:00+00:00",
        "url": "/devices/front-door"
    }
]
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Not Authenticated" %}
```javascript
{
    "status": "error",
    "message": "You are not authorised to access this"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error getting notifications. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}

## Dismissing notifications

{% swagger method="delete" path="/notification" baseUrl="https://your-ip-address:4083/api/v1" summary="Dismiss a notification" %}
{% swagger-description %}
Dismissing a notification will remove it from the SQLite Database resulting in it being hidden to the end-user
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" %}
Either a numeric integer or "all" to dismiss all notifications 
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Notification Dismissed" %}
```javascript
{
    "status": "success",
    "message": "The notification has been deleted successfully"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Not Authenticated" %}
```javascript
{
    "status": "error",
    "message": "You are not authorised to access this"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
{
    "status": "error",
    "message": "There has been an error dismissing this notification. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}
