ROSMaster X3 Robotics Project



Robot_x3/
└── robot/
    └── src/
        └── ro/
            └── ro_description/       # main ROS2 package
                ├── launch/           # launch files to start the simulation
                │   └── sim.launch.py
                ├── urdf/             # robot model definitions (Xacro)
                │   ├── control/      # drive/control definitions (mecanum drive)
                │   ├── mech/         # mechanical parts (base, wheels)
                │   ├── robots/       # top-level robot assembly file
                │   └── sensors/      # sensor definitions (IMU, LiDAR, RGBD camera)
                ├── meshes/           # 3D visual/collision models (STL) for the robot and sensors
                └── worlds/           # Gazebo simulation world files
