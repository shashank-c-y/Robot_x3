ROSMaster X3 Robotics Project
This repository serves as the central codebase for the ROSMaster X3 robotics project, integrating sensor fusion, 
mecanum drive control, and Gazebo simulation capabilitie

Project Overview
This project provides the complete URDF/Xacro models and launch files required to simulate and operate the ROSMaster X3 platform.
It is designed to be a modular foundation for navigation, mapping, and autonomous control development.


   robot/
        ├── README.md
        └── src/
            └── ro/
                ├── read.me
                └── ro_description/
                    ├── readme.md
                    ├── CMakeLists.txt
                    ├── LICENSE
                    ├── package.xml
                    ├── launch/
                    │   └── sim.launch.py
                    ├── meshes/
                    │   ├── intel_realsense/
                    │   │   └── visual/
                    │   │       └── d435.stl
                    │   ├── rosmaster_x3/
                    │   │   └── visual/
                    │   │       ├── back_left_wheel_X3.STL
                    │   │       ├── back_right_wheel_X3.STL
                    │   │       ├── base_link_X3.STL
                    │   │       ├── camera_link.STL
                    │   │       ├── front_left_wheel_X3.STL
                    │   │       ├── front_right_wheel_X3.STL
                    │   │       └── laser_link.STL
                    │   └── rplidar/
                    │       └── rplidar_s2.stl
                    ├── urdf/
                    │   ├── control/
                    │   │   └── mecanum_drive.urdf.xacro
                    │   ├── mech/
                    │   │   ├── mecanum_wheel.urdf.xacro
                    │   │   └── rosmaster_x3_base.urdf.xacro
                    │   ├── robots/
                    │   │   └── rosmaster_x3.urdf.xacro
                    │   └── sensors/
                    │       ├── imu.urdf.xacro
                    │       ├── lidar.urdf.xacro
                    │       └── rgbd_camera.urdf.xacro
                    └── worlds/
                        ├── empty.sdf
                        ├── office.sdf
                        └── test_world.sdf
