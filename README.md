# Real-Time-Data-Processing-System-for-Weather-Monitoring.

# Real-Time Data Processing System for Weather Monitoring

## Overview
This project implements a real-time data processing system to monitor weather conditions across major Indian cities. It fetches data from the OpenWeatherMap API, processes it, and provides summarized insights using rollups and aggregates. The system also includes an alerting mechanism for when temperatures exceed a specified threshold.

## Design Choices
1. **Data Source**: We use the OpenWeatherMap API to fetch real-time weather data for six major Indian cities.
2. **Data Storage**: Weather data is stored in memory using a list structure. For a production system, consider using a database for persistent storage.
3. **Rollups and Aggregates**: Daily summaries are calculated based on the accumulated data, including average, maximum, and minimum temperatures, and the dominant weather condition.
4. **Alerting System**: A simple console-based alerting system is implemented to notify when temperatures exceed a predefined threshold.
5. **Scheduling**: The system uses a simple sleep mechanism to fetch data at regular intervals. For more precise scheduling, consider using a dedicated scheduling library.

## Dependencies
This project requires the following Python libraries:
- requests
- json
- datetime
- time

You can install the required libraries using pip:
```
pip install requests
```
(Note: json, datetime, and time are part of Python's standard library)

## Build Instructions
1. Ensure you have Python 3.7 or higher installed on your system.
2. Clone this repository:
   ```
   git clone https://github.com/your-username/weather-monitoring-system.git
   cd weather-monitoring-system
   ```
3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```
4. Open the script and replace `"YOUR_API_KEY"` with your actual OpenWeatherMap API key.

## Usage
To run the weather monitoring system:
```
python weather_monitor.py
```

The script will continuously fetch weather data for the specified cities every 5 minutes. It will print alerts when the temperature exceeds the threshold and display a daily summary when a new day begins.

## Configuration
You can modify the following variables in the script to customize its behavior:
- `API_KEY`: Your OpenWeatherMap API key
- `cities`: List of cities to monitor
- `threshold_temp`: Temperature threshold for alerts (in °C)

## Sample Output
```
ALERT! Mumbai temperature exceeded 35°C
Daily Summary:
Avg Temp: 32.5°C
Max Temp: 37.2°C
Min Temp: 28.1°C
Dominant Weather: Clear
```

## Future Improvements
1. Implement database storage for persistent data and historical analysis.
2. Add more sophisticated alerting mechanisms (e.g., email notifications).
3. Implement data visualization for weather trends.
4. Add error handling and retry mechanisms for API failures.
5. Use a proper scheduling library for more precise data fetching intervals.

## Contributing
Contributions to this project are welcome. Please fork the repository and submit a pull request with your changes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
