# fault_injection_ros2
Ros injection tool that subscribes to a topic and makes chenges to it according to preset behavior

Setting up procedure
As it stands this tool works with ROS2 Humble, planned to port on ROS Melodic in near future. 

mkdir -p ws/src
cd ws/src
git clone https://github.com/danilo-pejovic/fault_injection_ros2
cd ..
rosdep install --from-paths src --ignore-src -r -y
source /opt/ros/humble/setup.bash
MAKEFLAGS="-j1 -l1" colcon build
source install/setup.bash

Known limitations: 

- Works only with untimestamped messages
- Produces bit of lag when taking a lot of data
- Has to be manually turned on and take messages
