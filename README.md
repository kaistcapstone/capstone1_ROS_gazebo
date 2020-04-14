### 1. installation and build the file

install dependent packages
```
sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python ros-kinetic-rosserial-server ros-kinetic-rosserial-client ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro ros-kinetic-compressed-image-transport ros-kinetic-rqt-image-view ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers

```

install gazebo_ros_control
```
sudo apt-get install ros-kinetic-gazebo-ros-pkgs ros-kinetic-gazebo-ros-control
```
down load source file
```
git clone https://github.com/kaistcapstone/capstone1_ROS_gazebo
```
build the code
```
cd ~/capstone1_ROS_gazebo
catkin_make
```


### 2. running the code

map open
```
roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch
```
swapn the robot
```
 roslaunch turtlebot3_gazebo test.launch
```
launch the controller_manager
```
roslaunch junny_control junny_control_without_actuator.launch
```
or
```
roslaunch junny_control junny_control_with_actuator.launch
```
steer the robot
```
rosrun turtlebot3_teleop turtlebot3_teleop_key
```

```
->              q     w     e
                a     s     d
                      x
```
w: linear velocity increase
a: angular velocity increase to clockwise
s: stop
d: angular velocity increase to counter-clockwise
x: linear velocity decrease
q: actuator actuation
e: actuator return to origin position

