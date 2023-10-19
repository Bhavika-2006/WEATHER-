<!DOCTYPE html>
<html>
<head>
 Mission and Vision 
</head>
<body>
  <h1>Weather in Your City</h1>
  <div id="weather-info"></div>

<body>
  Welcome to our project! 🚀 We're passionate about data and algorithms. Our mission is to create a robust system for storing and managing information related to mathematics, computer science, and events. Our algorithms ensure efficient data storage, retrieval, and organization, making this repository a valuable resource for enthusiasts and learners in these domains. From mathematical theorems to coding solutions and event details, our platform provides a seamless experience. Join us in our journey to explore, store, and analyze knowledge in the world of mathematics, computer science, and events. Let's collaboratively build a repository that empowers everyone with access to structured and comprehensive information.
 
</body>
this is the code i pasted on text editor
<br>file:///Users/bhavikamithrani/Desktop/weather.html<br>
<html>
<head>
  <title>Weather App</title>
</head>
<body>
  <h1>Weather in Your City</h1>
  <div id="weather-info"></div>

  <script>
    // Replace 'YOUR_API_KEY' with your OpenWeatherMap API key
    const apiKey = 'ef518f509c3d1105a83061baf3bcfb49';

    // Replace 'YOUR_CITY' with the name of the city for which you want to get weather information
    const city = 'NEW DELHI';

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
eather.html…]()



</body>
</html>
