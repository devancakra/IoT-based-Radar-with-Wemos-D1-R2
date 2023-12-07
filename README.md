[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
![IoT](https://img.shields.io/badge/Project-Internet%20of%20Things-blue?logo=github&color=ef4e4e)
![ArduinoIDE_Processing_MQTTExplorer](https://img.shields.io/badge/Tools-Arduino%20IDE%2C%20Processing%2C%20MQTT%20Explorer-light.svg?style=flat&logo=arduino&logoColor=white&color=ff9f42)
![Java](https://img.shields.io/badge/-Java-light.svg?style=flat&logo=openjdk&logoColor=white&color=fee863)
![C++](https://img.shields.io/badge/c++-light.svg?&style=flat&logo=c%2B%2B&logoColor=white&color=b3fe63)

# IoT-based-Radar-with-Wemos-D1-R2
<strong>UCI Coursera Final Project 2023</strong><br>
This project is closely related to defense technology, where this tool is used to detect the presence or absence of objects around a predetermined area. This defense system is run with the MQTT protocol. In addition, this system also provides a user interface to make monitoring easier.

<br><br>

## Features / Framework / Tools
| Media | Description |
| --- | --- |
| Board Development | Wemos D1 R2 |
| IoT Platform | mosquitto |
| Tools | Arduino IDE, Processing, MQTT Explorer |
| Arduino Library | ESP8266WiFi, Servo, PubSubClient, ArduinoJson |
| Actuators | Servo Motor 180° |
| Sensor | Ultrasonic Sensor (HC-SR04) |
| Other Components | Jumper cable & USB cable type A/B |

<br><br>

## Download & Install
1. Arduino IDE
   ```
   https://www.arduino.cc/en/software
   ```
   
2. Processing
   ```
   https://processing.org/download
   ```

3. MQTT Explorer
   ```
   https://mqtt-explorer.com/
   ```

<br><br>

## System Flow Schematic
When an object is in the sensor detection area, the sensor will respond by sending publish data to the IoT platform (mosquitto) and then sending back in the form of subscribe data to be displayed on the serial monitor. As for the graph, users can also see a significant color difference in the detection area. If no object is found, the sensor and actuator will always be on standby.

<br><br>

## Project Requirements
<table>
<tr>
<th width="420">Block Diagram</th>
<th width="420">Pictorial Diagram</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/71ed3ef5-8787-44fc-8c25-9d072c631e1a" alt="Block-Diagram"></td>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/183c9c9e-eb51-4b88-945b-d30ddc97833a" alt="Pictorial-Diagram"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Wiring</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/e49d2460-5653-4fe2-8c6d-0668844efd1f" alt="Wiring"></td>
</tr>
</table>

<br><br>
