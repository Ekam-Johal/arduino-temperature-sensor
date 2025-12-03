
<p align="center">
  <img src="https://github.com/user-attachments/assets/a2c15af9-ab77-4e63-9235-960fbb4b5f17" width="45%" style="border-radius:8px; margin-right:10px;">
  <img src="https://github.com/user-attachments/assets/9ebe3cce-17f4-4a39-8421-96054ca80baa" width="45%" style="border-radius:8px;">
</p>

# Arduino DHT11 LCD Temperature Monitor

Simple Arduino project that reads **temperature and humidity** from a DHT11 sensor and displays the values on a **16x2 I2C LCD**.  

This is one of my first embedded projects and is part of my electronics/Arduino learning journey.
This project was built as part of my self-directed learning in electronics and embedded systems during my first year of engineering.

---

## Features

- Reads temperature (°C) and humidity (%) using a **DHT11** sensor  
- Displays live readings on a **16x2 I2C LCD**  
- Updates every 2 seconds  
- Basic error handling if the sensor reading fails

<p align="center">
  <img src="https://github.com/user-attachments/assets/4d7f7638-fbfa-41dc-b3d6-9b41c795106c" width="45%">
  <img src="https://github.com/user-attachments/assets/44d1a2fb-d63b-4624-ab30-b5d1ac85f983" width="45%">
</p>

---

## Hardware

- Arduino Uno
- DHT11 temperature & humidity sensor module
- 16x2 LCD with I2C backpack (HW-61)
- Jumper wires
- USB cable

---

## Wiring

### DHT11 → Arduino

| DHT11 Pin | Arduino Pin |
|----------|-------------|
| `+` (VCC) | 5V |
| `-` (GND) | GND |
| `S` (Signal) | D2 |

### I2C LCD → Arduino

| LCD Pin | Arduino Pin |
|--------|-------------|
| `GND` | GND |
| `VCC` | 5V |
| `SDA` | A4 |
| `SCL` | A5 |

> If the LCD is powered but you see no text, gently adjust the blue contrast potentiometer on the I2C board.

---

## Arduino Libraries Used

Install these from **Library Manager**:

- `LiquidCrystal I2C` by Frank de Brabander
- `DHT sensor library` by Adafruit
- `Adafruit Unified Sensor`

---

## How to Run

1. Wire the Arduino, DHT11, and LCD as shown above.
2. Open `TemperatureMonitor/TemperatureMonitor.ino` in the Arduino IDE.
3. Select **Board:** `Arduino Uno` and the correct **Port`.
4. Click **Upload**.
5. The LCD will first show `Temp Monitor / Starting...` and then live temperature and humidity values.

---

## Skills Demonstrated

- Basic embedded C/C++ programming on Arduino
- Reading digital sensors (DHT11) and handling errors
- I2C communication with a 16x2 LCD display
- Interpreting wiring diagrams and building circuits on a breadboard
- Writing clear technical documentation for a hardware project

---

## What I Learned

- How to read a digital temperature & humidity sensor (DHT11)
- How I2C works and how to connect an I2C LCD to the Arduino
- Using external libraries in Arduino projects
- Organising a small embedded project and documenting it for GitHub

---

## Future Improvements

- Add LEDs or a buzzer to signal high temperature
- Log data to the Serial Plotter or an SD card
- Use a more accurate sensor (e.g. DHT22 or BME280)
