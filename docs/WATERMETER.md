# Watermeter

Device description.

# Hardware

- Board: Wemos D1 mini
- NPN proximity sensor

# Wiring

| Board      | NPN sensor cable |
| ---------- | ---------------- |
| D2 / GPIO4 | Black            |
| GND        | Blue             |
| 5V         | Brown            |

Add a 10K resistor between D2 and 5V.

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

# Other

## Service

This device exposes a service to Home Assistant which let you set or update the meter value from within Home Assistant without recompiling this firmware. For example when the `totalWaterUsage` value is no longer in sync with the water meter.

```yaml
service: esphome.watermeter_set_water_usage
data:
  meter_value: 123.456
```
