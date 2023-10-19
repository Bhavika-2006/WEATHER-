<!DOCTYPE html>
<html>
<head>
  <title>Weather App</title>
</head>
<body>
  <h1>Weather in Your City</h1>
  <div id="weather-info"></div>

  <script>
    // Replace 'YOUR_API_KEY' with your OpenWeatherMap API key
    const apiKey = 'YOUR_API_KEY';

    // Replace 'YOUR_CITY' with the name of the city you want to get the weather for
    const city = 'YOUR_CITY';

    const weatherInfo = document.getElementById('weather-info');

    // Fetch weather data from the API
    fetch(`https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}`)
      .then(response => response.json())
      .then(data => {
        const temperature = data.main.temp;
        const humidity = data.main.humidity;
        const description = data.weather[0].description;

        // Display the weather information
        weatherInfo.innerHTML = `
          <p>Temperature: ${temperature}°C</p>
          <p>Humidity: ${humidity}%</p>
          <p>Description: ${description}</p>
        `;
      })
      .catch(error => {
        console.error('Error fetching weather data:', error);
        weatherInfo.innerHTML = 'Unable to fetch weather data.';
      });
  </script>
</body>
</html>
