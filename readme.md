# Home assistant setup with Zigbee running in Docker
This repository holds a basic Home Assistant setup based on Docker Compose, with the following services:

* Home Assistant (see https://www.home-assistant.io/)
* Zigbee2mqtt (see https://www.zigbee2mqtt.io/)
* Mosquitto (see https://mosquitto.org/)
* ESPHome (see https://esphome.io/)

> [!IMPORTANT]
> Docker-For-Mac does not support mounting USB devices into Docker containers, this is caused by the Virtualization layer within MacOS.

## Usage
* Run `docker compose up`
* Connect to http://127.0.0.1:8123/

### ESPHome
* After starting connect to http://127.0.0.1:6052/
* Click on `secrets` in the right top corner and add the following yaml data:

```yaml
wifi_ssid: "<your wifi SSID>"
wifi_password: "<your wifi password>"
home_assistant_encryption_key: "<auto generated encryption key by esphome>"
ota_password: "<password used to update your device over wifi>"
```
