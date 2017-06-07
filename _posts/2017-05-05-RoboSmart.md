---
layout: post
title: RoboSmart
author: Geraldo Braho
tags: 		
subtitle: My senior design project
category: project1
visualworkflow: false
---
{% if page.visualworkflow == true %}
   {% include workflowmatlab.html %}
{% endif %}   


<!--
This HTML was auto-generated from MATLAB code.
To make changes, update the MATLAB code and republish this document.
-->

# Table of Contents

* TOC
{:toc}


<br>


![North American University](/img/robosmart/logo.png)


# Abstract:

In this project, we will deliberate how to control robot  car using Wi-Fi module through android and IPhone application of an android & apple mobile phone. We will also show that we can control the appliances even in the absence of an android phone by web-based application. The advantage of using robot controlled car is it can be used for various purposes like this project can be modified quite easily to include a spy camera and face recognition as well that can stream the videos to the user over Wi-Fi and detect faces. Attempts would be made to use solar cells instead of the regular lithium-ion battery for the project. This robot car can also be used to push the objects from one place to another. This project will be enhanced with better Wi-Fi, which would enable long distance communication. This paper analyses the motion technology to capture gestures through an android smartphone with an inbuilt accelerometer and Wi-Fi module to control the movements of a robot. Sensors placed on robot continuously update the temperature and gas values of surrounding area and display on mobile phone, LCD display. The Arduino processor controls the signals of the Wi-Fi Module. Also a camera is equipped for remote view and the robot will automatically avoid obstacle and move when it is in operation without intervention from the operator.

# Objective:

The basis of this project is to develop an advanced robot surveillance platform that can quickly be deployed in the field with minimal cost and training. This is achieved using readily available commercial off the shelf parts for the chassis and drivetrain, as well as all electronic components. The user interface must be carefully designed to provide an immediate sense of familiarity that allows for easy use, even with minimal training. This objective is achieved using mobile phone or computer and the robot that sends video, by controlling the robot and receive the video. This will provide a simple, yet effective tool to enhance reconnaissance and security monitoring.

# Acknowledgement:

This work would not have been possible without the enormous help of Dr.Ahmet Sonmez at North American University. We are especially indebted to all our computer science department and their staff like : Dr. Suslu, Dr. Aydin, and Dr.Said who have been initiator of this whole idea and who worked taught us more than we could ever give them credit for here. they has shown us, by their example, what a good, persistent and determined engineer (and person) should be.
We are grateful to all of those with whom we have had the pleasure to work during this project. We would like to thank all other professors who were great source of knowledge and support for our work. Most importantly we wish to thank your families whose inspiration and guidance were always with us.

# Introduction:

A robot is a machine designed to execute one or more tasks repeatedly, with speed and precision. There are as many different types of robots as there are tasks for them to perform. A robot is a mechanical or virtual artificial agent, usually an electro-mechanical machine that is guided by a computer program or electronic circuitry. Robots can be autonomous or semi-autonomous. Robots have replaced human in performing repetitive and dangerous tasks which humans prefer not to do, or are unable to do because of size limitations, or which take place in extreme environments such as outer space or the bottom of the sea. Wi-Fi is "short for wireless fidelity and is meant to be used generically when referring of any type of 802.11 network, whether 802.11b, 802.11a, dual-band, etc. Computer manufacturers offer notebook computers with built-in Wi-Fi capability and any standard notebook computer can easily become Wi-Fi enabled by simply plugging in an appropriate Wi-Fi network card. This new technology allows for Internet users to connect nearly 50 times faster than standard modem dial-up. If both Wi-Fi technology and robot are introduced together it will bring a great advantage. Thus we will be able to operate the robot with the help of Wi-Fi and can make hi do whatever we wish to.
In the present day, technology has so improved that an Unmanned Aerial Vehicle (UAV) also called as Drone can be controlled from a distance ranging from 2km to 20,000km. The Mars Rover, which was sent to Mars to explore various features of the planet, is an autonomous robot, which is programmed such that it performs the desired task as it is intended to do. There are many such systems, which are controlled either by Radio Frequency transmission or by creating intelligence. Such robots are called Non-autonomous robots. These robots have the programming logic to do the desired task but the decision power lies in the hand of controller (human) handling the robot. Here the interface can be made using two methods:
- Wired – Here the connection between controller and robot is maintained using wired interface. These interfaces can be serial or parallel but the underlying technology is transmission of signal, which is sent in the form of specific pattern to the robot to carry out the specific task, analyses these patterns with the help of a microcontroller governing its motion.

- Wireless – Here the connection between controller and robot is achieved by wireless interface such as
  - Bluetooth
  - Wi-Fi
  - Wi–Max
  - Zigbee and many more


The underlying technology is transmission of signals wirelessly in air by transmitter, which is captured by the receiver and sent to microcontroller mounted on the robot to carry out the task. Looking at the present demand for robots in this developing world to carry out work effectively and accurately, the development of cost effective robots is necessary.

# Background and Recent Research:

Robots have been with us for less than 50 years but the idea of inanimate creations represents a sincere bid whose success is much older. But real robots did not come into existence until 1950s and 60s. With the growing invention of transistors and integrated circuits, computer industry added brains to the brawn of already existing machines. In 1959, researchers illustrated the possibility of robotic manufacturing when they unveiled a computer-controlled milling machine. Telecom vendor Ericsson created Bluetooth technology in 1994. Android does Google that is open-source make an operating system. With such feature, Android grows rapidly since people can develop their own applications without the burden of certain regulations. Many application developers have contributed to create applications that run on this operating system. There is one who focuses on creating the application of game, one who focuses on creating the application of social media. Usually a smartphone is equipped with several sensors, such as accelerometer sensor. The accelerometer sensor is a sensor that can measure the acceleration due to gravity and vibration [1]. In android, this sensor is used to adjust the landscape or vertical position changes on the smartphone screen and set the hand movements as a tool for gaming consoles. On the other hand robot technology is developing rapidly, not only in software but also the hardware. Currently, it has already been developed a robot that can move flexibly, known as Omni-directional robot. The robot can move left and right and can be rotated on the axis
Manuscript received June, 2015.
Bansode Manisha B, ME VLSI & Embedded Systems –II year,
Vishwabharati Academy'S coe, Ahmednagar, India
Prof. Singh J.K, Asst.professor in E&TC Dept, Vishwabharti Academy’s COE, Ahmednagar, India.
point [2]. Based on the exposure and some research, which have been done previously, this research developed a system to control robot motion, in accordance with the tilt of accelerometer sensor for android smart-phone. In other words, the smartphones will be used as a remote control for robot movement.

# Existing System:

Now days due to advancement in technology various newly designed smart homes make use of Wi-Fi enabled robot for various applications. Mostly they are used for home security purpose. Thus one can keep an eye on the people coming inside home just by the robot car just by introducing a camera into it.
Various other application are also done by this robot car like doing various works on the command ex- switching on the lights when the robot is given command by the Wi-Fi enabled device.

# Proposed System:

The robot car can be easily moved from one place to another just by a single device. Robot car can be used for security purpose with the installation of a camera. We can make the car do various task like moving an object from one place to another without applying any physical force.


# Design Overview:
## Module-1:
Wi-Fi enabled smart robot is a system which can be controlled using a custom designed webpage. To make this feasible, an Arduino microcontroller board with an Arduino Ethernet Shield is used which guides the robot along the desired path. Switch control mode of robot is controlled using joystick and can be appropriately guided back, forth, left and right.
In this project, we have extended an interface to the switch control mode, which suits our requirements. Finally we are successful in interfacing our robot with the Arduino and eventually control it in the wireless environment through the control buttons on the custom built webpage. From the block diagram, it is evident that the control over robot can be achieved from the custom designed web page and hence the robot can be maneuvered in the designated directions.
When the allocated web address is entered in the web browser, webpage containing the control of robot gets loaded. When clicked on the respective direction controls on the webpage, the subsequent control packets are generated. These packets are transferred via internet and is received by the Arduino Ethernet Shield serially through the router at the receiver end. The data is then transferred from the Ethernet Shield via an SPI interface into the Arduino board and with the help of a motor driver circuit (L293D), the designated directions are henceforth assumed.

![Block Diagram of Wifi-Robot](/img/robosmart/1.png)


## Module-2:

In the first module, we have successfully achieved the mobility of robot via internet. This module describes controlling the robot using Bluetooth. Here we have used a Bluetooth module connected to the Arduino board which is encrypted by a MAC address. We have created an android applet with java which communicates serially with the Arduino board. By entering the allocated MAC address of the Bluetooth module, the connection between Arduino board and android phone is achieved. Controlling the direction of motion of robot is achieved by tapping the specific icon on the android phone.

![Block Diagram of Bluetooth enabled robot](/img/robosmart/1.png)


# System Description:

The system has two parts, namely; hardware and software. The hardware architecture consists of a stand-alone embedded system that is based on ATMEGA 328 adruino board, which is a 28 pin IC. It also consists of l293d, which is a motor driving IC and Wi-Fi module.

# Block Diagram of proposed system:

![](/img/robosmart/3.png)


# Equipment Used:

1. 1x Arduino Uno board
2. 1x 4WD Robotic Car kit (4 wheels, 4 motors, chassis, AA battery enclosure, screws)
3. 6x AA batteries
4. 1x 9V battery
5. 1x 9V battery power cable barrel jack connector
6. 1x L298N Motor Module
7. 1x Arduino Sensor Shield v5.0
8. 1x HC-SR04 Ultrasonic Sensor
9. 1x Servo motor (any small servo motor will do but if you don’t have one you can leave it out)
10. Assorted color wires:
   - 4x female-to-female wires for Ultrasonic Sensor
   - 8x female-to-female wires for the Motor Module to Sensor Shield
   - 	8x bare-ended wires to go from the four motors to the Motor Module
   - 2x bare-ended wires to go from the Motor Module to Sensor Shield
   - 3x wires for the servo motor with female end attaching to Sensor Shield (should already be included with the servo motor)
   - 2x bare-ended wires to go from AA Battery enclosure to the motor Module (should already be included with the battery enclosure)
11.	Arduino IDE software – free at http://www.arduino.cc
12.	1x USB cable (A male plug to B male plug)
13.	A computer to program with.

![Equipment](/img/robosmart/5.png)


# Assembling:

## How to Connect the Wires:

- Connect the red wire (voltage) from the battery enclosure to VCC on the L298N Motor Module.
- Connect the black wire (ground) from the battery enclosure to GND on the Motor Module.
- Connect the red wire from Motor A1 (rear left) and the red wire from Motor A2 (front left) to OUT1 on the Motor Module (both wires can be twisted together and will go into OUT1 – the wiring diagram further down this page shows how to do this).
- Connect the black wire from Motor A1 (rear left) and the black wire from Motor A2 (front left) to OUT2 on the Motor Module.
- Connect the red wire from Motor B1 (rear right) and the red wire from Motor B2 (front right) to OUT3 on the Motor Module.
- Connect the black wire from Motor B1 (rear right) and the black wire from Motor B2 (front right) to OUT4 on the Motor Module.
- Connect a female-to-female end wire from ENA (Engine A) on the Motor Module to signal pin 1 on the Sensor Shield (the 2 pin in the S row. There are three rows – S stands for Signal, V for Voltage and G for Ground).
- Connect a female-to-female end wire from 5V (next to ENA) on the Motor Module to voltage pin 1 on the Sensor Shield (it doesn’t really matter which pin for voltage as long as it is in the V row)
- Connect a female-to-female end wire from IN1 on the Motor Module to signal pin 2 on the Sensor Shield.
- Connect a female-to-female end wire from IN2 on the Motor Module to signal pin 3 on the Sensor Shield.
- Connect a female-to-female end wire from IN3 on the Motor Module to signal pin 4 on the Sensor Shield.
- Connect a female-to-female end wire from IN4 on the Motor Module to signal pin 5 on the Sensor Shield.
- Connect a female-to-female end wire from 5V (next to ENB) on the Motor Module to voltage pin 6 on the Sensor Shield (it doesn’t really matter which pin for voltage as long as it is in the V row).
- Connect a female-to-female end wire from ENB (Engine B) on the Motor Module to signal pin 6 on the Sensor Shield.
-	Connect the signal wire from the servo motor to signal (S) pin 7 on the Sensor Shield, the voltage wire from the servo motor to the voltage (V) pin 7 on the Sensor Shield, and the ground wire from the servo motor to the GND (G) pin 7 on the Sensor Shield.
- Attach the Ultrasonic Sensor to the servo motor and then attach the servo motor to the front of the car so that it can scan left and right looking for objects in its path. You can use sticky tape, blu-tack, glue or a 3D printed/laser cut mount or whatever you like to attach everything, as long as everything is firmly mounted
- Use female-to-female end plugs to connect the Ultrasonic sensor to the Sensor Shield. Firstly, attach the TRIG pin from the Ultrasonic sensor to signal (S) pin 8 on the Sensor Shield.
- Attach the ECHO pin from the ultrasonic sensor to signal (S) pin 9 on the Sensor Shield.
- Attach the VCC pin from the Ultrasonic Sensor to the voltage (V) pin 10 on the Sensor Shield. Lastly, attach the GND pin from the Ultrasonic Sensor to the GND (G) pin 11 on the Sensor Shield.
Now attach the Sensor Shield on top of the Arduino Uno board making sure to not bend any pins. Connect a 9V Battery Barrel Jack Connector to a 9V battery and then plug this in to the Arduino’s barrel jack (see diagram below). That’s it! After all these long steps I put the batteries and started messing around with the code.



![How To do the wire connection ](/img/robosmart/4.png)


# Software Used

## System Environment:  
Using a desktop PC with:
- Intel Core i5 or higher
- 4GB HDD3 RAM or higher
- 1TB Hard Drive
- Internet Connectivity
- 2 USB Ports
### Software:
- Although the host is windows, we will be using Ubuntu Server as a virtual machine. The next are the tools we need to install into Ubuntu.
- MySQL configured
- FTP server settings
- OpenSSH Server
- VNC Server/viewer to connect with Raspberry Pi
- Arduino Environment
- Fritzing

# How to install Ubuntu Server:  
## Step 1: Creating a new virtual machine in virtualbox:
This step explain how to set up a new virtual machine to host Ubuntu Server. Below is a step-by-step guide:
- Download and install Oracle VirtualBox from https://www.virtualbox.org/wiki/Downloads.
- Open VirtualBox. Then click “New” button to create new virtual Machine.
- Give a name to the virtual machine.
- Select Type as “Linux” and version “Ubuntu (64 bit)”.
- Select memory(RAM) as 1GB.
- Press Next with default option on “Create a new virtual hard drive now”
- Select disk type as “VMDK” which is also compatible with VMware Workstation.
- Select “Dynamically allocated” option which will allocate the space as and when data is created. If you select the option “Fixed size”, it will allocate the total disk space at once.
- Allocate the disk space. I have selected 32GB to be the VM disk space.
- Now a Virtual Machine is created now, but it does not have any operating system installed inside it. We will now install ubuntu Server 16.10 inside this newly created virtual machine.

## Step 2: Installing ubuntu Server 16.10 inside VirtualBox virtual machine.

Installing the operating system inside a virtual machine is almost the same as installing it on a real hard disk, follow the next steps to complete the installation.
- Download Ubuntu server 16.10 ISO from http://www.ubuntu.com/download/server.
- Download Ubuntu server 12.04 LTS ISO from http://www.ubuntu.com/download/server.
- Power on the VM and select “Choose a virtual CD/DVD disk file” from “Devices->CD/DVD Devices”.
- Attach the download ISO to the VM and reset the VM from “Machine->Reset”.
- VM will boot with the attached ISO. Select “English” as language.
- select “Install Ubuntu Server”
- Select installation language as “English”.
- Select your country.
- Configure your keyboard Layout.
- Enter the hostname. This will be name of the system.
- Create user for accessing the machine as a non-root user.
- Configure system clock.
- Partition the disk. Use default options.
- Configure the proxy if your network is behind a proxy server.
- Select update policy.
- Install “OpenSSH server” with the OS so that we can directly login via ssh. Press space to select the option.
- Select “DNS Server” and “LAMP Server” as well.
- Install GRUB boot loader.
- Ubuntu installation is now complete and the vm is ready to use.. Login with the username and password created above.

# Hardware Setup
The hardware setup consists of following components.
*Microcontroller:* The microcontroller board used in this setup is Arduino Mega ADK based on Atmega2560 which has 54 digital I/O pins and powered via the USB. It has a clock speed of 16MHz and can be programmed by Arduino software. The Arduino ADK has a number of facilities for communicating with a computer, another Arduino, or other microcontrollers. Arduino Ethernet shield: It has an Ethernet port which allows to connect it to the Ethernet port of a computer or a router. It is placed over the Arduino board with the specified digital and analog pins mating each other and power to run the Ethernet Shield is drawn from the Arduino board itself. The packet data from internet is transferred serially to Arduino board via the Ethernet cable connected between Ethernet Shield and computer.

 ![](/img/robosmart/6.png)

*Wi-Fi:* In the module-2 of our project, we are controlling the robot via a Wifi from an phone. This requires a UART (Universal Asynchronous Receiver Transmitter) Bluetooth modem at the receiver end which is connected serially with the Arduino board. The Bluetooth modem is powered by Arduino board and is encrypted with a MAC address which when entered on the android phone, achieves communication with the Arduino board.
*Prototype vehicle:* We are using a four wheeled vehicle as shown in Fig.3 which will house the Arduino board with Ethernet Shield, motor driver circuit, Bluetooth modem, wireless camera and the power source. A 12-volt Battery drives the vehicle; 60 rpm DC geared motor and will be able to perform all the maneuvers as desired by the controller.
*Camera:* A wireless camera with a TV tuner card is used to obtain the video feedback from the robot during its motion when it is controlled from a remote location. This video feedback helps the controller to control the direction of motion of robot along the desired path.
*Power source:* To drive the vehicle, we are using a 12-volt rechargeable battery which gives the maximum speed and torque. The Arduino board and Ethernet Shield is energized by a 5-volt battery which synchronizes with its operating voltage. Hence we are using dual power source to meet our requirements.


# Software Integration:

Arduino Mega ADK board can not only be programmed using Arduino software but with also through Eclipse, Processing and LabView. We chose to program the control algorithm in Arduino software by creating a web server. The webpage contains icons clicking upon which will guide the robot to move back, forth, left and right. The web

 ![](/img/robosmart/7.png)


 page is accessed via internet and commands are sent via router in packets which is received at the receiver end and transferred serially by the Ethernet port of Ethernet Shield into the Arduino board to control the motion of robot. For module-2, we used java for programming to control the robot. Programming is done in Eclipse, which is a tool for creating an applet from java programming language. The java programming is so done that, the icons in applet resembles the control done using a joystick. Applet is saved in .apk format and transferred to android phone. By entering the MAC address of Bluetooth modem, connection between Arduino board and the phone is established which allows the user to control various motions of the robot.


# Advantages and Disadvantages of the project (Wi-Fi Robot):

![](/img/robosmart/8.png)


# Comparison between Wi-Fi and Bluetooth RC Car:

![](/img/robosmart/9.png)


# Conclusion:

Hence the two modules of controlling the robot is successfully tested and demonstrated. Though controlling using Wi-Fi limits the range of distance for communication, a smart and easy means to guide a robot is achieved. Controlling the motion of robot via Internet is one of the easiest means as it requires the user to access the designated webpage to guide it. This system can be used in defense applications for detecting landmines in war field and for bomb detections by mounting a metal detector sensor on it. Further, the size of device can be miniaturized based upon specific applications.

# Future Work:

Robots are essentially a self-contained tribute to the wonders of technology. The most advanced models use fast computer processing, high-definition cameras, artificial intelligence and long-range sensors.
This prototype could and will be enhanced by adding a face recognition program that detects intruders or unfamiliar faces and notify home owners, for instance, through a phone application. Along with face recognition, listening to voices and understanding clues is another big feature that could be implemented so the robot can perform tasks only by listening to commands.
As for today, the phone application is simple and limited to moving the robot from point A to point B. A better application would be developed to enable live video streaming over the cloud, as well as notifications and warnings.
Another enhancement could be powering the robot with solar cells for longer durability of energy. A battery, no matter how big, could only last for a limited time, while solar cells provide unlimited source of energy especially if the robot is operating outside.
 Many features and enhancements could be added to RoboSmart. All of which give us a pretty good idea where technology is heading. In some ways, a robot provides a glimmer of the future and IT advancements.

# References

Arduino – ArduinoBoardUno  (n.d.). Retrieved May 4, 2017 from https://www.arduino.cc/en/main/arduinoBoardUno
Arduino UNO WiFi. (n.d.). Retrieved May 04, 2017, from http://www.arduino.org/products/boards/arduino-uno-wifi
Atmega328/P“ (n.d.). Retrieved May 04, 2017, from http://www.atmel.com
Hisham,, M., Prabhu, S., & Kumar, A. A Wi-Fi Enabled Robot. Manipal Centre For Information Sciences. Retrieved from http://manipal.net/mdn/tech_papers/iee_wifi_enable_robot.pdf
Pavan, C., & Sivakumar, B. (2012). Wi-Fi ROBOT FOR VIDEO MONITORING & SURVEILLANCE SYSTEM. International Journal Of Scientific & Engineering Research, 3(2229-5518).
 	Rosebrock, A. “Common Errors Using The Raspberry Pi Camera Module - Pyimagesearch”. PyImageSearch. Retrieved May 05, 2017 from http://www.pyimagesearch.com/2016/08/29/common-errors-using-the-raspberry-pi-camera-module/
Rosebrock, A. “Accessing the Raspberry Pi Camera with OpenCV and Python” - PyImageSearch. PyImageSearch. Retrieved May 05, 2017, from http://www.pyimagesearch.com/2015/03/30/accessing-the-raspberry-pi-camera-with-opencv-and-python/





# Appendix A

### Self Control and avoiding obstacles

```c
// Setup Motor A (front and rear) pins
int enableA = 1;
int pinA1 = 3;
int pinA2 = 2;
// Setup Motor B (front and rear) pins
int enableB = 6;
int pinB1 = 5;
int pinB2 = 4;
// Setup Ultrasonic Sensor pins
#define trigPin 8
#define echoPin 9
void setup() {
  // The setup code goes here and runs once only
  // Configure the pin modes for each drive motor
   pinMode (enableA, OUTPUT);
   pinMode (pinA1, OUTPUT);
   pinMode (pinA2, OUTPUT);
   pinMode (enableB, OUTPUT);
   pinMode (pinB1, OUTPUT);
   pinMode (pinB2, OUTPUT);
   // Configure the pin modes for the Ultrasonic Sensor
   pinMode(trigPin, OUTPUT);
   pinMode(echoPin, INPUT);
}
void loop() {
  // Main code goes here and will run repeatedly:
  car(); // function keeps moving car forward while distance of objects in front are > 15cm away
  avoid(); // function makes car go back, turn slightly right to move forward in new direction
}
// Create motor functions
void motorAforward() {
 digitalWrite (pinA1, HIGH);
 digitalWrite (pinA2, LOW);
}
void motorBforward() {
 digitalWrite (pinB1, LOW);
 digitalWrite (pinB2, HIGH);
}
void motorAbackward() {
 digitalWrite (pinA1, LOW);
 digitalWrite (pinA2, HIGH);
}
void motorBbackward() {
 digitalWrite (pinB1, HIGH);
 digitalWrite (pinB2, LOW);
}
void motorAstop() {
 digitalWrite (pinA1, HIGH);
 digitalWrite (pinA2, HIGH);
}
void motorBstop() {
 digitalWrite (pinB1, HIGH);
 digitalWrite (pinB2, HIGH);
}
void motorAcoast() {
 digitalWrite (pinA1, LOW);
 digitalWrite (pinA2, LOW);
}
void motorBcoast() {
 digitalWrite (pinB1, LOW);
 digitalWrite (pinB2, LOW);
}
void motorAon() {
 digitalWrite (enableA, HIGH);
}
void motorBon() {
 digitalWrite (enableB, HIGH);
}
void motorAoff() {
 digitalWrite (enableA, LOW);
}
void motorBoff() {
 digitalWrite (enableB, LOW);
}
// Setup movement functions
void forward (int duration) {
 motorAforward();
 motorBforward();
 delay (duration);
}
void backward (int duration) {
 motorAbackward();
 motorBbackward();
 delay (duration);
}
void right (int duration) {
 motorAbackward();
 motorBforward();
 delay (duration);
}
void left (int duration) {
 motorAforward();
 motorBbackward();
 delay (duration);
}
void coast (int duration) {
 motorAcoast();
 motorBcoast();
 delay (duration);
}
void breakRobot (int duration) {
 motorAstop();
 motorBstop();
 delay (duration);
}
void disableMotors() {
 motorAoff();
 motorBoff();
}
void enableMotors() {
 motorAon();
 motorBon();
}
// Setup Ultrasonic Sensor distance measuring
int distance() {
  int duration, distance;
  digitalWrite(trigPin, HIGH);
  delayMicroseconds(1000);
  digitalWrite(trigPin, LOW);
  duration = pulseIn(echoPin, HIGH);
  distance = (duration/2) / 29.1;
  return distance;
}
// Setup the main car function
void car() {
int distance_0;
distance_0 = distance();
  // Keep moving forward in a straight line while distance of objects in front > 15cm away
  while(distance_0 > 30)
  {
     motorAon();
     motorBon();
     forward(1);
     distance_0 = distance();
  }
  breakRobot(0);
}
// Go back and turn slightly right to move car in new direction
// This function only runs if an obstacle within 15cm is detected
void avoid()
{
    backward(500);
    right(360);
}



```


### Wifi Robot  Intelligent( Arduino)

```c
/*

* Abstract: wifi robot intelligent car control
*/
#include <Servo.h>
#include <EEPROM.h>

int ledpin = 13;//Set the system startup light
int ENA = 5;//L298 Enable A
int ENB = 6;//L298 Enable B
int INPUT2 = 7;//Motor interface 1
int INPUT1 = 8;//Motor interface 2
int INPUT3 = 12;//Motor interface 3
int INPUT4 = 13;//Motor interface 4
int num;//Defines the motor flag

int Echo = A5;  // Define the ultrasonic signal to receive the pin
int Trig = A4;  // Defines the ultrasonic signal firing pin
int Input_Detect_LEFT = A3;    //Define the left side of the car infrared
int Input_Detect_RIGHT = A2;  //Define the right side of the car infrared
int Input_Detect = A1;//Define the car front infrared
int Carled = A0;//Define the car lights interface
int Cruising_Flag = 0;
int Pre_Cruising_Flag = 0 ;
int Left_Speed_Hold = 255;//Defines the left speed variable
int Right_Speed_Hold = 255;//Defines the right speed variable

//The macro defines the direction of the car steering
#define MOTOR_GO_FORWARD  {digitalWrite(INPUT1,LOW);digitalWrite(INPUT2,HIGH);digitalWrite(INPUT3,LOW);digitalWrite(INPUT4,HIGH);}    //Body forward
#define MOTOR_GO_BACK	  {digitalWrite(INPUT1,HIGH);digitalWrite(INPUT2,LOW);digitalWrite(INPUT3,HIGH);digitalWrite(INPUT4,LOW);}    //Body forward
#define MOTOR_GO_RIGHT	  {digitalWrite(INPUT1,HIGH);digitalWrite(INPUT2,LOW);digitalWrite(INPUT3,LOW);digitalWrite(INPUT4,HIGH);}    //Body forward
#define MOTOR_GO_LEFT	  {digitalWrite(INPUT1,LOW);digitalWrite(INPUT2,HIGH);digitalWrite(INPUT3,HIGH);digitalWrite(INPUT4,LOW);}    //Body forward
#define MOTOR_GO_STOP	  {digitalWrite(INPUT1,LOW);digitalWrite(INPUT2,LOW);digitalWrite(INPUT3,LOW);digitalWrite(INPUT4,LOW);}    //Body forward


void forward(int num)
{
	switch(num)
	{
		case 1:MOTOR_GO_FORWARD;return;
		case 2:MOTOR_GO_FORWARD;return;
		case 3:MOTOR_GO_BACK;return;
		case 4:MOTOR_GO_BACK;return;
		case 5:MOTOR_GO_LEFT;return;
		case 6:MOTOR_GO_LEFT;return;
		case 7:MOTOR_GO_RIGHT;return;
		case 8:MOTOR_GO_RIGHT;return;
		default:return;
	}
}

void back(int num)
{
		switch(num)
	{
		case 1:MOTOR_GO_BACK;return;
		case 2:MOTOR_GO_BACK;return;
		case 3:MOTOR_GO_FORWARD;return;
		case 4:MOTOR_GO_FORWARD;return;
		case 5:MOTOR_GO_RIGHT;return;
		case 6:MOTOR_GO_RIGHT;return;
		case 7:MOTOR_GO_LEFT;return;
		case 8:MOTOR_GO_LEFT;return;
		default:return;
	}
}
void left(int num)
{
		switch(num)
	{
		case 1:MOTOR_GO_LEFT;return;
		case 2:MOTOR_GO_RIGHT;return;
		case 3:MOTOR_GO_LEFT;return;
		case 4:MOTOR_GO_RIGHT;return;
		case 5:MOTOR_GO_FORWARD;return;
		case 6:MOTOR_GO_BACK;return;
		case 7:MOTOR_GO_FORWARD;return;
		case 8:MOTOR_GO_BACK;return;
		default:return;
	}
}
void right(int num)
{
		switch(num)
	{
		case 1:MOTOR_GO_RIGHT;return;
		case 2:MOTOR_GO_LEFT;return;
		case 3:MOTOR_GO_RIGHT;return;
		case 4:MOTOR_GO_LEFT;return;
		case 5:MOTOR_GO_BACK;return;
		case 6:MOTOR_GO_FORWARD;return;
		case 7:MOTOR_GO_BACK;return;
		case 8:MOTOR_GO_FORWARD;return;
		default:return;
	}
}


//Servo servo1;// Create a steering gear # 1
//Servo servo2;// Create a steering gear # 2
Servo servo3;// Create the steering gear # 3
Servo servo4;// Create a steering gear # 4
Servo servo5;// Create a steering gear # 5
Servo servo6;// Create a steering gear # 6
Servo servo7;// Create a steering gear # 7
Servo servo8;// Create a steering gear # 8



//byte angle1=60;//Servo # 1 initial value
//byte angle2=60;//Servo # 2 initial value
byte angle3=60;//Servo # 3 initial value
byte angle4=60;//Servo # 4 initial value
byte angle5=60;//Servo # 5 initial value
byte angle6=120;//Servo # 6 initial value
byte angle7=60;//Servo # 7 initial value
byte angle8=60;//Servo # 8 initial value


int buffer[3];  //The serial port receives the data cache
int rec_flag;   //Serial receive flag
int serial_data;
int Uartcount;
int IR_R;
int IR_L;
int IR;
unsigned long Pretime;
unsigned long Nowtime;
unsigned long Costtime;
float Ldistance;
```


### Open the headlights

```c


/*
*********************************************************************************************************
** Function name ：Open_Light()
** Function: Open the headlights
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void Open_Light()//Open headlights
    {
      digitalWrite(Carled,HIGH);   //Pull low, positive connected to the power supply, negative Io mouth
      delay(1000);
    }

```


### Turn off the lights

```c

/*
*********************************************************************************************************
** Function name ：Close_Light()
** Function: Turn off the lights
**Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void Close_Light()//Off the lights
    {
      digitalWrite(Carled, LOW);   //Pull low, positive connected to the power supply, negative Io mouth
      delay(1000);
    }

```

### Infrared obstacle avoidance function

```c

/*
*********************************************************************************************************
** Function name  ：Avoiding()
** Function function: Infrared obstacle avoidance function
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void  Avoiding()//Infrared obstacle avoidance function
    {
      IR = digitalRead(Input_Detect);
       if((IR == HIGH))
       {
          forward(num);;//Direct line
          return;
       }
       if((IR == LOW))
       {
            MOTOR_GO_STOP;//stop
            return;
       }
    }

```


### line inspection mode

```c


/*
*********************************************************************************************************
** Function name ：FollowLine()
** Function function: line inspection mode
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void FollowLine()   // Line inspection mode
    {
      IR_L = digitalRead(Input_Detect_LEFT);//Read the left sensor value
      IR_R = digitalRead(Input_Detect_RIGHT);//Read the right sensor value

      if((IR_L == LOW) && (IR_R == LOW))//Both sides simultaneously detect obstacles
      {
        forward(num);//Direct line
        return;

      }
      if((IR_L == LOW) && (IR_R == HIGH))//The right side of the obstacles
      {
        left(num);//Turn Left
        return;

      }
      if((IR_L == HIGH) &&( IR_R == LOW))//Obstruction on the left
      {
        right(num);//Turn right
        return;

      }
      if((IR_L == HIGH) && (IR_R == HIGH))//Are detected around, as in the video as encountered in a cross tape
      {
        MOTOR_GO_STOP;//Stop
        return;
       }
    }

```

### Ultrasonic measurement of distance


```c



/*
*********************************************************************************************************
** Function name ：Get_Distence()
** Function: Ultrasonic measurement of distance
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
char Get_Distence()//Measure the distance
 {
      digitalWrite(Trig, LOW);   // Let the ultrasonic emission low voltage 2μs
      delayMicroseconds(2);
      digitalWrite(Trig, HIGH);  // So that ultrasonic emissions of high voltage 10μs, where at least 10μs
      delayMicroseconds(10);
      digitalWrite(Trig, LOW);    // Maintain ultrasonic emission Low voltage
      Ldistance = pulseIn(Echo, HIGH);  // Reading difference time difference
      Ldistance= Ldistance/5.8/10;      // Change the time to distance (in centimeters)
    //  Serial.println(Ldistance);      //Show distance
      return Ldistance;

  }

```

### Ultrasonic obstruction

```c

/*
*********************************************************************************************************
** Function name ：Avoid_wave()
** Function: Ultrasonic obstruction
** Entry parameters: none
* ** export parameters: none
* *********************************************************************************************************
*/
void Avoid_wave()//Ultrasonic obstacle avoidance function
{
  Get_Distence();
  if(Ldistance < 15)
      {
          MOTOR_GO_STOP;
      }
      else
      {
           forward(num);
      }
}

```

### Ultrasonic distance PC side display

```c

/*
*********************************************************************************************************
** Function name ：Send_Distance()
** Function function: Ultrasonic distance PC side display
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void Send_Distance()//The ultrasonic distance is displayed on the PC side
{
  int dis= Get_Distence();
  Serial.write(0xff);
  Serial.write(0x03);
  Serial.write(0x00);
  Serial.write(dis);
  Serial.write(0xff);
  delay(1000);
}

```

### Delayed program

```c

/*
*********************************************************************************************************
** Function name ：Delayed()
** Function: Delayed program
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void  Delayed()    //Delay 40 seconds and other WIFI module started
{
    int i;
    for(i=0;i<20;i++)
    {
        digitalWrite(ledpin,LOW);
        delay(1000);
        digitalWrite(ledpin,HIGH);
        delay(1000);
    }
}

```


### System initialization (serial port, motor, servo, light initialization).

```c

/*
*********************************************************************************************************
** Function name ：setup().Init_Steer()
**Function: System initialization (serial port, motor, servo, light initialization).
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void Init_Steer()//The steering machine is initialized (the angle is the last saved value)
{
   // angle1 = EEPROM.read(0x01);//Read the value in register 0x01
   // angle2 = EEPROM.read(0x02);//Read the value in register 0x02
    angle3 = EEPROM.read(0x03);//Read the value in register 0x04
    angle4 = EEPROM.read(0x04);//Read the value in register 0x05
    angle5 = EEPROM.read(0x05);//Read the value in register 0x06
    angle6 = EEPROM.read(0x06);//Read the value in register 0x07
    angle7 = EEPROM.read(0x07);//Read the value in register 0x08
    angle8 = EEPROM.read(0x08);//Read the value in register 0x09

    if(angle7 == 255 && angle8 == 255)
    {
       // EEPROM.write(0x01,60);//The initial perspective into the address 0x01 inside
       // EEPROM.write(0x02,60);//The initial perspective into the address 0x02 inside
        EEPROM.write(0x03,60);//The initial perspective into the address 0x03 inside
        EEPROM.write(0x04,60);//The initial perspective into the address 0x04 inside
        EEPROM.write(0x05,60);//The initial perspective into the address 0x05 inside
        EEPROM.write(0x06,120);//The initial perspective into the address 0x06 inside
        EEPROM.write(0x07,60);//The initial perspective into the address 0x07 inside
        EEPROM.write(0x08,60);//The initial perspective into the address 0x08 inside
        return;
    }

   // servo1.write(angle1);//Assign the saving angle to the servo 1
   // servo2.write(angle2);//Assign the save angle to the servo 2
    servo3.write(angle3);//Assign the saving angle to the steering gear 3
    servo4.write(angle4);//Assign the saving angle to the steering gear 4
    servo5.write(angle5);//Assign the saving angle to the servo 5
    servo6.write(angle6);//Assign the saving angle to the steering gear  6
    servo7.write(angle7);//Assign the saving angle to the steering gear 7
    servo8.write(angle8);//Assign the saving angle to the servo 8
    num = EEPROM.read(0x10);//Read the value in register 0x10
    if(num==0xff)EEPROM.write(0x10,1);
}

void setup()
{
    pinMode(ledpin,OUTPUT);
    pinMode(ENA,OUTPUT);
    pinMode(ENB,OUTPUT);
    pinMode(INPUT1,OUTPUT);
    pinMode(INPUT2,OUTPUT);
    pinMode(INPUT3,OUTPUT);
    pinMode(INPUT4,OUTPUT);
    pinMode(Input_Detect_LEFT,INPUT);
    pinMode(Input_Detect_RIGHT,INPUT);
    pinMode(Carled, OUTPUT);
    pinMode(Input_Detect,INPUT);
    pinMode(Echo,INPUT);
    pinMode(Trig,OUTPUT);

    Delayed();//Delay 40 seconds and other WIFI module started
    analogWrite(ENB,Left_Speed_Hold);//Assign value to L298 enable B
    analogWrite(ENA,Right_Speed_Hold);//Assign value to L298 enabled side A
    digitalWrite(ledpin,LOW);
    //servo1.attach(SDA);//Define the steering gear 1 control port
    //servo2.attach(SCL);//Define the steering gear 2 control port
    servo3.attach(3);//Define the steering gear 3 control port
    servo4.attach(4);//Define the steering gear 4 control port
    servo5.attach(2);//Define the steering gear 5 control port
    servo6.attach(11);//Define the steering gear 6 control port
    servo7.attach(9);//Define the steering gear 7 control port
    servo8.attach(10);//Define the steering gear 8 control port
    Serial.begin(9600);//The serial port baud rate is set to 9600 bps
    Init_Steer();
}

```

### Main function

```c
/*
*********************************************************************************************************
** Function name: loop ()
** Function: Main function
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void Cruising_Mod()//Mode function switching function
    {

	 if(Pre_Cruising_Flag != Cruising_Flag)
	 {
	     if(Pre_Cruising_Flag != 0)
		 {
		     MOTOR_GO_STOP;
		 }

    	 Pre_Cruising_Flag =  Cruising_Flag;
	 }
	switch(Cruising_Flag)
	  {

	   case 2:FollowLine(); return;//Line inspection mode
	   case 3:Avoiding(); return;//Obstacle avoidance mode
	   case 4:Avoid_wave();return;//Ultrasonic obstacle avoidance mode
           case 5:Send_Distance();//The ultrasonic distance is displayed on the PC side
	   default:return;
	  }

}

void loop()
  {
    while(1)
    {
        Get_uartdata();
        UartTimeoutCheck();
        Cruising_Mod();
     }
  }

```


### Serial command decode

```c

/*
*********************************************************************************************************
** Function name: Communication_Decode ()
** Function: Serial command decode
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void Communication_Decode()
{
    if(buffer[0]==0x00)
    {
        switch(buffer[1])   //Motor command
        {
            case 0x01:MOTOR_GO_FORWARD; return;
	    case 0x02:MOTOR_GO_BACK;    return;
	    case 0x03:MOTOR_GO_LEFT;    return;
            case 0x04:MOTOR_GO_RIGHT;   return;
	    case 0x00:MOTOR_GO_STOP;    return;
           default: return;
        }
    }
   else if(buffer[0]==0x01)//Steering command
    {
        if(buffer[2]<1)return;
        switch(buffer[1])
        {
           // case 0x01:angle1 = buffer[2];servo1.write(angle1);return;
           // case 0x02:angle2 = buffer[2];servo2.write(angle2);return;
            case 0x01:if(buffer[2]>170)return;angle3 = buffer[2];servo3.write(angle3);return;
            case 0x02:if(buffer[2]>170)return;angle4 = buffer[2];servo4.write(angle4);return;
            case 0x03:if(buffer[2]>170)return;angle5 = buffer[2];servo5.write(angle5);return;
            case 0x04:if((buffer[2]<110)||(buffer[2]>178))return;angle6 = buffer[2];servo6.write(angle6);return;
            case 0x07:if(buffer[2]>170)return;angle7 = buffer[2];servo7.write(angle7);return;
            case 0x08:if(buffer[2]>170)return;angle8 = buffer[2];servo8.write(angle8);return;
            default:return;
        }
    }

   else if(buffer[0]==0x02)//Speed control
	{
		if(buffer[2]>10)return;

		if(buffer[1]==0x01)//Left gear
		{
                        Left_Speed_Hold=buffer[2]x16+95;//Speed stall is 0 ~ 10 converted into pwm speed pwm less than 95 motor does not turn
                        analogWrite(ENB,Left_Speed_Hold);
		}
                if(buffer[1]==0x02)//On the right
                {
                        Right_Speed_Hold=buffer[2]x16+95;//Speed stall is 0 ~ 10 converted into pwm speed pwm less than 95 motor does not turn
                        analogWrite(ENA,Right_Speed_Hold);
                }else return;
        }
    else if(buffer[0]==0x33)//Read the steering angle and assign the value
	{
		 Init_Steer();return;
        }
    else if(buffer[0]==0x32)//Save command
    {
       // EEPROM.write(0x01,angle1);
       // EEPROM.write(0x02,angle2);
        EEPROM.write(0x03,angle3);
        EEPROM.write(0x04,angle4);
        EEPROM.write(0x05,angle5);
        EEPROM.write(0x06,angle6);
        EEPROM.write(0x07,angle7);
        EEPROM.write(0x08,angle8);
        return;
    }
    	else if(buffer[0]==0x13)//Mode switch
	{
	    switch(buffer[1])
		{

                  case 0x02: Cruising_Flag = 2; return;//巡线
		  case 0x03: Cruising_Flag = 3; return;//Avoidance
		  case 0x04: Cruising_Flag = 4; return;//Radar obstacle avoidance
                  case 0x05: Cruising_Flag = 5; return;//The ultrasonic distance is displayed on the PC side
                  case 0x00: Cruising_Flag = 0; return;//Normal mode
		  default:Cruising_Flag = 0; return;//Normal mode
		}
	}
        else if(buffer[0]==0x05)
    {
        switch(buffer[1])   //
        {
            case 0x00:Open_Light(); return;
	    case 0x01:Close_Light(); return;
            default: return;
        }
    }
        else if(buffer[0]==0x40)//存储电机标志
	{
	   num=buffer[1];
	   EEPROM.write(0x10,num);
	}
}


```


### Read the serial command

```c

/*

*********************************************************************************************************
** Function name: Get_uartdata ()
** Function: Read the serial command
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void Get_uartdata(void)
{
    static int i;

    if (Serial.available() > 0) //Determines whether the serial buffer is loaded
    {
        serial_data = Serial.read();//Read the serial port
        if(rec_flag==0)
        {
            if(serial_data==0xff)
            {
                rec_flag = 1;
                i = 0;
               Costtime = 0;
            }
        }
        else
        {
            if(serial_data==0xff)
            {
                rec_flag = 0;
                if(i==3)
                {
                    Communication_Decode();
                }
                i = 0;
            }
            else
            {
                buffer[i]=serial_data;
                i++;
            }
        }
    }
}

```


### Serial timeout detection

```c

/*
*********************************************************************************************************
** Function name: UartTimeoutCheck ()
** Function: Serial timeout detection
** Entry parameters: none
** Export parameters: none
*********************************************************************************************************
*/
void UartTimeoutCheck(void)
{
    if(rec_flag == 1)
    {
       Costtime++;
      if(Costtime == 100000)
      {
           rec_flag = 0;
      }
    }
}

```

## Extra Features

### Temperature sensor Experiment

LM35 is a very common and easy to use temperature sensor components, components in the application of only need a LM35 components, only the use of an analog interface can be difficult is that the algorithm will read the analog value is converted to the actual temperature.
The required components are as follows.
1. Straight-through LM35 * 1
2. Breadboard * 1
3. Breadboard jumper * 1 bar

```c
//Geraldo Braho


int potPin = 0; // Define analog interface 0 Connect LM35 temperature sensor
void setup()
{
Serial.begin(9600);// Set the baud rate
}
void loop()
{
int val;// Define the variable
int dat;// Define the variable
val=analogRead(0);// Read the analog value of the sensor and assign it to val
dat=(125*val)>>8;// Temperature calculation formula
Serial.print("Tep:");// The original output shows the Tep string representing the temperature
Serial.print(dat);// Outputs the value of dat
Serial.println("C");// Output the C string as it is
delay(500);// Delay 0.5 seconds
}
```
