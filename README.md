# Muar AI Flood Prediction & Alert System

This repository contains the Frontend UI for the Muar AI Flood Prediction System. It is built with HTML, Tailwind CSS (via CDN), Leaflet Maps, and Chart.js. 

The UI is currently running in **Simulation Mode** with a built-in fallback generator so it never crashes while the backend is being developed.

## 🔌 Instructions for the Backend Developer (ARIMA API)

To connect the Python/ARIMA backend, you only need to modify two JavaScript functions in the HTML files. 

### 1. Live Sensor Data (`index.html`)
Find the `fetchStations()` function (around line 380). Replace the demo generator with a `fetch()` call to your live sensor API. 
The UI expects this exact JSON object shape:
```json
{
  "S1": { "level": 2.34, "trend": 0.12, "rain": 4.2 },
  "S2": { "level": 2.62, "trend": 0.05, "rain": 4.2 },
  "S3": { "level": 2.88, "trend": 0.85, "rain": 4.2 }
}