# Particulate matter

This is an ESPHome version of the particulate matter sensor from sensor.community. The shopping list (~30$) and build steps can be found on [sensor.community](https://sensor.community/en/sensors/airrohr/).

# Hardware

- Board: ESP8266 NodeMCU V2
- SDS011 Fine dust sensor
- BME280 6-PIN, temperature, humidity and air pressure

# Wiring

| Board      | SDS011 |
| ---------- | ------ |
| D1 / GPIO5 | Pin 1  |
| D2 / GPIO4 | Pin 2  |
| GND        | Pin 3  |
| Unused     | Pin 4  |
| VIN        | Pin 5  |
| Unused     | Pin 6  |
| Unused     | Pin 7  |

| Board      | BME280 |
| ---------- | ------ |
| 3V3        | 3V3    |
| GND        | GND    |
| D3 / GPIO0 | SDA    |
| D4 / GPIO2 | SCL    |

# Configuration

The device configuration can be found in [particulate_matter.yaml](../particulate_matter.yaml)

# Secrets

This configuration requires the following secrets to be defined in your `secrets.yaml`

```yaml
wifi_ssid: wifi_name
wifi_password: wifi_password
ap_password: access_point_password
gateway: 192.168.0.1
subnet: 255.255.255.0
dns1: 8.8.8.8
dns2: 8.8.4.4

particulate_matter_static_ip: 192.168.0.123
particulate_matter_ota_password: ota_password
particulate_matter_encryption_key: abcdefghijklmnopqrstuvwxyz1234567890ABCDEFG=

luftdaten_x_sensor: esp8266-XXXXXXXX
opensensemap_url: https://api.opensensemap.org/boxes/XXXXXXXX/data?luftdaten=1
opensensemap_access_token: XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

# Other

## APIS

- [api.sensor.community](https://github.com/opendata-stuttgart/meta/wiki/EN-APIs)
- [api-rrd.madavi.de](https://github.com/opendata-stuttgart/meta/wiki/EN-APIs)
- [OpenSenseMap](https://docs.opensensemap.org/#api-Measurements-postNewMeasurements)

## Device registration

For sensor.community and madavi you need to register your sensor on [devices.sensor.community](https://devices.sensor.community/). For OpenSenseMap you need to do that on [opensensemap.org](https://opensensemap.org/account).
In OpenSenseMap you can find your `Access Token` under the security options of the specific senseBoxes.

## Miscellaneous

Case being used: https://www.thingiverse.com/thing:4041319

### SDS011 update interval

This sensor has a limited lifespan and shouldn't be activated too often. Setting the `update_interval` to `30min` is recommended. However, this doesn't seem to work out of the box resulting in the sensor being on continuously and pushing readings every second. This can be resolved by setting the value to `0min` first and then to `30min`. For me, I had to repeat this a few times to get this working. More info in this [ESPHome issue](https://github.com/esphome/issues/issues/1144)
