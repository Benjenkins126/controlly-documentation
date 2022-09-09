---
description: Here you can find all endpoints relating to the user on Controlly.
---

# 🧑 User

## Sign In

{% swagger method="post" path="/sign-in" baseUrl="https://your-ip-address:4083/api/v1/user" summary="Sign In" %}
{% swagger-description %}
This will return the login token needed to authenticate requests to the API
{% endswagger-description %}

{% swagger-parameter in="query" name="username" required="true" type="String" %}
The Username or Email Address of the user
{% endswagger-parameter %}

{% swagger-parameter in="query" name="password" required="true" type="String" %}
The Password of the user
{% endswagger-parameter %}

{% swagger-parameter in="query" name="ip_address" required="true" type="String" %}
The IP Address of the user attempting to login
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Return the user token that will authenticate requests to the API" %}
```javascript
{
    "status": "success",
    "token": "(Authentication Token)"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Missing Parameters" %}
```javascript
{
    "status": "error",
    "message": "The fields username, password and ip_address are not all present"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Invalid Credentials" %}
```javascript
{
    "status": "error",
    "message": "Your credentials are incorrect"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error checking your credentials. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}

## Sign Up

{% swagger method="post" path="/sign-up" baseUrl="https://your-ip-address:4083/api/v1/user" summary="Sign Up" %}
{% swagger-description %}
Create a user to access Controlly. This can only be run when the Setup Status is set to 3
{% endswagger-description %}

{% swagger-parameter in="query" name="email_address" type="String" required="true" %}
Email Address of user
{% endswagger-parameter %}

{% swagger-parameter in="query" name="username" type="String" required="true" %}
Username of user
{% endswagger-parameter %}

{% swagger-parameter in="query" name="password" type="String" required="true" %}
Password of user
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Account Created Successfully" %}
```javascript
{
    "status": "success",
    "message": "Your account has been created successfully"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Password does not contain uppercase and lowercase characters" %}
```javascript
{
    "status": "error",
    "message": "The password must contain both uppercase and lowercase characters"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Password does not contain a number" %}
```javascript
{
    "status": "error",
    "message": "The password must contain at least 1 number"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Password is too short or too long" %}
```javascript
{
    "status": "error",
    "message": "The password length must be between 8-64 characters in length"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Username is too short or too long" %}
```javascript
{
    "status": "error",
    "message": "The username length must be between 3-16 characters in length"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Email Address is not valid" %}
```javascript
{
    "status": "error",
    "message": "Your email address is not valid"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Missing Parameters" %}
```javascript
{
    "status": "error",
    "message": "The fields 'email_address', 'username' or 'password' are not present"
}
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="Invalid setup stage" %}
```javascript
{
    "status": "error",
    "message": "You are currently in the incorrect setup stage to be creating a user"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="Server Error" %}
```javascript
{
    "status": "error",
    "message": "There has been an error setting up the administrator. Please check your Controlly Log for information"
}
```
{% endswagger-response %}
{% endswagger %}
