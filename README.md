RoboFusion 🚗

RoboFusion is a ROS2-based mobile robot simulation project that integrates LiDAR and camera sensors using URDF/Xacro, and runs in Gazebo.

Features
- Modular robot design using URDF/Xacro  
- LiDAR sensor integration  
- Camera sensor integration  
- Differential drive system (Gazebo plugin)  
- Gazebo simulation environment  
- RViz visualization support  

Technologies
- ROS2 (Humble)
- Gazebo
- RViz
- URDF / Xacro

Project Structure
RoboFusion/
├── my_robot_bringup/           # Launch files and simulation startup
├── my_robot_description/       # Robot model (URDF/Xacro, sensors)
└── simple_robot_description/   # Basic example / test package

Run the Project
cd ~/ros2_ws_1
source /opt/ros/$ROS_DISTRO/setup.bash
colcon build --packages-select my_robot_bringup my_robot_description
source install/setup.bash
unset GTK_PATH
ros2 launch my_robot_bringup my_robot_gazebo.launch.xml

Description
This project demonstrates how to build a mobile robot simulation pipeline in ROS2, including:
- Robot modeling with URDF/Xacro  
- Sensor integration (LiDAR and camera)  
- Simulation setup in Gazebo  
- Modular package structure for scalability  

Future Work
- EKF-based localization (IMU + odometry fusion)  
- Advanced sensor fusion  
- Autonomous navigation using Nav2  

Notes
- my_robot_description contains the main robot model and sensor definitions  
- my_robot_bringup is responsible for launching the simulation  
- simple_robot_description is included as a basic reference package  
