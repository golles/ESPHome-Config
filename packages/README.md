# ESPHome packages

This folder contains packages that can be shared by multiple ESPHome devices.

### `device_base.yaml`
This file contains all the standard components all my devices should have, `wifi`, `ota`, `api`, `captive_portal`, `logger`, `time`, `binary_sensor`, `button`, `text_sensor`, and some `sensor`.
A new device can be created with the following template:
```yaml
substitutions:
  devicename: newdevice
  upper_devicename: NewDevice
  static_ip: !secret newdevice_static_ip
  wifi_ap_password: !secret ap_password
  api_password: !secret newdevice_api_password
  ota_password: !secret newdevice_ota_password
    
packages:
  device_base: !include packages/device_base.yaml

esphome:
  name: $devicename
  platform: ESP32
  board: esp32doit-devkit-v1
```

### `secrets.yaml`
Because ESPHome isn't able to read the secrets from a parent folder, this file is needed to pass secrets on to files in this folder. The file should include the parent `secrets.yaml` and not contain any secrets or passwords.
