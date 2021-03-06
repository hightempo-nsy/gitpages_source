---
title: 중국 온도조절기(ZhongHong)
description: Instructions on how to integrate ZhongHong Support thermostats within Home Assistant.
logo: zhong_hong.png
ha_category:
  - Climate
ha_release: 0.72
ha_iot_class: Local Push
---

The `zhong_hong` climate platform lets you control [Zhonghong HVAC Gateway Controller](http://zhonghongtech.cn/v1/index.shtml) thermostats through Home Assistant.

To set it up, add the following information to your configuration.yaml file:

```yaml
climate:
  - platform: zhong_hong
    host: GATEWAY_IP
```

{% configuration %}
host:
  description: The IP address of your controller.
  required: true
  type: string
port:
  description: The port of your controller.
  required: false
  default: 9999
  type: integer
gateway_address:
  description: The gateway address for the gateway (Settings in the controller itself).
  required: false
  default: 1
  type: integer

{% endconfiguration %}

When Gateway is found, All HVAC devices will be configured automatically.
