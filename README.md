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
ros-kinetic-gazebo-ros-control
```

## Prerequisite:
Make sure that no workspace is sourced in your .bashrc file. Check it via:

`vim ~/.bashrc`

## Installation:

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

## Usage:
roslaunch turtlebot1_gazebo turtlebot1_empty_world.launch
roslaunch turtlebot1_gazebo turtlebot1_launch_all_robots.launch
roslaunch turtlebot1_gazebo turtlebot1_roomba_empty_world.launch
roslaunch turtlebot1_teleop teleop_key.launch

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

