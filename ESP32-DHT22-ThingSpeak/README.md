# ESP32 – DHT22 IoT Monitoring System with ThingSpeak MQTT

## 📌 Project Overview

This project implements an IoT-based environmental monitoring system using an ESP32 microcontroller and a DHT22 temperature and humidity sensor.

The system collects environmental data, transmits it to the ThingSpeak IoT platform using MQTT communication, and displays measurements through a web dashboard.

It also supports remote LED control through the dashboard using ThingSpeak and MQTT.

## 🎯 Project Objectives

- Measure temperature and humidity using a DHT22 sensor.
- Collect and process sensor readings using an ESP32.
- Establish wireless communication through Wi-Fi.
- Transmit sensor measurements to ThingSpeak using MQTT.
- Visualize environmental data through a web dashboard.
- Control an LED remotely using MQTT subscriptions.

## 🏗️ System Architecture

The project consists of four main components:

1. **ESP32:** Main microcontroller responsible for collecting and transmitting sensor data.
2. **DHT22:** Sensor used to measure temperature and relative humidity.
3. **ThingSpeak:** Cloud IoT platform used to store and manage sensor measurements.
4. **Web Dashboard:** Interface for displaying sensor readings and controlling the LED.

### Communication Flow

```text
       DHT22 Sensor
             |
             v
           ESP32
             |
           Wi-Fi
             |
             v
      ThingSpeak MQTT
             |
       +-----+------+
       |            |
       v            v
  Cloud Data    LED Commands
       |            ^
       v            |
  Web Dashboard ----+
```

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| ESP32 | Microcontroller |
| DHT22 | Temperature and humidity sensing |
| Arduino Framework | Embedded programming |
| C++ | Firmware development |
| Wi-Fi | Wireless connectivity |
| MQTT | Communication protocol |
| ThingSpeak | IoT cloud platform |
| HTML / CSS / JavaScript | Web dashboard |
| VS Code / PlatformIO | Development environment |
| Wokwi | ESP32 simulation |

## 📊 ThingSpeak Channel Configuration

The project uses the following channel fields:

| Field | Description |
|---|---|
| Field 1 | Humidity (%) |
| Field 2 | Temperature (°C) |
| Field 3 | LED control command (0 or 1) |

### MQTT Configuration

- Broker: `mqtt3.thingspeak.com`
- Port: `1883`
- Publishing topic: `channels/3591335/publish`
- Subscription topic: `channels/3591335/subscribe/fields/field3`
- Data publishing interval: 20 seconds

## 🌐 Web Dashboard

The web dashboard provides:

- Temperature monitoring.
- Humidity monitoring.
- Graphical gauges for both measurements.
- LED ON/OFF control buttons.
- LED status indicator.
- Automatic data refresh every 15 seconds.

The dashboard can be hosted using GitHub Pages.

## 📁 Project Structure

```text
ESP32-DHT22-ThingSpeak/
│
├── index.html
└── README.md
```

Adjust this tree if your repository uses a different structure.

## ⚙️ Installation and Configuration

### 1. Clone the Repository

```bash
git clone https://github.com/kharmachiS/ESP32-DHT22-ThingSpeak.git
```

### 2. Open the Project

Open the project folder in Visual Studio Code with PlatformIO installed.

### 3. Install Dependencies

The required libraries are:

- PubSubClient
- DHTesp

PlatformIO can install them automatically through `platformio.ini`.

### 4. Configure Wi-Fi and MQTT

Update the firmware with your Wi-Fi and ThingSpeak MQTT credentials.

**Security:** Never publish MQTT passwords, private API keys, or other credentials in a public repository. If a credential has already been committed, rotate it; deleting it from the latest version alone does not remove it from Git history.

### 5. Build and Run

Build the firmware using PlatformIO and upload it to the ESP32, or run it through the Wokwi simulator.

## 🚀 Deployment

The web dashboard can be deployed using GitHub Pages.

After enabling GitHub Pages for the repository, the expected URL is:

https://kharmachiS.github.io/ESP32-DHT22-ThingSpeak/

## 👩‍💻 Author

**Soumaya Kharmachi**

IoT Project – ESP32, DHT22 and ThingSpeak MQTT

---

*This project demonstrates the integration of embedded systems, wireless communication, cloud-based IoT services, and web technologies in an environmental monitoring application.*
