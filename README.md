1. installation and copying the files


0) dependent packages

sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python ros-kinetic-rosserial-server ros-kinetic-rosserial-client ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro ros-kinetic-compressed-image-transport ros-kinetic-rqt-image-view ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers

1) turtlebot3 & turtlebot3_msgs

git clone https://github.com/ROBOTIS-GIT/turtlebot3.git
git clone https://github.com/ROBOTIS-GIT/turtlebot3_msgs.git

2) turtlebot3_simulation

git clone https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

3) gazebo_ros_control

sudo apt-get install ros-kinetic-gazebo-ros-pkgs ros-kinetic-gazebo-ros-control

4) copy files in world_files folder to ~/catkin_ws/turtlebot3_simulation/turtlebot3_gazebo/worlds folder

-> change the directories in map_final_3_jh.world file

5) copy files in launch_files to ~/catkin_ws/turtlebot3_simulation/turtlebot3_gazebo/launch folder

6) copy files in model_files folder to ~/model_editor_models folder (if it does not exist, make one)

7) copy junny_control folder to catkin_ws/src folder

8) copy files in urdf_files/without_actuator folder to ~/catkin_ws/turtlebot3/turtlebot3_description/urdf folder 
-> if you want to try ones with actuator mode on, copy files from urdf_files/with_actuator folder.

9) copy files in teleop_files to ~/catkin_ws/turtlebot3/turtlebot3_teleop/nodes folder.



2. running the code

1) roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch

2) roslaunch turtlebot3_gazebo test.launch

3) roslaunch junny_control junny_control_without_actuator.launch

3*) roslaunch junny_control junny_control_with_actuator.launch

4) rosrun turtlebot3_teleop turtlebot3_teleop_key



->              q     w     e
                a     s     d
                      x

w: linear velocity increase
a: angular velocity increase to clockwise
s: stop
d: angular velocity increase to counter-clockwise
x: linear velocity decrease
q: actuator actuation
e: actuator return to origin position

