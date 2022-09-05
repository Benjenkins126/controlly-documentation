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

To access the API all requests must be authenticated using the x-access-token header. You can retrieve your access token by calling /api/v1/user/sign-in [#user](./#user "mention")

#### Example Authentication Header

```
"x-access-token: (Access_Token)"
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

## Search

Endpoints that relate to searching in Controlly.

{% content-ref url="search.md" %}
[search.md](search.md)
{% endcontent-ref %}

## Dashboard

Endpoints that relate to dashboards in Controlly.

{% content-ref url="dashboard.md" %}
[dashboard.md](dashboard.md)
{% endcontent-ref %}

## Device

Endpoints that relate to devices in Controlly.

{% content-ref url="device.md" %}
[device.md](device.md)
{% endcontent-ref %}

## Group

Endpoints that relate to groups in Controlly.

{% content-ref url="group.md" %}
[group.md](group.md)
{% endcontent-ref %}

## Automation

Endpoints that relate to automations in Controlly.

{% content-ref url="automation.md" %}
[automation.md](automation.md)
{% endcontent-ref %}

## Widget

Endpoints that relate to widgets in Controlly.

{% content-ref url="widget.md" %}
[widget.md](widget.md)
{% endcontent-ref %}

## Integration

Endpoints that relate to integrations in Controlly.

{% content-ref url="integration.md" %}
[integration.md](integration.md)
{% endcontent-ref %}

## Theme Configuration

Endpoints that relate to Theme Configuration in Controlly.

{% content-ref url="theme-configuration.md" %}
[theme-configuration.md](theme-configuration.md)
{% endcontent-ref %}

## Display Controller

Endpoints that relate to Display Controllers in Controlly.

{% content-ref url="display-controller.md" %}
[display-controller.md](display-controller.md)
{% endcontent-ref %}

## Settings

Endpoints that relate to Settings in Controlly.

{% content-ref url="settings.md" %}
[settings.md](settings.md)
{% endcontent-ref %}

## Updates

Endpoints that relate to OTA Updates in Controlly.

{% content-ref url="updates.md" %}
[updates.md](updates.md)
{% endcontent-ref %}

## Changelog

Endpoints that relate to Changelogs in Controlly.

{% content-ref url="changelog.md" %}
[changelog.md](changelog.md)
{% endcontent-ref %}
