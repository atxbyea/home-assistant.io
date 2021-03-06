---
title: "KNX Notify"
description: "Instructions on how to use the KNX notify with Home Assistant."
logo: knx.png
ha_category:
  - Notifications
ha_release: 0.53
ha_iot_class: Local Push
---

The `knx` notify platform allows you to send notifications to [KNX](http://www.knx.org) devices.

The `knx` integration must be configured correctly, see [KNX Component](/components/knx).

## Configuration

To use your KNX switch in your installation, add the following lines to your `configuration.yaml` file:

```yaml
notify:
  - platform: knx
    name: Alarm
    address: '5/1/10'
```

{% configuration %}
address:
  description: KNX group address of the notification.
  required: true
  type: string
name:
  description: A name for this device used within Home Assistant.
  required: false
  type: string
{% endconfiguration %}
