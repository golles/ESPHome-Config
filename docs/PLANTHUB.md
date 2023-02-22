# Plant hub
This device is a bluetooth proxy for Xiaomi Mijia BLE sensors (HHCCJCY01). In the past this device was using the `xiaomi_hhccjcy01` platform combined with `esp32_ble_tracker`, hence the name Plant hub.

# Hardware
 - Board: DOIT ESP32 DEVKIT V1

# Configuration
The device configuration can be found in [planthub.yaml](../planthub.yaml)

# Secrets
This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0

planthub_static_ip: 192.168.0.123
planthub_ota_password: ota_password
planthub_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=
```
