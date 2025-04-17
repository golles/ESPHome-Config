# Everything presence light sensors

Everything Presence Lite is based on the huge success of the Everything Presence One, offering excellent presence detection performance with a more affordable price tag.

Featuring multi-target tracking, support for zones, light level sensing, Bluetooth proxy and support for multiple different mmWave sensors, the Lite offers next level features for a more pocket-friendly point.

# Hardware

- Board: everything-presence-light (esp32dev)
- LD2450 mmWave Sensor

# Configuration

The device configuration can be found in

- [EPL Eettafel](../everything-presence-lite-eettafel.yaml)
- [EPL Keuken](../everything-presence-lite-keuken.yaml)
- [EPL Woonkamer](../everything-presence-lite-woonkamer.yaml)
- [EPL Zolder](../everything-presence-lite-zolder.yaml)

# Components

The following components are required to be installed:

- [Everything Smart Technology Everything Presence light](hhttps://github.com/EverythingSmartHome/everything-presence-lite/blob/main/everything-presence-lite-ha.yaml)

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

Support the creator and buy your own version of the [Everything presence light](https://shop.everythingsmart.io/products/everything-presence-lite).
