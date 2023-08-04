# Everything presence one 1 / 2

This ultimate smart home sensor supports a 24GHz mmWave Sensor for precise motion tracking as well as a powerful PIR for lightning fast responses. With a Temperature and Humidity sensor for monitoring climate status, Ambient Lighting sensor for smart control of lights, Bluetooth Tracking for wearables and an ESP32 for connectivity.

# Hardware

- Board: everything-presence-one (esp32dev)
- DFRobot SEN0395 mmWave Sensor
- Panasonic Industrial PIR EKMC1603111/3

# Configuration

The device configuration can be found in [epo1.yaml](../epo1.yaml) or [epo2.yaml](../epo2.yaml).

# Components

The following components are required to be installed:

- [Everything Smart Technology Everything Presence One](https://github.com/EverythingSmartHome/everything-presence-one/blob/main/everything-presence-one.yaml)

# Secrets

This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0

epo1_static_ip: 192.168.0.123
epo1_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=
```

# Other

Support the creator and buy your own version of the [Everything presence one](https://shop.everythingsmart.io/en-nl/products/everything-presence-one-kit).
