# 🌤️ Weather App

A clean, glassmorphic weather app that shows real-time weather conditions — temperature, humidity, wind speed, and current sky conditions — for any city in the world. Built with vanilla HTML, CSS, and JavaScript, powered by the OpenWeatherMap API.

![alt text](<images/image1.png>)
![alt text](<images/image2.png>)

## Features

- 🔍 Search weather by city name
- 🌡️ Live temperature, humidity, and wind speed
- 🎨 Dynamic weather icons that change based on conditions (clear, clouds, rain, drizzle, mist, snow)
- ⚠️ Friendly error state for invalid city names
- 💎 Modern glassmorphic UI with an animated ambient background

## Demo

```
1. Open the app
2. Type a city name (e.g. "London")
3. Click the search button
4. View current weather conditions instantly
```

## Project Structure

```
weather-app/
├── index.html      # Markup / structure
├── style.css        # Styling and animations
├── script.js         # Weather-fetching logic
└── images/
    ├── search.png
    ├── clear.png
    ├── clouds.png
    ├── rain.png
    ├── drizzle.png
    ├── mist.png
    ├── snow.png
    ├── humidity.png
    └── wind.png
```

## Getting Started

### 1. Clone or download this project

```bash
git clone https://github.com/your-username/weather-app.git
cd weather-app
```

### 2. Get a free API key

This app uses the [OpenWeatherMap API](https://openweathermap.org/api).

1. Create a free account at [openweathermap.org](https://home.openweathermap.org/users/sign_up)
2. Go to **My API Keys** in your account dashboard
3. Copy your API key
   > New keys can take a few minutes to a couple of hours to activate.

### 3. Add your API key

Open `script.js` and paste your key into the `apiKey` variable:

```javascript
const apiKey = "YOUR_API_KEY_HERE";
```

### 4. Run the app

No build tools or dependencies needed — just open `index.html` in your browser, or serve it locally:

```bash
# using VS Code
Right-click index.html → "Open with Live Server"

# or using Python
python -m http.server
```

Then visit `http://localhost:8000` (or wherever it's served).

## How It Works

1. The user types a city name and clicks the search button.
2. `checkWeather()` calls the OpenWeatherMap API with the city name and API key.
3. If the city isn't found (`404`), an error message is shown.
4. Otherwise, the response data updates the city name, temperature, humidity, and wind speed on the page.
5. A weather icon is chosen based on the `weather.main` field returned by the API (Clear, Clouds, Rain, Drizzle, Mist, or Snow).

## Tech Stack

- **HTML5** — semantic structure
- **CSS3** — glassmorphism, gradients, and animation
- **JavaScript (ES6+)** — `async/await` and the Fetch API
- **[OpenWeatherMap API](https://openweathermap.org/api)** — live weather data

## Roadmap / Ideas for Improvement

- [ ] Search on `Enter` keypress, not just button click
- [ ] "Use my location" button (Geolocation API)
- [ ] Loading spinner while fetching data
- [ ] 5-day forecast view
- [ ] Remember last-searched city (localStorage)
- [ ] °C / °F unit toggle

## Credits

- Weather data from [OpenWeatherMap](https://openweathermap.org/)
- Icons: custom/sourced weather icon set (`/images`)

## License

This project is open source.