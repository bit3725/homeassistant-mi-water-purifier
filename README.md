# homeassistant-mi-water-purifier
XiaoMi Water Purifier component for Home Assistant.

![Screenshot1](https://raw.githubusercontent.com/bit3725/homeassistant-mi-water-purifier/master/images/screenshot1.png)
![Screenshot2](https://raw.githubusercontent.com/bit3725/homeassistant-mi-water-purifier/master/images/screenshot2.png)
![Screenshot3](https://raw.githubusercontent.com/bit3725/homeassistant-mi-water-purifier/master/images/screenshot3.png)

## Installation
1. Copy *custom_components/sensor/mi_water_purifier.py* to **.homeassistant/custom_components/sensor**.
2. Get the IP of your sensor.
3. Follow [Retrieving the Access Token](https://home-assistant.io/components/vacuum.xiaomi_miio/#retrieving-the-access-token) guide to get the token of your sensor

## Configuration
```yaml
sensor:
  - platform: mi_water_purifier
    host: YOUR_SENSOR_IP
    token: YOUR_SENSOR_TOKEN
    name: YOUT_SENSOR_NAME
```

```yaml
group:
  - xiaomi_water_purifier:
    name: Xiaomi Water Purifier
    icon: mdi:water
    entities:
      - sensor.tap_water
      - sensor.filtered_water
      - sensor.pp_cotton_filter
      - sensor.front_active_carbon_filter
      - sensor.ro_filter
      - sensor.rear_active_carbon_filter
```
