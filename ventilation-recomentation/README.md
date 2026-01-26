


## 1. Calculate the Absolute Humidity 📊

This one is the most basic sensor. It simply calculates the absolute humidity based on Temperature (°C) and relative Humidity (%). 

Can be used for statistics 📊 or as trigger for automation ⚙️. The Input values are also available as attributes:

```mermaid
flowchart LR
    A@{ shape: brace-r, label: "Temperature (°C)<br>Humidity (%)" }
    B("Absolute Humidity (g/m³)")
    C@{ shape: text, label: "Input Sensor Values" }
    A -- Sensors --> B -. Attributes .- C
```

<details><summary><strong>Setup</strong></summary>

To set up this sensor, you need to do two things:
1. Import this Blueprint  
[![Open your Home Assistant instance and show the blueprint import dialog with a specific blueprint pre-filled.](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fgithub.com%2FFlo-R1der%2FMy_Smart-Home_stuff%2Fblob%2Fmain%2Fventilation-recomentation%2Fabsolute-humidity.yaml)
2. Add one ore multiple sensors to your `configuration.yaml` (or `template.yaml`):

```yaml
template:
  - use_blueprint:
      path: Flo-R1der/absolute-humidity.yaml
      input:
      temperature: #weather-station-or-forecast-or-room-temperature
      relative_humidity: #weather-station-or-forecast-or-room-humidity
  name: Absolute Humidity #outside-or-room-name
  unique_id: absolute_humidity_ #outside-or-room-name
```
Obviously you need to fill the correct entity-id for each input sensor. You can set up one sensor for each area you want to track (outside, living room, bedroom, bath, ...).

<img src="absolute-huminity_example.jpg" width=400px/>

</details>

---

## 2. Calculate the Potential Humidity Improvement

```yaml
template:
  - use_blueprint:
      path: Flo-R1der/potential-humidity-improvement.yaml
      input:
        outside_temperature: #weather-station-or-forecast
        outside_humidity: #weather-station-or-forecast
        inside_temperature: #room-temperature
        inside_humidity: #room-humidity
    name: Potential Humidity Improvement #room-name
    unique_id: potential_humidity_improvement_ #room-name
```


## 3. Ventilation Recommendation

```yaml
template:
  - use_blueprint:
      path: Flo-R1der/ventilation-recommendation.yaml
      input:
        outside_temperature: #weather-station-or-forecast
        outside_humidity: #weather-station-or-forecast
        inside_temperature: #room-temperature
        inside_humidity: #room-humidity
        minimum_improvement_value: 10 #change-if-required
        threshold_room_humidity: 50 #change-if-required
    name: Ventilation Recommendation #room-name
    unique_id: ventilation_recommendation_ #room-name
```
