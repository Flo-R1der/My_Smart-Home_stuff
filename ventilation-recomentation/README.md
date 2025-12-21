





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

