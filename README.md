# ESP8266 IoT Dashboard

This project uses an ESP8266 to create a real-time IoT dashboard. The dashboard displays live weather updates, stock prices, 3D printer status, and a clothing recommendation based on current weather. The project is accessible through a modern web interface, designed for seamless use on any device.

---

## Features

### Real-Time Dashboard
- **Weather Information:**
  - Fetches live weather data from OpenWeatherMap.
  - Displays current weather, temperature, and clothing recommendations.
  
- **Stock Tracker:**
  - Monitors real-time stock prices for AAPL, TSLA, and GOOG using Alpha Vantage API.
  - Automatically updates every 60 seconds.

- **3D Printer Monitor:**
  - Integrates with OctoPrint to show print job progress.
  - Displays job name, print percentage, and a graphical progress bar.

- **Time and Date:**
  - Real-time local time for Toronto with NTP synchronization.
  - Adjusts for daylight savings automatically.

- **Web Interface:**
  - Clean and responsive web interface.
  - Live updates for all features without requiring manual refresh.

---

## Accessing the Web Interface

1. Open the **Serial Monitor** in Arduino IDE after uploading the code.
2. Copy the ESP8266's IP address displayed in the monitor.
3. Paste the IP into any web browser on the same WiFi network.
4. Enjoy the live IoT dashboard!

---

## Web Interface

### Live Features
1. **Current Time:** Displays real-time local time for Toronto, refreshed every second.
2. **Weather:** Shows live weather conditions, temperature, and clothing recommendations.
3. **Stocks:** Real-time prices for AAPL, TSLA, and GOOG, updated every minute.
4. **3D Printer Status:** Displays job name, progress, and a graphical progress bar for ongoing prints.

### Preview
![Dashboard Preview](https://via.placeholder.com/800x400?text=ESP8266+IoT+Dashboard)

---

## Wiring Diagram

| ESP8266 Pin | Description         |
|-------------|---------------------|
| VCC         | Connect to 3.3V    |
| GND         | Connect to Ground  |
| D4          | Connect to LED or Debug Pin (if required) |

---

## Example Configuration

Ensure these lines are updated in the code:
```cpp
const char* ssid = "YourWiFiSSID";
const char* password = "YourWiFiPassword";
const String weatherApiKey = "YourOpenWeatherMapAPIKey";
const String stockApiKey = "YourAlphaVantageAPIKey";
const String octoPrintApiKey = "YourOctoPrintAPIKey";
const String octoPrintUrl = "http://YourOctoPrintIP:Port/api/job";
