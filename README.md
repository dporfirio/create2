# Create2 Robot Control

## Installation

If you have not done so already, create a ROS workspace called `unity_ros_ws`. Then do the following:

```
cd unity_ros_ws/src
git clone -b noetic-devel https://github.com/tu-darmstadt-ros-pkg/hector_slam.git
git clone https://github.com/Unity-Technologies/ROS-TCP-Endpoint.git
git clone https://github.com/dporfirio/create2.git
```

Open `robot_ctrl/config/params.yaml` and set the `ROS_IP` param to the local IP of your computer (i.e., `192.168.0.---`).


## Running

```
roslaunch robot_ctrl ctrl.launch
```
