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
![IOTD](https://github.com/user-attachments/assets/8cf01c4a-1f1b-44c0-803f-4ba0339a124e)
![IMG_4153](https://github.com/user-attachments/assets/3afcce2d-c2e4-43a1-afd3-51cff47691b8)
![IMG_4154](https://github.com/user-attachments/assets/6846f702-bdcc-453a-84aa-5dea9e7f11e9)

https://github.com/user-attachments/assets/fe3df28d-7841-4d9c-a58e-32409727b064



---

## Wiring Diagram ONLY IF YOUR ESP8266 DOES NOT HAVE A USB PORT

| ESP8266 Pin | Description         |
|-------------|---------------------|
| VCC         | Connect to 3.3V    |
| GND         | Connect to Ground  |
| D4          | Connect to LED or Debug Pin |

---

## Example Configuration

Ensure these lines are updated in the code:
```cpp
ssid = "YourWiFiSSID";
password = "YourWiFiPassword";
weatherApiKey = "YourOpenWeatherMapAPIKey";
stockApiKey = "YourAlphaVantageAPIKey";
octoPrintApiKey = "YourOctoPrintAPIKey";
octoPrintUrl = "http://YourOctoPrintIP:Port/api/job";
