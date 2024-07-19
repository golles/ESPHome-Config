# Watermeter

This ESPHome integration utilizes a proximity sensor to monitor my water meter. The sensor detects the presence of metal, providing a pulse each time a full meter cycle is completed by recognizing the metal piece placed on the meter.

# Hardware

- Board: ESP8266 NodeMCU V2
- NPN proximity sensor (LJ18A3-8-Z/BX-5V)

# Wiring

| Board       | NPN sensor cable |
| ----------- | ---------------- |
| D6 / GPIO12 | Black            |
| GND         | Blue             |
| 5V          | Brown            |

# Configuration

The device configuration can be found in [watermeter.yaml](../watermeter.yaml)

# Secrets

This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0

watermeter_static_ip: 192.168.0.123
watermeter_ota_password: ota_password
watermeter_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=
```

# Proximity sensor

Choosing the right proximity sensor can be tricky; buying the LJ18A3 sensor eliminates the need for additional resistors. Ensure you select the LJ18A3-8-Z/BX-5V variant from AliExpress.com, as it comes with a built-in resistor and operates on 5V, allowing direct power from the ESP.

## Service

This device offers a Home Assistant service for adjusting the meter value without firmware recompilation. For instance, if the `totalWaterUsage` deviates from the actual water meter reading, you can update it directly within Home Assistant.

```yaml
service: esphome.watermeter_set_water_usage
data:
  meter_value: 123,456
```
