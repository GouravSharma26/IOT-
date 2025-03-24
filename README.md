# 🌤️ IoT-Based Weather Monitoring System

An IoT-based weather monitoring system using **ESP32**, multiple sensors, and the **Blynk IoT** platform. It collects and displays real-time environmental data such as temperature, humidity, air quality, light intensity, and UV radiation on the Blynk mobile app.

---

## 📌 Features
- Real-time monitoring of **Temperature & Humidity** (DHT11)
- Detects **Air Quality** (MQ135 Sensor)
- Measures **Light Intensity** (LDR Sensor)
- Monitors **UV Radiation** (UV Sensor)
- Sends data to **Blynk Cloud** via Wi-Fi
- Real-time data visualization on **Blynk Mobile App**
- Custom alerts on specific thresholds

---

## ⚙️ Hardware Components

| Component            | Description                                         |
|----------------------|-----------------------------------------------------|
| **ESP32 Board**      | Wi-Fi & Bluetooth enabled microcontroller           |
| **DHT11 Sensor**     | Measures temperature and humidity                   |
| **MQ135 Gas Sensor** | Detects air quality (CO2, NH3, Benzene, etc.)       |
| **LDR**              | Detects light intensity                             |
| **UV Sensor**        | Measures UV radiation levels                        |
| **Breadboard & Jumper Wires** | For connecting components                  |
| **Power Supply**     | Powers the ESP32 and sensors                        |

---

## 🔌 Circuit Diagram

> 📷 Add the circuit diagram image file (`circuit_diagram.png`) to your repository and update the link below.

![Circuit Diagram](circuit_diagram.png)

---

## 🛠️ How the System Works

1. Power ON the ESP32 board.
2. ESP32 connects to Wi-Fi with SSID and password.
3. ESP32 authenticates with Blynk Cloud using the Auth Token.
4. Sensor initialization:
    - DHT11 reads temperature and humidity.
    - MQ135 reads air quality.
    - LDR reads light intensity.
    - UV sensor reads UV radiation.
5. Data is sent every 2 seconds to Blynk Virtual Pins (V0 - V4).
6. The Blynk mobile app displays live data through widgets (gauges, graphs, etc.).
7. Users can monitor and set alerts remotely from the app.

---

## 🚀 Getting Started

### Prerequisites
- ESP32 board
- Blynk IoT mobile app (Android/iOS)
- Arduino IDE (installed with ESP32 board support)
- Required Arduino libraries:
  - **Blynk** library
  - **DHT sensor** library

### Blynk Setup
1. Download and install the Blynk IoT app.
2. Create a new project, select **ESP32** as the hardware.
3. Choose Wi-Fi as the connection type.
4. You will receive an **Auth Token** via email.
5. Add widgets:
   - Gauge or Label for Temperature (V0)
   - Gauge or Label for Humidity (V1)
   - Gauge or Label for Air Quality (V2)
   - LED or Label for Light Intensity (V3)
   - Gauge or Label for UV Radiation (V4)

---

## 📱 Mobile App UI (Blynk)

- **V0** → Temperature (°C)
- **V1** → Humidity (%)
- **V2** → Air Quality (ppm)
- **V3** → Light Intensity (On/Off)
- **V4** → UV Radiation (mW/cm²)

---

## ✨ Future Improvements
- Add Rain or Wind Sensors
- Implement SMS/Email alerts
- Solar-powered version for outdoor deployment
- Data logging with Google Sheets or Firebase for historical data analysis

---

## 📚 License
This project is open-source and available under the [MIT License](LICENSE).

