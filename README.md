# Create2 Robot Control

## Installation

The following must be installed:

```
sudo apt-get install python3-catkin-tools
```

If you have not done so already, create a ROS workspace called `unity_ros_ws`. Then do the following:

```
cd unity_ros_ws/src
git clone -b noetic-devel https://github.com/tu-darmstadt-ros-pkg/hector_slam.git
git clone https://github.com/Unity-Technologies/ROS-TCP-Endpoint.git
git clone -b melodic https://github.com/AutonomyLab/create_robot.git
git clone https://github.com/AutonomyLab/libcreate.git
git clone https://github.com/dporfirio/create2.git
git clone https://github.com/dporfirio/TabulaSynthesizer.git
git clone https://github.com/ros-drivers/joystick_drivers.git

cd ../
catkin build  # do not run catkin make
```

Note: `catkin_make` will not work in this workspace. You must run `catkin build`.

Lastly, open `robot_ctrl/config/params.yaml` and set the `ROS_IP` param to the local IP of your computer (i.e., `192.168.0.---`).


## Running

```
roslaunch mapping_bringup slam.launch
roslaunch robot_ctrl ctrl.launch
```
