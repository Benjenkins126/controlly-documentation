---
description: Here you can find the endpoints related to Changelogs on Controlly
---

# ❗ Changelog

## Retrieve changelogs

{% swagger method="get" path="/changelog" baseUrl="https://your-ip-address:4083/api/v1" summary="Retrieve all changelogs" %}
{% swagger-description %}
This method will return all changelogs that are actively installed on the Controlly application.
{% endswagger-description %}

{% swagger-response status="200: OK" description="Return an array of changelogs" %}
```javascript
[
    {
        "id": 1,
        "version": "1.0",
        "release_date": "2022-08-28T00:00:00+00:00"
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
    "message": "There has been an error getting changelogs. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}

## Retrieve specific changelog

{% swagger method="get" path="/changelog" baseUrl="https://your-ip-address:4083/api/v1" summary="Retrieve a specific changelog" %}
{% swagger-description %}
This method will return additional information about a specific changelog entry.
{% endswagger-description %}

{% swagger-parameter in="query" name="changelogID" type="Integer" required="true" %}
The ID of the changelog that you want details for
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Returns details on specific changelog" %}
```javascript
[
    {
        "id": 1,
        "changelog_version": 1,
        "name": "Controlly Officially Released!",
        "excerpt": "After many months of development version 1.0 is finally here...",
        "image_path": "/assets/img/changelogs/1.0/controlly-released.png",
        "details": "Full HTML Description will be presented in this field"
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
    "message": "There has been an error getting this notification. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}
