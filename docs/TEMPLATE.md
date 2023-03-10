# DEVICE_NAME

Device description.

# Hardware

- Board: boardname
- Other device

# Wiring

| Board | other device |
| ----- | ------------ |
| GND   | GND          |
| 3V3   | 3V3          |

# Configuration

The device configuration can be found in [device.yaml](../device.yaml)

# Components

No components are required to install.

# Secrets

This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0

device_static_ip: 192.168.0.123
device_ota_password: ota_password
device_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=
```

# Other

Any other information that need to be documented.
