# fault_injection_ros2
Ros injection tool that subscribes to a topic and makes chenges to it according to preset behavior

Setting up procedure

As it stands this tool works with ROS2 Humble, planned to port on ROS Melodic in near future. 

1. `mkdir -p ws/src` 
2. `cd ws/src`
3. `git clone https://github.com/danilo-pejovic/fault_injection_ros2`
4. `cd ..`
5. `rosdep install --from-paths src --ignore-src -r -y`
6. `source /opt/ros/humble/setup.bash`
7. `MAKEFLAGS="-j1 -l1" colcon build`
8. `source install/setup.bash`

After that one of the launch files like: 
 
  `ros2 launch fault_injection_ros2 launch_robot.launch.py`

Should have mux enabled by default with hardcorded priorities.

Known limitations: 

- Works only with untimestamped messages
- Produces bit of lag when taking a lot of data
- Has to be manually turned on and take messages
