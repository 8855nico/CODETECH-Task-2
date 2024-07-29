**Name:** Nicolas Marandi

**Companey:** CODETECH IT SOLUTION PVT LTD

**ID:** CT08DS5176

**Domain:** INTERNET OF THINGS

**Duration:** JULY 15TH TO AUGUST 15TH,2024

**Mentor:**Muzammil Ahmed


## Overview of Project

### Project:WEATHER MONITORING STATION


### Objective


The goal of this project is to build an IoT-based weather monitoring station that collects data on temperature, humidity, and atmospheric pressure using IoT sensors. The collected data will be displayed in real-time on a dashboard or mobile app.


### Key Components


### Hardware Components:

**Microcontroller/Single-Board Computer:** Raspberry Pi or Arduino

**Sensors:** DHT22 (Temperature and Humidity), BMP180 (Atmospheric Pressure)

**WiFi Module:** ESP8266 for Arduino or built-in WiFi on Raspberry Pi

**Power Supply:** Adequate power supply for the microcontroller and sensors



### Software Components:


**Firmware for Microcontroller:** Code running on Arduino/Raspberry Pi to read sensor data

**Backend Server:** To handle data collection and storage

**Dashboard/Mobile App:** For real-time data visualization


## System Architecture


### Microcontroller Setup:


**Arduino:** Programmed with C++ using the Arduino IDE, equipped with ESP8266 for WiFi connectivity.

**Raspberry Pi:** Programmed using Python, running a web server using Flask to handle HTTP requests.


### Sensor Integration:


Connect the DHT22 sensor to measure temperature and humidity.
Connect the BMP180 sensor to measure atmospheric pressure.


## Data Transmission:


**MQTT:** Lightweight messaging protocol for transmitting sensor data.

**HTTP/REST API:** For sending data from the microcontroller to the backend server.


### User Interface:


**Dashboard:** Built using a web framework like React for real-time data visualization.

**Mobile App:** Built using frameworks like React Native for cross-platform functionality.



## Development Steps


### Hardware Configuration:


#### Arduino with DHT22 and BMP180:


-**Connect the DHT22 and BMP180 sensors to the Arduino.

-**Use the ESP8266 module for WiFi connectivity.


#### Raspberry Pi with DHT22 and BMP180:

-**Connect the DHT22 and BMP180 sensors to the Raspberry Pi GPIO pins.

-**Use the built-in WiFi for connectivity.


## Firmware Development:

-** Arduino
-** Raspberry Pi 

 
## Backend Server Setup:

-** Develop a server using Flask (Python) to handle incoming data from the microcontroller.

_** Store the data in a database (e.g., SQLite, PostgreSQL).


## Dashboard/Mobile App Development:


### React Dashboard 


import React, { useState, useEffect } from 'react';
import axios from 'axios';

function App() {
  const [data, setData] = useState([]);

  useEffect(() => {
    const fetchData = async () => {
      const result = await axios.get('http://your-flask-server/data');
      setData(result.data);
    };
    fetchData();
  }, []);

  return (
    <div>
      <h1>Weather Monitoring Dashboard</h1>
      <table>
        <thead>
          <tr>
            <th>Timestamp</th>
            <th>Temperature (°C)</th>
            <th>Humidity (%)</th>
            <th>Pressure (hPa)</th>
          </tr>
        </thead>
        <tbody>
          {data.map((entry, index) => (
            <tr key={index}>
              <td>{new Date(entry.timestamp).toLocaleString()}</td>
              <td>{entry.temperature}</td>
              <td>{entry.humidity}</td>
              <td>{entry.pressure}</td>
            </tr>
          ))}
        </tbody>
      </table>
    </div>
  );
}

export default App;


## IoT Based Weather Monitoring System Using Arduino 

<img src="https://cdn-0.electronics-project-hub.com/wp-content/uploads/2021/12/IoT-based-weather-moniotring-system_bb-1024x685.jpg">
















## Conclusion

By following these steps, you can develop a comprehensive IoT weather monitoring station that collects and displays real-time weather data on a dashboard or mobile app. This system integrates hardware, firmware, and software components to provide a complete solution for weather monitoring.















































