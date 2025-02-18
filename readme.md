# Autonomous Explorer with TurtleBot3 and Slam ToolBox

## Installation

1. Install required packages
```bash
sudo apt install ros-humble-gazebo-ros-pkgs ros-humble-cartographer ros-humble-cartographer-ros ros-humble-navigation2 ros-humble-nav2-bringup ros-humble-rmw-cyclonedds-cpp ros-humble-slam-toolbox
```
2. Clone this Repo and Build using Colcon
3. Set Environment Variables
```bash
echo 'RMW_IMPLEMENTATION=rmw_cyclonedds_cpp' >> ~/.bashrc
echo 'export TURTLEBOT3_MODEL=burger' >> ~/.bashrc
source ~/.bashrc
```
4. Run with 3 terminals (must be in order)
```bash
ros2 launch slam_toolbox online_async_launch.py
```
```bash
ros2 launch turtlebot3_gazebo turtlebot3_world.launch.py
```
```bash
ros2 run autonomous_exploration control
```


## Prerequisite

- ROS2 (Humble)
- Colcon
- Slam Toolbox
- Turtlebot3 Package