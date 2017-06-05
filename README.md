# Installation of Turtlebot1 and Turtlebot2:

## Requirements:
Ubuntu 14.04.4 (or higher)
ROS-INDIGO     (or higher)
Gazebo7        (or higher)
Gazebo diff drive Plugin:
```
sudo apt-get install ros-indigo-gazebo7-*
sudo apt-get install ros-indigo-effort-controllers
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
turtle install simulation
turtle install roomba_521
turtle update_make
source setup.bash
turtle sim
```

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

