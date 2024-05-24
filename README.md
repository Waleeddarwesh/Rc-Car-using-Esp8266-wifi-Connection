# NodeMCU Wi-Fi Controlled Car

This project demonstrates how to control a two-motor car using a NodeMCU (ESP8266) via a web interface. The car's movement and speed are controlled by sending HTTP requests to the NodeMCU, which interprets the commands and drives the motors accordingly through an L298N motor driver.

## Features

- **Wi-Fi Access Point**: The NodeMCU acts as a Wi-Fi access point, allowing you to connect directly to it with any Wi-Fi-enabled device.
- **Web Server**: A simple web server runs on the NodeMCU, accepting commands to control the car.
- **Motor Control**: Control the direction and speed of two DC motors using an L298N motor driver.
- **Real-time Command Execution**: Send commands to move the car forward, backward, left, right, and stop. Adjust the speed using predefined levels.

## Hardware Requirements

- NodeMCU (ESP8266)
- L298N Motor Driver
- Two or Four DC Motors
- Power Supply for Motors (e.g., battery pack)
- Connecting Wires
- Car Chassis (optional, for mounting the motors and electronics)

## Pin Configuration

- **ENA**: GPIO14 (D5) - PWM signal to control the speed of the right motor.
- **ENB**: GPIO12 (D6) - PWM signal to control the speed of the left motor.
- **IN1**: GPIO15 (D8) - Direction control for the right motor.
- **IN2**: GPIO13 (D7) - Direction control for the right motor.
- **IN3**: GPIO2 (D4) - Direction control for the left motor.
- **IN4**: GPIO0 (D3) - Direction control for the left motor.

## Software Requirements

- Arduino IDE
- ESP8266 Board Package for Arduino IDE
- Libraries:
  - `ESP8266WiFi`
  - `WiFiClient`
  - `ESP8266WebServer`

## Installation

1. **Install the Arduino IDE** and add the ESP8266 board package using this link : "http://arduino.esp8266.com/stable/package_esp8266com_index.json".
2. **Clone this repository** to your local machine.
3. **Open the project in Arduino IDE** and ensure you have the required libraries installed.
4. **Upload the code** to your NodeMCU.

## Usage

1. **Power the NodeMCU** and the motors.
2. **Connect to the NodeMCU’s Wi-Fi** network (SSID: `NodeMCU Car`).
3. **Open the Application**
4. **Control the car** by sending commands via the App interface.

## Commands

- `F`: Move forward
- `B`: Move backward
- `L`: Turn left
- `R`: Turn right
- `S`: Stop
- `0-9`: Set speed (from 400 to 1023)



