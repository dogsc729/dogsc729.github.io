---
layout: page
title: Bikesla
description: A embedded system device on a bicycle with STM32 IoT Node, connected to iPadOS App via Bluetooth.
img: assets/img/bikesla_background.jpg
github: https://github.com/dogsc729/Bikesla
importance: 1
category: Course Work
---
### Function
1. ***Speed-checking:*** Using the Hall sensor, with the magnets on the wheel, we can calculate the speed of the spinning of the wheel and inference the speed of the bicycle. The method of calculating the speed of the bicycle is:  
   $$ speed = {perimeter \over timediff} $$, where  
   perimeter = The perimeter of the wheel  
   timediff = The difference between two times the magnet passing through the Hall sensor.
2. ***Lock/Unlock:*** Using the App, we can unlock and lock the bicycle.
3. ***Bicycle-finding:***
   1. Using the App, pressing the Flash button to make the LED flicker. It is convenient for finding our bicycle at night.
   2. Press the Ring button to make the buzzer ring for 2 seconds, users can locate where the bicycle is much easily with this function.
   3. There is an additional drop down menu for users to adjust the lightness and the frequency of the LED.
4. ***Speeding detection:*** Based on the speed limit of Palm Avenue, we set the buzzer to ring for 2 seconds if the speed exceeds 20 km/hr.
5. ***Theft alarm:*** If the bicycle is locked, with the Hall sensor on the wheel, if the sensor detects that the wheel spins over some certain criteria, we regard it as abnormal usage, the buzzer will ring continuously.
6. ***Fall detection:*** Using the intrinsic triaxial accelerometer of the STM32 IoT Node, if we detect the z-axis acceleration is less than 500 m/s, we regard it as someone crashed, the buzzer will ring continuously, informing the people nearby.