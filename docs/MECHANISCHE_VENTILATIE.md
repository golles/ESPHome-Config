# Mechanische ventilatie
This is a controller that controls the `Zehnder Stork Comfofan S Hygro` mechanical ventilation.

# Hardware
 - Board: DOIT ESP32 DEVKIT V1
 - NRF905 transceiver module

# Wiring
| Board | NRF905 |
|--|--|
| D15 / GPIO15 | CS |
| D32 / GPIO32 | AM |
| D33 / GPIO33 | CD |
| D27 / GPIO27 | CE |
| D35 / GPIO35 | DR |
| D26 / GPIO26 | PWR |
| D25 / GPIO25 | TXEN |
| GND | GND |
| 3V3 | VCC |

# Configuration
The device configuration can be found in [mechanische_ventilatie.yaml](../mechanische_ventilatie.yaml)

# Components
The following components are required to be installed:
 - [nRF905 Wireless Transceiver component](../components/nrf905/)
 - [nRF905 Zehnder component](../components/zehnder/)

# Secrets
This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0

mechanische_ventilatie_static_ip: 192.168.0.123
mechanische_ventilatie_ota_password: ota_password
mechanische_ventilatie_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=
```
