---
description: >-
  The Controlly API is an internal reference used to display content on the
  Controlly Dashboard. You should not interact with this API due to updates
  being overwritten with our automatic OTA updates.
---

# API Reference

{% hint style="info" %}
Please refer to our Widget, Automation and Integration creation process if you would like to contribute to the Controlly Project
{% endhint %}

## Authentication

To access the API all requests must be authenticated using BASIC authentication. Passwords must be provided encrypted using an MD5 hash.

#### Example Authentication Header

```
"Authorization: Basic (USERNAME):(ENCRYPTED_PASSWORD)"
```

## Notifications

Endpoints that relate to sending, receiving and dismissing notifications through Controlly.

{% content-ref url="notification.md" %}
[notification.md](notification.md)
{% endcontent-ref %}

## User

Endpoints that relate to users in Controlly.

{% content-ref url="user.md" %}
[user.md](user.md)
{% endcontent-ref %}
