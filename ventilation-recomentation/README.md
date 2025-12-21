





## 1. Calculate the Absolute Humidity

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
