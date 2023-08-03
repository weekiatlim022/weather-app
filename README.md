![Weather-App Screenshot](/public/screenshot.png)
# Weather App in ReactJS

This is a weather app developed using ReactJS that allows users to search for cities and view the current weather as well as a 7-day forecast.

**Live demo**: https://weather-with-cities.netlify.app/

## Description

### App.js

The entry point of the application that handles state management and data fetching. It contains the main container and integrates the Search component for city search and the CurrentWeather component for displaying the current weather. Additionally, it utilizes the Forecast component to show the 7-day weather forecast.

### Search.js

The Search component provides a search input box where users can enter the name of a city. It uses the `AsyncPaginate` from `react-select-async-paginate` to asynchronously fetch city suggestions from the server. Upon selecting a city, it triggers a search change event and passes the city's latitude and longitude to the parent component (App.js) for weather data fetching.

### CurrentWeather.js

The CurrentWeather component displays the current weather information for the selected city. It shows the city name, weather description, temperature, and other details such as feels like temperature, wind speed, humidity, and pressure.

### Forecast.js

The Forecast component presents a 7-day weather forecast in an accordion-style format. It displays the weather icon, weather description, minimum and maximum temperatures for each day. When users click on a particular day, it expands to show additional details like pressure, humidity, clouds, wind speed, sea level, and feels like temperature.

## How to Use

1. Open the app in your web browser.
2. In the search input box, type the name of the city you want to search for.
3. As you type, the app will suggest matching cities with a population of at least one million.
4. Select your desired city from the suggestions.
5. The current weather for the selected city will be displayed, including temperature, weather description, and other details.
6. Scroll down to see the 7-day forecast.
7. Click on a specific day to view additional weather details for that day.

## Technologies Used

- ReactJS for building the user interface and managing state.
- OpenWeather API: https://openweathermap.org/
- GeoDB Cities API: https://rapidapi.com/wirefreethought/api/geodb-cities/
- `react-select-async-paginate` for handling asynchronous city search suggestions.
- `react-accessible-accordion` for creating an accessible accordion-style component to display the 7-day weather forecast.
- CSS for styling the app and making it visually appealing.

Note: To run this app, you need to provide your own weather API key, which should be set in the `WEATHER_API_KEY` constant in the `api.js` file.