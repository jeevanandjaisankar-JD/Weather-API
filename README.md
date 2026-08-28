# 🌤️ SkyFetch — Weather Dashboard

A simple and responsive weather dashboard built with **HTML, CSS, and JavaScript** that fetches real-time weather information using the **OpenWeatherMap API**.

SkyFetch provides a clean interface for displaying the current weather conditions of a selected city, including temperature, weather description, and an appropriate weather icon.

---

## ✨ Features

* 🌍 Fetches real-time weather data
* 🌡️ Displays current temperature in Celsius
* ☁️ Shows weather condition and description
* 🏙️ Displays the requested city name
* 🌤️ Dynamically loads weather icons
* ⚡ Uses Axios for API requests
* 🎨 Clean gradient-based UI
* ✨ Smooth weather information animation
* 📱 Responsive layout for different screen sizes
* ❌ Handles API/request errors gracefully

---

## 🛠️ Technologies Used

| Technology             | Purpose                                |
| ---------------------- | -------------------------------------- |
| **HTML5**              | Structure and layout                   |
| **CSS3**               | Styling, responsiveness and animations |
| **JavaScript**         | Application logic and API handling     |
| **Axios**              | HTTP requests                          |
| **OpenWeatherMap API** | Real-time weather data                 |

---

## 📂 Project Structure

```text
SkyFetch/
│
├── index.html      # Main webpage
├── style.css       # Styling and animations
├── app.js          # Weather API logic
└── README.md       # Project documentation
```

---

## ⚙️ How It Works

SkyFetch follows a simple API-driven workflow:

```text
User opens the webpage
        ↓
JavaScript calls OpenWeatherMap API
        ↓
Weather data is returned
        ↓
Required information is extracted
        ↓
Weather information is dynamically rendered
        ↓
User sees current weather conditions
```

The application sends a request to the OpenWeatherMap weather endpoint with:

* City name
* API key
* Metric units

The response is then processed to extract:

* City name
* Temperature
* Weather description
* Weather icon

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/skyfetch.git
```

### 2. Navigate to the project

```bash
cd skyfetch
```

### 3. Configure your API key

Create or obtain an API key from OpenWeatherMap.

In `app.js`, configure your API key:

```javascript
const API_KEY = 'YOUR_API_KEY';
```

> ⚠️ **Security Note:** Do not commit a real API key to a public GitHub repository. The current project structure places the key in client-side JavaScript, which means it can be exposed to users. For production applications, use a backend/serverless API layer to protect secrets.

### 4. Run the project

Since this is a frontend project, you can simply open:

```text
index.html
```

in your browser.

For a better development experience, you can also use **VS Code Live Server** or another local development server.

---

## 🔌 API

This project uses the **OpenWeatherMap Current Weather Data API**.

The request follows this structure:

```text
https://api.openweathermap.org/data/2.5/weather
```

Example parameters:

```text
?q=London
&appid=YOUR_API_KEY
&units=metric
```

The application uses the API response to dynamically generate the weather card.

---

## 🧠 Key JavaScript Concepts

This project demonstrates several important frontend development concepts:

### API Requests

Axios is used to communicate with the weather API:

```javascript
axios.get(url)
```

### Promises

The response is handled using `.then()` and `.catch()`:

```javascript
axios.get(url)
    .then(function(response) {
        displayWeather(response.data);
    })
    .catch(function(error) {
        console.error(error);
    });
```

### DOM Manipulation

Weather information is dynamically inserted into the page:

```javascript
document.getElementById('weather-display').innerHTML = weatherHTML;
```

### Template Literals

JavaScript template literals are used to construct the weather UI dynamically:

```javascript
const weatherHTML = `
    <div class="weather-info">
        <h2>${cityName}</h2>
        <div>${temperature}°C</div>
        <p>${description}</p>
    </div>
`;
```

---

## 🎨 UI Design

SkyFetch uses a minimal dashboard-style interface with:

* Purple gradient background
* Glass-like white content card
* Large temperature display
* Weather icon
* Smooth fade-in animation
* Centered responsive layout

The goal is to keep the interface **simple, readable, and visually clean** while focusing on the API integration.

---

## 🔮 Future Improvements

Possible upgrades for future versions:

* 🔎 Add a city search input
* 📍 Detect user's current location
* 🌡️ Display feels-like temperature
* 💧 Show humidity
* 💨 Show wind speed
* 🌅 Display sunrise and sunset
* 📅 Add a multi-day weather forecast
* 🌙 Add dark mode
* 🌍 Add country information
* 📱 Improve mobile-first UI
* 🔐 Move API requests to a backend/serverless function
* 💾 Add recent/search history
* 🎨 Change the background based on weather conditions

---

## 📸 Preview

> Add a screenshot or GIF of your application here.

```text
Coming Soon...
```

---

## 📚 What I Learned

Through this project, I practiced:

* Working with third-party APIs
* Making asynchronous HTTP requests
* Using Axios
* Handling JSON responses
* DOM manipulation
* JavaScript template literals
* Error handling
* Dynamic UI rendering
* Basic responsive web design
* CSS animations

---

## 🤝 Contributing

Contributions, improvements, and suggestions are welcome.

If you find a bug or have an idea for improving SkyFetch, feel free to open an issue or submit a pull request.

---

## 📄 License

This project is open-source and available under the **MIT License**.

---

### 🌤️ SkyFetch

**A simple weather dashboard built while learning API integration and frontend development.**

> *Fetch the weather. Understand the sky. Build something useful.*
