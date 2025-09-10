# Braccio Arm ROS2 Control

This repository contains ROS2 packages for controlling the Braccio robotic arm using MoveIt2.

## Packages

### braccio_description
- Contains URDF/Xacro files describing the Braccio arm robot
- STL mesh files for visualization
- Launch files for displaying the robot in RViz

### braccio_moveit_config
- MoveIt2 configuration package for the Braccio arm
- Contains motion planning, kinematics, and control configurations
- Launch files for running MoveIt2 with the Braccio arm

## Installation

1. Clone this repository into your ROS2 workspace:
```bash
cd ~/ros2_ws/src
git clone https://github.com/Kuan2003/braccio_arm_ros2_control.git
```

2. Install dependencies:
```bash
cd ~/ros2_ws
rosdep install --from-paths src --ignore-src -r -y
```

3. Build the packages:
```bash
colcon build --packages-select braccio_description braccio_moveit_config
```

4. Source the workspace:
```bash
source install/setup.bash
```

## Usage

### Launch MoveIt2 Demo
```bash
ros2 launch braccio_moveit_config demo.launch.py
```

### Display Robot in RViz
```bash
ros2 launch braccio_description display.launch.py
```

## Requirements

- ROS2 Humble or later
- MoveIt2
- RViz2

## License

This project is licensed under the Apache 2.0 License.
