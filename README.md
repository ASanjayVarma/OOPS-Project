# WeatherAppProject

## Overview

The **WeatherAppProject** is a Java-based application that provides weather information, including the current weather and a multi-day forecast. It retrieves data from the OpenWeather API and allows users to view temperature, humidity, wind speed, and weather descriptions. The application also includes user preferences for units (metric or imperial) and enables notifications for high and low temperature alerts.

### Key Features

- **Current Weather and Forecast**: Fetches real-time weather data and forecasts for a specified number of days.
- **Unit Preferences**: Allows users to switch between metric (°C, m/s) and imperial (°F, mph) units.
- **Notifications**: Provides alerts for high and low temperatures based on user-selected units.
- **Persistence**: Saves user preferences (units and notifications) in a `userPreferences.properties` file, so they persist across sessions.


## Prerequisites

- **Java JDK**: Ensure Java Development Kit (JDK) is installed (version 8 or higher).
- **Gson Library**: The `gson-2.11.0.jar` file should be in the `lib` directory.

## Setup and Execution

### Step 1: Compile the Code

To compile the code, open a terminal or command prompt, navigate to the project directory (`WeatherAppProject`), and run the following command based on your operating system.

#### On Windows

```cmd
javac -cp "lib\gson-2.11.0.jar" -d bin src\*.java
```

#### On Linux/macOS

```bash
javac -cp "lib/gson-2.11.0.jar" -d bin src/*.java
```

This command compiles all `.java` files in the `src` folder and places the generated `.class` files in the `bin` folder.

### Step 2: Run the Application

After compilation, you can run the `WeatherApp` class from the `bin` directory.

#### On Windows

```cmd
java -cp "bin;lib\gson-2.11.0.jar" WeatherApp
```

#### On Linux/macOS

```bash
java -cp "bin:lib/gson-2.11.0.jar" WeatherApp
```

This command launches the application, and you’ll be able to interact with the weather features and set preferences.

### Usage

1. **Current Weather**: Enter the city name to view current weather details.
2. **Weather Forecast**: Specify the city and number of days for forecast data.
3. **Preferences**: Update unit preferences (metric or imperial) and enable/disable notifications for high/low temperature alerts.

## Notes

- The `userPreferences.properties` file in the `resources` folder saves the user’s preferences for units and notifications.
- Make sure to set your API key in the `WeatherAPIManager` class if you replace the code or API credentials.

## Troubleshooting

- If you encounter compilation errors, ensure that the `gson-2.11.0.jar` file is in the `lib` folder and that the `bin` folder exists.
- Make sure to use the appropriate path separators (`;` for Windows, `:` for Linux/macOS) when specifying the classpath.