# Robot-Setup-Gripper-Integration-implementing-FollowJointTrajectory
ROS 2 setup for the Fanuc CRX-10iA robot including URDF/Xacro configuration, and a FollowJointTrajectory action server.  The setup supports joint trajectory execution with an attached Robotiq gripper  and visualization in RViz.

Features:-
-Fanuc CRX-10iA robot description using URDF/Xacro
-RViz visualization
-robot_state_publisher and joint_state_publisher
-FollowJointTrajectory action server
-Robotiq gripper integrated into the robot model
-ROS 2 compliant package structure

System Requirements:-
Operating System-Ubuntu 24.04 LTS
ROS 2 Distribution-ROS 2 Jazzy Jalisco
🐍 Python Requirements:-Python 3.12
ROS 2 Python packages:
-rclpy
-launch
-launch_ros
-xacro
-ament_index_python

Motion & action interfaces:
control_msgs
trajectory_msgs
builtin_interfaces
Visualization:
rviz2
joint_state_publisher
robot_state_publisher
Python is used for launch files and implementing the FollowJointTrajectory action server.

🧱 C++ Requirements
ROS 2 C++ libraries:
rclcpp
rclcpp_action
control_msgs
trajectory_msgs
sensor_msgs
Build tools:
ament_cmake
colcon
C++ is used for controller logic and trajectory execution.
🧰 Robotics & Control Tools
RViz2
ros2_control

File Structure:-
joint_trajectory_controllerfanuc_description/
├── config/
│   └── controllers.yaml
│
├── launch/
│   ├── control.launch.py
│   └── view_robot.launch.py
│
├── meshes/
│   └── lbr_iiwa_14_r820/
│       ├── collision/
│       │   ├── base_link.stl
│       │   ├── link_1.stl
│       │   └── ...
│       ├── visual/
│       │   ├── base_link.dae
│       │   ├── link_1.dae
│       │   └── ...
│
├── robotiq_2f_85/
│   ├── collision/
│   └── visual/
│
├── urdf/
│   ├── fanuc_crx10ia.urdf.xacro
│   └── robotiq_2f_85.urdf.xacro
│
├── CMakeLists.txt
└── package.xml
