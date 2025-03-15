# Home Assistant Temperature Aggregation Blueprint

This blueprint creates a template sensor in Home Assistant that calculates either the average (mean) or median temperature from multiple temperature sensors.

## Features

- Calculate **average (mean)** or **median** temperature
- Works with any sensor that has a temperature device class
- Handles unavailable or unknown sensor readings gracefully
- Includes diagnostic attributes for troubleshooting
- Rounds results to one decimal place for readability

## Installation

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/TheTrickeyOne/home-assistant/main/ha-blueprints/temperature-aggregation/temperature_aggregation.yaml)

1. Click the "Import Blueprint" button above
2. Follow the import wizard in Home Assistant
3. Create a sensor by going to Settings → Blueprints → Temperature Aggregation Sensor → Create Template Sensor

## Configuration Options

| Option | Description |
|--------|-------------|
| Sensor Name | Name for your aggregated temperature sensor |
| Temperature Sensors | Select which temperature sensors to include in the calculation |
| Calculation Type | Choose between Average (Mean) or Median calculation |
| Unit of Measurement | Select Celsius (°C) or Fahrenheit (°F) |

## Attributes

The sensor includes these additional attributes:

- `calculation_type`: Shows which method is being used (average or median)
- `sensors_used`: Number of sensors with valid readings included in calculation
- `total_sensors`: Total number of sensors selected
- `source_sensors`: List of all source sensor entity IDs

## When to Use Median vs Average

- **Average (Mean)**: Best for general use when all sensors are reliable
- **Median**: Better when you have occasional outliers or less reliable sensors

## Example Use Cases

- Create an average temperature for each floor of your home
- Calculate the median temperature of rooms with uneven heating/cooling
- Use as an input for climate control systems

## Support

If you find this blueprint helpful, consider:
- Starring the repository
- Sharing it with other Home Assistant users
- Opening an issue if you encounter problems or have enhancement ideas
