# Installation of Turtlebot1 and Turtlebot2:

## Requirements:
Ubuntu 14.04.4 (or higher)
ROS-INDIGO     (or higher)
Gazebo7        (or higher)

Gazebo diff drive Plugin (for INDIGO):
```
sudo apt-get install ros-indigo-gazebo7-*
sudo apt-get install ros-indigo-effort-controllers
```

Gazebo diff drive Plugin (for KINETIC):
```
sudo apt-get install ros-kinetic-gazebo-ros-pkgs
sudo apt-get install ros-kinetic-gazebo-ros-control
```

## Prerequisite:
Make sure that no workspace is sourced in your .bashrc file. Check it via:

`vim ~/.bashrc`

## Installation:

[![Turtlebot1_Installation](https://img.youtube.com/vi/UkTMbMdC_Wg/0.jpg)](https://www.youtube.com/watch?v=UkTMbMdC_Wg)

```
cd ~
mkdir turtlebot1
cd turtlebot1
git clone https://github.com/CesMak/turtlebot_install .
./install.sh
source setup.bash
turtle install simulation (optional)
turtle install roomba_521 (optional)
turtle update_make
source setup.bash
turtle switch_gazebo [required under indigo: switch to gazebo version7]
turtle sim  (requires simulation to be installed)
```

## Simulation:

[![Turtlebot1_Simulation](https://img.youtube.com/vi/XWDSzjQCw/2.jpg)](https://www.youtube.com/watch?v=4-XWDSzjQCw)

1. Install it via:
```
turtle install simulation
turtle update_make
```

2. Launch the Simulation via:

| Command | Explanation |
| ------------- | ------------- |
| roslaunch turtlebot1_gazebo turtlebot1.launch| |
| roslaunch turtlebot1_gazebo turtlebot1_default.launch||
| roslaunch turtlebot1_gazebo turtlebot1_launch_all_robots.launch||
| roslaunch turtlebot1_gazebo turtlebot1_full.launch|rviz, gazebo with teleop in tb1 world|
| roslaunch turtlebot1_teleop teleop_key.launch||


## Installation of the Roomba_521 package:

[![PD_Controller](https://img.youtube.com/vi/pNLwUF0T-Nc/0.jpg)](https://www.youtube.com/watch?v=pNLwUF0T-Nc)

1. Install the Roomba package:
```
turtle install  roomba_521
turtle update_make
```

2. Give rights to the USB:
```
sudo usermod -a -G dialout $USER
```

3. Logut and login for permission to take effect
4. Connect your pc via usb with the open interface of the roomba
5. Start the roomba (click the power button) make sure the power light glows green (if not charge your roomba first)
6. Start the node:
```
roslaunch r_driver r_521.launch
```

7. Subscribe / publish Topics:

| Command | Explanation |
| ----------------- | ------ |
| rostopic pub mySong std_msgs/Bool true| |
| rostopic pub /sound std_msgs/UInt8MultiArray '{data:[70,102]}'||
| rostopic pub -r 10 /cmd_vel geometry_msgs/Twist '{linear: {x: 0.1, y: 0.0, z: 0.0}, angular: {x: 0.0,y: 0.0,z: 0.0}}'||
| rostopic echo bumper||
| rostopic pub /dock_led std_msgs/Bool "data: false" |sets dock light to green|
| rostopic pub /power_led std_msgs/UInt8MultiArray "data: '[12,100]'"   |sets the power_led to a specific color|
| rostopic pub /turtle1/PositionCommand geometry_msgs/Pose2D "x: 1.5 y: 0.0 theta: 10.0" |if controller node is started in r_521.launch - you can drive to a determined position.|

See also: [Roomba Doku](https://github.com/CesMak/roomba_521)



## Gazebo simulation:
![](https://github.com/CesMak/turtlebot1/blob/master/doc/gazebo_all_robots.png)

## Installation Sources overview:
![](https://github.com/CesMak/turtlebot1/blob/master/doc/Installation_Overview.png)


### Github initialization:

```
git init
git add --a
git commit -m "name"
git remote add HTTPS-rep
git push -u origin master
```

