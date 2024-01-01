# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1: robomaster is a built-in modulle in python from which robot to be imported and import time
Step2: initialise the robot by giving initialize function for the robot to get commands from the user and move
Step3: give a value to the x axis so that the robot moves in the forward direction and for the robot to move towards left or right give a certain value to y
Step4: value assigned to z variable indicates the speed of the robot
Step5: set_led would determine the colors of the led lights on each side of the robot certain values
of red,green and blue to be given to get the color
STEP 6: give distance, speed and color change for the specified path and at the end give close to

## Program
```
from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera

    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)

    ep_chassis.move(x=2.9, y=0, z=0, xy_speed=1.3).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=255,effect="on")
    
    ep_chassis.move(x=0, y=0, z=80).wait_for_completed()
    ep_led.set_led(comp = "all",r=0,g=255,b=0,effect="on")

    ep_chassis.move(x=1.0, y=0, z=0, xy_speed=1.4).wait_for_completed()
    ep_led.set_led(comp = "all",r=255,g=255,b=0,effect="on…
```

## MobileRobot Movement Image:
![robo](./img/robomaster.png)

## MobileRobot Movement Video:
https://youtu.be/AfILpxM_i3w?si=ipA3zAPUk_KQ7MpP
## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
