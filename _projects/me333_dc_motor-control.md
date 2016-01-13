---
layout: project
title: DC Motor Control 
date: March 18, 2015
image: https://cloud.githubusercontent.com/assets/4311090/12085752/ce89838e-b288-11e5-8054-10e7322a7878.png
---
##Overview
This was the final project of the Introduction to Mechatronics class. The goals were to become familiar with writing code library of functions for a PIC32 and using it to control a bar’s position on the end of a motor and  get the bar to follow a certain trajectory.
![function library](https://cloud.githubusercontent.com/assets/4311090/12290066/1dcd557e-b9a5-11e5-82a6-ac1f1754b7da.png)

The bar’s angular position tracked a reference signal by using a PID controller.

Control of the DC motor occurred through MATLAB, in which serial communication sent commands to the PIC32 to directly control the DC motor. Hardware used was quadrature decoder and counter chip, current sensor, H-bridge, as well as resistors and capacitors. We built up a library of functions before having a bar attached to the end of the motor follow a reference trajectory.

### Circuit Schematics
![schematics](https://cloud.githubusercontent.com/assets/4311090/12287334/6c4feca2-b991-11e5-8714-e2aa83206b51.png)

###current tuning with optimized gains 
![image](https://cloud.githubusercontent.com/assets/4311090/12290969/2529f584-b9aa-11e5-9634-12020f8f03c6.png)

### 180 degree sine curve trajectory
![180_degree_trajectory](https://cloud.githubusercontent.com/assets/4311090/12291342/49127e7e-b9ac-11e5-9a4c-ad7d84791d0f.png)


[Here's the link to the github repository](https://github.com/ChuChuIgbokwe/me333_final_project)
