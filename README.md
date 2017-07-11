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

![](https://github.com/CesMak/turtlebot1/blob/master/doc/installation.gif)

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

![Simulation video](https://www.youtube.com/watch?v=4-XWDSzjQCw)

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
[Roomba Doku](https://github.com/CesMak/roomba_521)

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

