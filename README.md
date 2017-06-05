# Installation of Turtlebot1:

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


## Installation Sources overview:
![](https://github.com/gareth-cross/rviz_satellite/blob/master/.screenshot.png)

