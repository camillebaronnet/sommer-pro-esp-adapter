# Sommer Pro+ to D1 Mini Adapter (ESP8266)

*todo...*

# Hardware

*todo...*

# Software


*todo...*

## ESPHome configuration

```yaml
# [...]
binary_sensor:
  - platform: gpio
    pin: GPIO16
    name: "Door status"
    device_class: "door"

switch:
  - platform: gpio
    pin: GPIO0
    id: open_door
    name: "Open door"
    icon: "mdi:gate"
    on_turn_on:
    - delay: 1000ms
    - switch.turn_off: open_door

  - platform: gpio
    pin: GPIO2
    id: close_door
    name: "Close door"
    icon: "mdi:gate"
    on_turn_on:
    - delay: 1000ms
    - switch.turn_off: close_door
```
