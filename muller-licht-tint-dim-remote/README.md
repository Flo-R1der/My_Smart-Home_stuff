# Muller Licht Remote 404049D – Home Assistant Blueprint

This is a Home Assistant automation blueprint to control lights using the **[Müller Licht 404049D dim remote](https://www.zigbee2mqtt.io/devices/404049D.html)** via **[Zigbee2MQTT](https://github.com/Koenkk/zigbee2mqtt)**. The blueprint utilizes MQTT triggers to handle button presses and provides configuration options for common actions like turning lights on/off, adjusting brightness, and cycling scenes.

> [!IMPORTANT]  
> Will not wok with ZHA. Instead **Zigbee2MQTT** is required for this blueprint to work.


## Configuration

To use this blueprint:

1. Ensure Zigbee2MQTT is set up and publishing MQTT messages. You may check the device logbook for incoming actions in Home Assistant.
2. Note the MQTT topic for the device (e.g., `zigbee2mqtt/muller_licht_remote`). <br>
   ![MQTT info location](mqtt-info_location.png)
3. Import the blueprint to your Home Assistant instance: <br>
   [![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=FIXME)
4. Create a new automation using the blueprint
   - Fill in the MQTT topic and assign actions to each button press

<br>

---

## Like My Work?
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I3I4160K4Y)
