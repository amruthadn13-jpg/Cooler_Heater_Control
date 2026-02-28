# Cooler_Heater_Control
**🌡️ ESP32 Based Automatic Cooler & Heater Control System (Wokwi)**

This project demonstrates an automatic temperature-based control system using an ESP32 microcontroller.
The system turns ON a cooler when the temperature is high and ON a heater when the temperature is low.
The entire project is simulated using Wokwi.

The ESP32 used in this project is developed by
Espressif Systems.

**📌 Project Description**

This project reads temperature data from a DHT22 sensor and automatically controls two devices:

Cooler (represented using a servo motor)

Heater (represented using a relay module)

The ESP32 continuously monitors the temperature and decides which device should be turned ON or OFF based on predefined temperature limits.

This project is useful for learning:

sensor interfacing

decision-based control logic

basic automation using microcontrollers

**🧰 Components Used (Wokwi)**

ESP32 Development Board

DHT22 Temperature & Humidity Sensor

Servo Motor (used as cooler representation)

Relay Module (used as heater control)

Connecting wires

**⚙️ Working Principle**

The ESP32 reads temperature and humidity from the DHT22 sensor.

The temperature value is compared with two limits:

High temperature limit

Low temperature limit

Based on the temperature:

If temperature is higher than the high limit → cooler turns ON and heater turns OFF.

If temperature is lower than the low limit → heater turns ON and cooler turns OFF.

If temperature is within the normal range → both devices remain OFF.

The ON and OFF states are displayed on the Serial Monitor.

**🔁 Control Logic**
Condition	Cooler	Heater
Temperature > 25°C	ON	OFF
Temperature < 20°C	OFF	ON
20°C – 25°C	OFF	OFF
🔌 Pin Connections
DHT22 Sensor
DHT22 Pin	ESP32 Pin
VCC	3.3V
DATA	GPIO 12
GND	GND
Servo Motor (Cooler)
Servo Wire	ESP32 Pin
Signal	GPIO 19
VCC	5V
GND	GND
Relay Module (Heater)
Relay Pin	ESP32 Pin
IN	GPIO 18
VCC	5V
GND	GND
**🖥️ Serial Monitor Output**
The Serial Monitor shows:

current temperature

current humidity

cooler and heater status

Example:

Temperature: 24.00 °C , Humidity: 40.00 %
Status: COOLER ON , HEATER OFF
**🎯 Applications**

Automatic room temperature controller

Smart home temperature management

Basic thermostat system

Learning project for embedded systems and IoT

**👩‍💻 Author**

Amrutha D N

**📝 Notes**

This project is fully simulated in Wokwi and does not require physical hardware.

In real hardware:

the cooler would be a fan or air-cooler

the heater would be a real heating device controlled through a relay or contactor

This project focuses on understanding the control logic and sensor-based automation.
