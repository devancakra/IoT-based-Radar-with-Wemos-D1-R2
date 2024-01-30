[![Open Source Love](https://badges.frapsoft.com/os/v1/open-source.svg?style=flat)](https://github.com/ellerbrock/open-source-badges/)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?logo=github&color=%23F7DF1E)](https://opensource.org/licenses/MIT)
![GitHub last commit](https://img.shields.io/github/last-commit/devancakra/IoT-based-Radar-with-Wemos-D1-R2)
![IoT](https://img.shields.io/badge/Project-Internet%20of%20Things-blue?logo=arduino&color=%23F7DF1E)

# IoT-based-Radar-with-Wemos-D1-R2
<strong>UCI Coursera Final Project 2023</strong><br><br>
This project is closely related to defense technology, where this tool is used to detect the presence or absence of objects around a predetermined area. This defense system is run with the MQTT protocol. In addition, this system also provides a user interface to make monitoring easier.

<br><br>

## Project Requirements
| Part | Description |
| --- | --- |
| Development Board | Wemos D1 R2 |
| Code Editor | Arduino IDE & Processing |
| Driver | USB-Serial CH340 |
| IoT Platform | mosquitto |
| IoT Appliances | MQTT Explorer |
| IoT Protocol | MQTT |
| IoT Architecture | 3 Layer |
| Programming Language | C/C++ and Python |
| Arduino Library | ESP8266WiFi, Servo, PubSubClient, ArduinoJson |
| Actuators | Servo Motor SG90 180° (x1) |
| Sensor | HC-SR04: Ultrasonic Sensor (x1) |
| Other Components | Micro USB cable - USB type A (x1), Jumper cable (1 set), Screws (1 set), and HC-SR04 Mounting Bracket (x1) |

<br><br>

## Download & Install
1. Arduino IDE
   
   ```
   https://www.arduino.cc/en/software
   ```
   <br>
   
2. Processing
   
   ```
   https://processing.org/download
   ```
   <br>

3. MQTT Explorer
   
   ```
   https://mqtt-explorer.com/
   ```
   <br>
   
4. USB-Serial CH340

   ```
   https://bit.ly/CH340_Driver
   ```
   
<br><br>

## System Flow Schematic
When an object is in the sensor detection area, the sensor will respond by sending publish data to the IoT platform (mosquitto) and then sending back in the form of subscribe data to be displayed on the serial monitor. As for the graph, users can also see a significant color difference in the detection area. If no object is found, the sensor and actuator will always be on standby.

<br><br>

## Project Designs
<table>
<tr>
<th width="420">Block Diagram</th>
<th width="420">Pictorial Diagram</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/b9890292-0b28-4a78-8f9d-39df8f806177" alt="Block-Diagram"></td>
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

## Arduino IDE Setup
1. Open the ``` Arduino IDE ``` first, then open the Wemos D1 R2 Radar project by clicking: ``` File ``` -> ``` Open ``` -> ``` wemos_d1r2_radar.ino ```.<br><br>
   
2. Fill in the ``` Additional Board Manager URLs ``` in Arduino IDE<br><br>
   • Method: click ``` File ``` -> ``` Preferences ``` -> enter the ``` Boards Manager Url ``` by copying the following link:
   
   ```
   http://arduino.esp8266.com/stable/package_esp8266com_index.json
   ```
   
3. ``` Board Setup ``` in Arduino IDE<br><br>
   • Method: click ``` Tools ``` -> ``` Board ``` -> ``` Boards Manager ``` -> Install ``` esp8266 ```. Then selecting a Board by clicking: ``` Tools ``` -> ``` Board ``` -> ``` ESP8266 Board ``` -> ``` LOLIN(WEMOS) D1 R2 & mini ```.
   <br><br>
   
4. ``` Change the Board Speed ``` in Arduino IDE<br><br>
   • Method: click ``` Tools ``` -> ``` Upload Speed ``` -> ``` 115200 ```.
   <br><br>
   
5. ``` Install Library ``` in Arduino IDE<br><br>
   • Method: download all the library zip files. Then paste it in the: ``` C:\Users\Computer_Username\Documents\Arduino\libraries ```.
   <br><br>

6. ``` Port Setup ``` in Arduino IDE<br><br>
   • Method: click ``` Port ``` -> Choose according to your device port ``` (you can see in device manager) ```.
   <br><br>

7. Change the ``` WiFi Name ```, ``` WiFi Password ```, and ``` Client ID ``` according to what you are currently using.<br><br>

8. Before uploading the program please click: ``` Verify ```.<br><br>

9. If there is no error in the program code, then please click: ``` Upload ```.

<br><br>

## Processing Setup
1. Open the ``` Processing ``` first, then open the Radar GUI project by clicking: ``` File ``` -> ``` Open ``` -> ``` radar_gui.pde ```.<br>

2. Customize your ``` port ``` with the one in the ``` Arduino IDE ```. This is so that the board can be recognized by ``` Processing ```, so that the code can be run properly.<br>

3. The last step, please click: ``` Run ```.

<br><br>

## MQTT Explorer Setup
1. Open the ``` MQTT Explorer ```. Then, click the Connections: ``` test.mosquitto.org ```.<br>

2. Click the ``` ADVANCED ``` -> ``` Delete All Topics ```.<br>

3. Create a ``` new Topic ``` with QoS "0":
   ```
   coursera/uci/radar
   ```

4. Copy and paste the ``` Client ID ``` into the ``` Arduino IDE ``` project.<br>

5. Next, click: ``` BACK ```. The last step, please click: ``` CONNECT ```.

<br><br>

## Get Started
1. Download and extract this repository.<br><br>

2. Make sure you have the necessary electronic components.<br><br>
   
3. Make sure your components are designed according to the diagram.<br><br>
   
4. Configure your device according to the settings above.<br><br>
   
5. Please enjoy [Done].

<br><br>

## Highlights
<table>
<tr>
<th width="840" colspan="2">Hardware View</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/d031c2ea-2737-4537-8948-1cac52725464" alt="IMG-1"></td>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/dd84d910-2cb5-4e75-99cd-1c362e8c7475" alt="IMG-2"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">MQTT Explorer (JSON data on Topic)</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/37031059-3957-40a9-a5d2-7e38a6d59037" alt="IMG-3"></td>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/fd90dd5e-9056-4480-8bf9-2177f8778d1f" alt="IMG-4"></td>
</tr>
</table>
<table>
<tr>
<th width="840" colspan="2">Serial Monitor (Publish & Subscribe)</th>
</tr>
<tr>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/54902d4c-9631-4c8b-aeb0-248be38e0456" alt="IMG-5"></td>
<td width="420"><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/5a154c46-4529-4fa8-a581-dcfdfbf04676" alt="IMG-6"></td>
</tr>
</table>
<table>
<tr>
<th width="840">Processing (Radar Graphic User Interface)</th>
</tr>
<tr>
<td><img src="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/assets/54527592/6ee9c1eb-2d88-45ba-96fe-12c81b01bc61" alt="IMG-7"></td>
</tr>
</table>

<br><br>

## Reminder
1. Before starting the project, you should test the components first to make sure the devices used can work properly. This has been provided by the creator of the program, please download and try one section at a time.
   
2. The use of serial communication between Arduino IDE and Processing cannot be run simultaneously, so if you want to open the Processing GUI then at the same time you cannot open the Serial Monitor Arduino IDE. It also applies to the other way around.

<br><br>

## Component Testing
You can download the component test file via the following link: <a href="https://github.com/devancakra/IoT-based-Radar-with-Wemos-D1-R2/tree/master/Assets/Component%20Testing">Click Here</a>

<br><br>

## Disclaimer
This application has been created by including third-party sources. Third parties here are service providers, whose services are in the form of libraries, frameworks, and others. I thank you very much for the service. It has proven to be very helpful and implementable.

<br><br>

## LICENSE
MIT License - Copyright (c) 2023 - Devan C. M. Wijaya, S.Kom

Permission is hereby granted without charge to any person obtaining a copy of this software and the software-related documentation files to deal in them without restriction, including without limitation the right to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons receiving the Software to be furnished therewith on the following terms:

The above copyright notice and this permission notice must accompany all copies or substantial portions of the Software.

IN ANY EVENT, THE AUTHOR OR COPYRIGHT HOLDER HEREIN RETAINS FULL OWNERSHIP RIGHTS. THE SOFTWARE IS PROVIDED AS IS, WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, THEREFORE IF ANY DAMAGE, LOSS, OR OTHERWISE ARISES FROM THE USE OR OTHER DEALINGS IN THE SOFTWARE, THE AUTHOR OR COPYRIGHT HOLDER SHALL NOT BE LIABLE, AS THE USE OF THE SOFTWARE IS NOT COMPELLED AT ALL, SO THE RISK IS YOUR OWN.
