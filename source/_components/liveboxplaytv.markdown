---
layout: page
title: "Orange Livebox Play TV"
description: "Instructions on how to integrate a Livebox Play TV appliance into Home Assistant."
date: 2017-01-25 07:27
sidebar: true
comments: false
sharing: true
footer: true
logo: orange.png
ha_category:
  - Media Player
ha_release: 0.38
ha_iot_class: Local Polling
redirect_from:
 - /components/media_player.liveboxplaytv/
---

The `liveboxplaytv` platform allows you to control [Orange Livebox Play TV appliances](https://boutique.orange.fr/internet/decodeur-tv-livebox).

## {% linkable_title Configuration %}

To add an Orange Livebox Play TV to your installation, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
media_player:
  - platform: liveboxplaytv
    host: 192.168.1.3
```

{% configuration %}
host:
  description: The IP address or hostname of the Orange Livebox Play TV appliance.
  required: true
  type: string
name:
  description: The name to use in the frontend.
  required: false
  default: "`Livebox Play TV`"
  type: string
port:
  description: The port on which the Livebox is listening on.
  required: false
  default: 8080
  type: integer
{% endconfiguration %}

## {% linkable_title Full configuration %}

A full configuration example for an Orange TV appliance can look like this:

```yaml
# Example configuration.yaml entry
media_player:
  - platform: liveboxplaytv
    host: 192.168.1.3
    port: 8080
    name: Orange Livebox Play TV
```
