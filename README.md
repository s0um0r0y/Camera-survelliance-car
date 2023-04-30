# Camera-survelliance-car

In this project we have made a camera surveillance car with pan tilt control, in which the camera is attached with a pan tilt servo base that rotates 180 degrees in the vertical as well as the horizontal direction. The microcontroller board used to program the car was Arduino Uno, which contains ATmega328P as the microprocessor. The camera used to record the background of the car was a ESP32 Cam Module, which is a WI-FI camera module that can transmit the visual feed through the internet connection and the visual feed can be observed in the online web browser by connecting with the IP address of the ESP32 Cam Module. The movement of the car could be controlled by the user in four different directions – front, back, left and right. The interpretation of the movement instructions and the execution of the movement of the car was enabled by the microcontroller board Arduino Uno. The microcontroller board had an explicit program uploaded to it and this program was written in the software Arduino IDE. The programming language in Arduino IDE is a derivative of C++ programming language.

##	INNOVATION COMPONENT IN THE PROJECT

In this project we have provided mobility for the camera using two pan and tilt servo motors generally camera are attached to a fixed base which restricts its field of view. We increase the field of view to be 180 degrees vertical and 180 degree horizontal. Instead of using Arduino flash memory to run the motors of our car we use ESP32 inbuilt flash memory to store data in its web sockets. We fetch data from the web socket using the Ip address of the ESP32 board and display it on a web-based platform app instead of using an external manual controller or remote. For the battery we used a male to female T dean plugs to ensure smooth transmission of the power from battery to motor driver and the entire assembly.

![image](https://user-images.githubusercontent.com/75070782/235339620-39a125af-1ab8-4f66-9deb-462ee1e1dff1.png)

![image](https://user-images.githubusercontent.com/75070782/235339651-b6328fd9-98dd-490b-8f57-9c3d6165c376.png)

##  CIRCUIT DIAGRAM AND COMPONENTS DESCRIPTION 

a)  Circuit diagram for uploading the Arduino code from the software in the laptop to the microcontroller board and then to the ESP32 Cam Module through breadboard connections.

![image](https://user-images.githubusercontent.com/75070782/235339695-d42640c4-a461-4bd8-a1f4-e14c3dc97775.png)

![image](https://user-images.githubusercontent.com/75070782/235339771-d2c8950b-d67b-4a4d-b0a8-54beaf45e446.png)

![image](https://user-images.githubusercontent.com/75070782/235339775-9aa10eb7-ed86-469b-af8f-38bcbf142fda.png)

b)	Circuit diagram for assembling the entire car

![image](https://user-images.githubusercontent.com/75070782/235339820-a5f87270-bb5f-4692-833a-02a63fbed32f.png)

![image](https://user-images.githubusercontent.com/75070782/235339900-43f3fe19-c674-4327-9d02-1552ff55db87.png)

![image](https://user-images.githubusercontent.com/75070782/235339908-6a933753-1291-4985-8e50-d2d7c3e8a4e7.png)

## COMPONENTS DESCRIPTION
COMPONENT	PRODUCT DESCRIPTION

1.	MICROCONTROLLER BOARD	
ARDUINO UNO R3
( MICROPROCESSOR – Atmega328P )

2.	WIFI CAMERA AND DEVELOPMENT BOARD	
OV2640 CAMERA MODULE
ESP32 CAM WIFI BLUETOOTH DEVELOPMENT BOARD

•	INPUT VOLTAGE : 3.6V– 5V
•	RAM SIZE : 520KB SRAM +4MB PSRAM
•	UART BAUDRATE : 115200 BPS
•	WIFI : 802.11 b/g/n/e/i

3.	BREADBOARD	
400 TIES SOLDERLESS BREADBOARD

4.	MOTOR DRIVER	
L298N MOTOR DRIVER CONTROLLER MODULE

•	INPUT VOLTAGE RANGE : 3.2V – 40V DC
•	CONFIGURATION : DUAL H-BRIDGE DC MOTOR DRIVER
•	OPERATING VOLTAGE : 5V – 35V
•	PEAK CURRENT : 2A
•	TYPE OF INPUT SIGNAL : PWM ( PULSE WIDTH MODULATED ) SIGNAL
•	MAXIMUM POWER CONSUMPTION : 20W

5.	BATTERY	
LITHIUM POLYMER BATTERY PACK

•	CAPACITY : 850 mAh
•	DISCHARGE PLUG : T-CONNECTOR FEMALE
•	MAXIMUM CONTINUOUS DISCHARGE : 30C
•	OUTPUT VOLTAGE : 7.4V
•	MAXIMUM CHARGE RATE : 5C
•	BALANCE PLUG : JST-XH
•	NUMBER OF CELLS : 2

6.	CAR CHASSIS AND ASSEMBLY PACK	
4 WHEELED CAR CHASIS + 4 DC MOTORS ( 5V DC MOTOR ) WITH WHEEL ENCODER + 4 CASTOR WHEELS + M2 SCREWS + 4 SPACERS

7.	PAN TILT SERVO ASSESBLY	
PAN/TILT CAMERA PLATFORM WITH 2-AXIS FPV ( FIRST PERSON VIEW )

SPECIFICATIONS :
•	WEIGHT : 37GMS
•	BASE DIMENSIONS : 37MM*33MM*3MM
•	STANDING HEIGHT ( ZERO TILT) : 67MM

8.	SERVO MOTOR	
SG90 MICRO SERVO MOTOR

•	OPERATING SPEED : 0.12 SECOND/60 DEGREE
•	STALL TORQUE : 1 KG/CM
•	OPERATING VOLTAGE : 3.0V – 7.2V
•	DEAD BANDWIDTH : 7 MICROSECOND

9.	JUMPER WIRES	
•	MALE TO MALE
•	FEMALE TO FEMALE
•	MALE TO FEMALE
 
10.	T PLUG MALE CONNECTOR	DEANS STYLE T PLUG MALE CONNECTOR

•	LENGTH : 14AWG
•	MATERIAL OF CABLE : SILICON

## METHODOLOGY

The project methodology can be divided into two domains : hardware methodology and software methodology.

A)	HARDWARE METHODOLOGY 
1.	First we assembled the car chassis by connecting the four dc motors to the chassis with the help of screws, nuts and bolts.

![image](https://user-images.githubusercontent.com/75070782/235340084-0f5540be-3e53-4563-a36b-a21a3c333a49.png)

![image](https://user-images.githubusercontent.com/75070782/235340092-f5b19d84-ffb2-453c-9345-93ea52b0a7df.png)

2.	We assembled the pan tilt servo assembly base

<img width="314" alt="image" src="https://user-images.githubusercontent.com/75070782/235341553-bbab23a0-9d66-408f-a22b-1a708a93c30d.png">

B)	SOFTWARE METHODOLOGY
1.	To install the ESP32 board in arduino ide we added the url for the json files in the space provided for additional board manager urls.

<img width="409" alt="image" src="https://user-images.githubusercontent.com/75070782/235341647-2c57acda-1b29-46fb-94b8-af641e51b53d.png">

2.	We installed the ESP32 board by going to the boards manager window under the tools section.

<img width="425" alt="image" src="https://user-images.githubusercontent.com/75070782/235341681-1243d699-6fc7-40e0-8c21-f6d0f3e4e0e9.png">

3.	We installed two libraries (AsyncTCP and ESPAsyncWebServer). The AsyncWebServer library helps us to get the visual feed from the camera through the wifi connection. The AsyncTCP library generates the ip address of the web socket of the ESP32 Cam Module.

<img width="431" alt="image" src="https://user-images.githubusercontent.com/75070782/235341770-be9a5694-9caa-4767-8d6d-3fde921cd678.png">

4.	We installed ESP32 servo library from the Ardruino library manager

<img width="451" alt="image" src="https://user-images.githubusercontent.com/75070782/235341794-2bdd91c7-2d58-47f1-9403-269ee70fb731.png">

5.  We setup the ardruino IDE to run ESP32 module where we choose the board as the ESP32 Wrover Module, the upload speed as 115200, flash frequency as 80 MHz, flash mode as QIO, partition scheme as “ Huge APP ( 3MB No OTA/1M8 SPIFFS”, and the core debug level as none.

<img width="433" alt="image" src="https://user-images.githubusercontent.com/75070782/235341857-653c986f-8892-4cc0-9ed7-1ce8b2ee3d16.png">

## RESULTS AND DISCUSSION

Connecting mobile to the ESP32 WIFI board: We type the ip address in the online web browser as 192.168.4.1.This ip address transfers the online visual feed of the camera and displays it in the web browser, alongwith rotation of the servo motor. The name of the wifi sssd is MyWifiCar, password for connecting is 12345678.

<img width="367" alt="image" src="https://user-images.githubusercontent.com/75070782/235341952-6cdf7a77-71b2-42c6-9b58-c01cdc9baacd.png">

<img width="433" alt="image" src="https://user-images.githubusercontent.com/75070782/235342008-ff934a13-0d95-43f3-b0bb-5800f6a380b9.png">

<img width="293" alt="image" src="https://user-images.githubusercontent.com/75070782/235342083-0d83e9ac-5680-49de-b29c-9a53e65c6746.png">

## CONCLUSION

In this project we have made a camera surveillance car with pan tilt control. We navigated through an unknown environment by using the camera feed from ESP32 cam and displayed it on a web page. On web page we had 4 buttons (forward ,left, right, back) which helped used to control the car’s movement in the new and unknown environment. We also had 4 sliders on web page to change the angle of the servo so that we could get a wider field of view and survey the entire area.  

## FUTURE WORK

We plan to extend this project further by running advance algorithms on the ESP32 cam to do face recognition, detection and human pose detection for surveillance application. Combining computer vision with the Esp32-Cam turns this versatile little microcontroller into an AI-powered machine. In facial recognition system we map individual facial features mathematically and store the data as a faceprint. The facial recognition data requires an algorithm to detect part of images for verification. Once verified, the new faceprint can be compared with stored faceprints to determine if there has been a match. We use machine learning algorithms to find human faces in larger images. The face detection algorithm starts with searching for human eye as they are the easiest features to detect. Then the algorithm might aim to detect eyebrows, mouth nose nostrils and the iris. Once the algorithm concludes, that it has found a facial region, it applies additional tests to confirm that it has in fact detected a face.

## REFERENCES

Entire project:

https://www.youtube.com/watch?v=tyY7AN132Xs

surveillance car assembly

https://www.youtube.com/watch?v=HfQ7lhhgDOk

Servo Pan tilt control assembly

https://www.youtube.com/watch?v=Rm_R0MAmHHA

Camera connection Diagram

https://github.com/un0038998/CameraCar/tree/main/Diagrams

Pan tilt control Diagram

https://github.com/un0038998/CameraCarWithPanTiltControl

ESP32 Datasheet

https://media.digikey.com/pdf/Data%20Sheets/DFRobot%20PDFs/DFR0602_Web.pdf

Ardruino UNO R3 Datasheet

https://docs.arduino.cc/resources/datasheets/A000066-datasheet.pdf

Motor Driver Datasheet

https://www.sparkfun.com/datasheets/Robotics/L298_H_Bridge.pdf

Car chassis assembly

https://www.youtube.com/watch?v=Ze4c_a3luqg

