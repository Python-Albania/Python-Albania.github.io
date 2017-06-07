---
layout: post
title: RoboSmart
author: Geraldo Braho
tags: 		
subtitle: My senior design project
category: project1
visualworkflow: true
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

![Description](/img/_logo.png)


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
