# Presence 1 / 2

This is a configuration for presence detection using a mmWave and PIR sensor. This sensor is very similar to the [Everything Presence One](https://github.com/EverythingSmartHome/everything-presence-one) made by [@EverythingSmartHome](https://github.com/EverythingSmartHome). That great product had limited availability and was sold out before I could buy any.

This version has limited functionality compared to the Everything Presence One device. This uses a different PIR sensor, I had a few `HC-SR501` sensors lying around, also I haven't added a light, temperature, and humidity sensor.

# Hardware

- Board: DOIT ESP32 DEVKIT V1
- DFRobot SEN0395 mmWave Sensor
- HC-SR501 PIR Motion Sensor

# Wiring

| Board        | SEN0395 |
| ------------ | ------- |
| D27 / GPIO27 | IO2     |
| D26 / GPIO26 | IO1     |
| D25 / GPIO25 | RX      |
| D33 / GPIO33 | TX      |
| GND          | G       |
| 5V           | V       |

| Board        | HC-SR501 |
| ------------ | -------- |
| D13 / GPIO13 | OUT      |
| GND          | GND      |
| 5V           | VCC      |

# Configuration

The device configuration can be found in [presence1.yaml](../presence1.yaml) or [presence2.yaml](../presence2.yaml)

# Secrets

This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0

presence1_static_ip: 192.168.0.123
presence1_ota_password: ota_password
presence1_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=
```
