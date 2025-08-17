# 🎛️ Paulmann 4 Button smart Switch – Home Assistant Blueprint

This is a Home Assistant automation blueprint to control entities using a **Paulmann 4 button Remote** like the **[Paulmann 501.34](https://www.zigbee2mqtt.io/devices/501.34.html)** via **[Zigbee2MQTT](https://github.com/Koenkk/zigbee2mqtt)**. The blueprint uses the MQTT device triggers to detect button presses and provides action-selector for each available button pressed event.

> [!IMPORTANT]  
> Will not wok with ZHA. Instead **Zigbee2MQTT** is required for this blueprint to work.


## 🛠️ Configuration

This one is pretty easy:
1. Import the blueprint to your Home Assistant instance: <br>
   [![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://github.com/Flo-R1der/My_Smart-Home_stuff/blob/main/Paulmann-501.34/Paulmann-501.34.yaml)
2. Select the **Action entity** of the device
3. **Define actions** you want to bind to those keys.

<br>

---

## ❤️ Like My Work?
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/I3I4160K4Y)
