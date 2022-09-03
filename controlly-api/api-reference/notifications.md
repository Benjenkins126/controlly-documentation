---
description: Here you can find the endpoints related to Notifications on Controlly
---

# Notifications

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

{% swagger-response status="401: Unauthorized" description="" %}
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
    "message": "There has been an error creating a notification. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}
