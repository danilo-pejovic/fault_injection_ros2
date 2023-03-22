# fault_injection_ros2
Ros injection tool that subscribes to a topic and makes chenges to it according to preset behavior

Setting up procedure
As it stands this tool works with ROS2 Humble, planned to port on ROS Melodic in near future. 

mkdir -p ws/src

1. `cd ws/src`
2. `git clone https://github.com/danilo-pejovic/fault_injection_ros2`
3. `cd ..`
4. `rosdep install --from-paths src --ignore-src -r -y`
5. `source /opt/ros/humble/setup.bash`
6. `MAKEFLAGS="-j1 -l1" colcon build`
7. `source install/setup.bash`

Known limitations: 

- Works only with untimestamped messages
- Produces bit of lag when taking a lot of data
- Has to be manually turned on and take messages
