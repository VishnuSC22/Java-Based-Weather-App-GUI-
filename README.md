**AppLauncher.java**
The AppLauncher class serves as the entry point for the Weather App GUI. It is designed to initialize and display the graphical user interface (GUI) of the application while adhering to best practices for Java Swing applications.

The AppLauncher class:
->Initializes the application by invoking the GUI on the correct thread (EDT).
->Acts as a connector between the backend logic (WeatherApp class) and the GUI (WeatherAppGui class).
->Ensures modularity by keeping the GUI and backend functionalities separate.


**WeatherApp.java**
The WeatherApp class handles the core logic for retrieving and processing weather data for a specified location.It communicates with external APIs to fetch geographic and weather data, processes the response, and formats it for use by the GUI.

The WeatherApp class:
i>Weather Data Retrieval
->Fetches weather information (temperature, humidity, wind speed, and weather condition) for a specified location using the Open-Meteo Weather API.
->Extracts real-time hourly data and processes it to present the current weather.

ii>Location Data Retrieval
->Uses the Open-Meteo Geocoding API to retrieve latitude and longitude coordinates for a given location name.

iii>Utility Methods
->Formats the current time to match the API's hourly time format.
->Converts raw weather codes from the API into human-readable weather descriptions.


**WeatherAppGui.java**
The WeatherAppGui class provides the graphical user interface (GUI) for the Weather App. It allows users to search for the current weather of a specified location and displays the results visually.

i>User-Friendly Design
->Modern GUI with weather visuals (icons for conditions, humidity, and wind speed).
->Centralized layout for an aesthetically pleasing user experience.

ii>Real-Time Weather Display
->Users can search for weather information by entering a location in the search bar.
->Displays real-time weather details including:
     Temperature
     Weather condition (e.g., Clear, Cloudy, Rain)
     Humidity percentage
     Wind speed
     
iii>Interactive Components
->Search button with hand cursor to improve usability.
->Dynamically updates all displayed data based on user input.
