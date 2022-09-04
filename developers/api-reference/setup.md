---
description: Here you can find endpoints related to Setup with Controlly
---

# 🔧 Setup

## Get current setup step

{% swagger method="get" path="/setup/step" baseUrl="https://your-ip-address:4083/api/v1" summary="Get the current stage that setup is on (Non-Authenticated)" %}
{% swagger-description %}
Check the stage that the application is currently on during setup
{% endswagger-description %}

{% swagger-response status="200: OK" description="Return current stage" %}
```javascript
{
    "status": "success",
    "stage": 1
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error getting the setup stage. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}

## Set current setup step

{% swagger method="post" path="/setup/step" baseUrl="https://your-ip-address:4083/api/v1" summary="Set the current stage that setup is on (Non-Authenticated)" %}
{% swagger-description %}
Alter the stage that the current stage is on during setup. This endpoint is only available whilst the device is in setup mode.
{% endswagger-description %}

{% swagger-parameter in="query" name="stage" type="Integer" required="true" %}
The setup phase (1, 2, 3, 0 = Complete)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Stage updated successfully" %}
```javascript
{
    "status": "success",
    "message": "The setup stage has been updated successfully"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error setting the setup stage. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}

## Run a systems health check

{% swagger method="get" path="/setup/health-check" baseUrl="https://your-ip-address:4083/api/v1" summary="Run a systems health check and return the results to the user (Non-Authenticated)" %}
{% swagger-description %}
Start a systems health check and return the results to the end-user during the setup phase. This can only be run during the setup phase
{% endswagger-description %}

{% swagger-response status="200: OK" description="Returns Health Check results" %}
```javascript
{
    "status": "success",
    "results": {
        "webServerConfiguration": {
            status: true,
            message: "Your Controlly Web Server is setup successfully."
        },
        "controllyCoreService": {
            status: true,
            message: "Your Controlly Core is online and operational."
        },
        "updatesServerConnection": {
            status: false,
            message: "Your Controlly instance cannot connect to the updates server. This will prevent you from using Over-the-air updates"
        },
        "acceptableServerSpeed": {
            status: false,
            message: "Your Controlly Web Server had a 1000ms ping to Controlly Core. This can cause delays in actions"
        }
    }
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error running the system health check. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}

## Update core details of product

{% swagger method="post" path="/setup/core" baseUrl="https://your-ip-address:4083/api/v1" summary="Update the core details of the application (Non-Authenticated)" %}
{% swagger-description %}
Update the core details of the application during setup. This can only be set during the setup phase
{% endswagger-description %}

{% swagger-parameter in="query" name="homeName" type="String" required="true" %}
The Controlly Instance name
{% endswagger-parameter %}

{% swagger-parameter in="query" name="homeDomain" type="String" %}
The Controlly Instance external domain name
{% endswagger-parameter %}

{% swagger-parameter in="query" name="homeTimezone" type="String" required="true" %}
The Controlly Instance timezone
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Updated Core Details" %}
```javascript
{
    "status": "success",
    "message": "The core details have been updated successfully"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error setting core details. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}
