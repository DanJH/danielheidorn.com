---
layout: post
title:  "Making a Smart AC"
date:   2026-08-28 12:00:00 -0400
categories: project personal
lastpost: "Game Design: Drift Star"
lastposthref: "./project/school/2022/02/06/game-design-proj-1-zelda.html"
nextpost: "Arduino Buttonbox for Sim- Racing, Flying, and more!"
nextposthref: "http://127.0.0.1:4000/project/personal/2026/06/22/arduino-buttonbox.html"
---

# __Work in Progress__

# Project

TODO add actual picture
![Picture of my AC and Arduino](/images/arduino.jpg)

This was another one of the hottest summers *yet*. Especially in the Midwest where the humidity from the Great Lakes and all the crops makes for a very humid summer.

I have a small apartment built back in the 70s. At that time, central AC was not too common, especially in small, two floor residental apartments. But my landlord at least put in an A/C from the pastt decade or so, the only issue is that I have little control over the actual temperature


# Hardware 

The hardware requirements are very minimal - not even requiring display unless desired. There are only a few key components:
- An Arduino board containing: 
    - WiFi
    - EEPROM
    - Obviously some digital and analog I/O
    - *I used an Uno R5 WiFi*
- BME680x sensor
    - Very common Bosch combo (temperature, air pressure, humidity and gas resistance) sensor 
    - *I used Adafruit BME680 breakout with SPI input*
- Actuator or IR
    - *TBD*

# Software 

## Air Sensor

I configured a library to hold all air sensor functionality including craetiung 

## Configuration 

I am planning on using this project for future uses and want to change calbirations on the fly (i.e. activation, hysterisis, etc.) so I decided to create an EEPROM layout to handle all these details with padding to grow.

At startupo