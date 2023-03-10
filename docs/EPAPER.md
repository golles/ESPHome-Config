# Epaper

This is my version of an epaper display showing values from my Home Assistant, originally build by [@maxmacstn](https://github.com/maxmacstn/HA-ePaper-Display).

# Hardware

- Board: DOIT ESP32 DEVKIT V1
- Waveshare 4.2" epaper display

# Wiring

| Board        | Epaper display |
| ------------ | -------------- |
| D25 / GPIO25 | BUSY           |
| D26 / GPIO26 | RST            |
| D27 / GPIO27 | DC             |
| D15 / GPIO15 | CS             |
| D14 / GPIO14 | CLK            |
| D13 / GPIO13 | DIN            |
| GND          | GND            |
| 3V3          | 3V3            |

# Configuration

The device configuration can be found in [epaper.yaml](../epaper.yaml)

# Fonts

The following fonts need to be added inside the `fonts` folder:

- [fonts/Roboto-Medium.ttf](../fonts/Roboto-Medium.ttf)
- [fonts/Roboto-Regular.ttf](../fonts/Roboto-Regular.ttf)
- [fonts/Roboto-Bold.ttf](../fonts/Roboto-Bold.ttf)
- [fonts/materialdesignicons-webfont.ttf](../fonts/materialdesignicons-webfont.ttf)

# Secrets

This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0

epaper_static_ip: 192.168.0.123
epaper_ota_password: ota_password
epaper_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=
```
