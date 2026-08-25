# Robot_x3

A ROS2 (Jazzy) package for the ROSMaster X3 robot — includes the robot's Xacro/URDF models, meshes, and a Gazebo simulation setup.

## Structure

```
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
```

**What each folder is for:**

- **`ro_description/`** — the ROS2 package itself, containing everything needed to describe and simulate the robot.
- **`launch/`** — has `sim.launch.py`, the entry point that starts the robot in Gazebo.
- **`urdf/`** — the robot's kinematic/physical description, split by purpose: control logic, mechanical structure, sensors, and the final assembled robot.
- **`meshes/`** — the actual 3D shapes (STL files) used to render the robot and its sensors (camera, LiDAR) in simulation.
- **`worlds/`** — the simulated environment the robot is placed into.

<img width="1687" height="1044" alt="Robot in Gazebo simulation" src="https://github.com/user-attachments/assets/f451825e-6185-424d-97c6-42ce5cf0dfe5" />
<img width="1678" height="1047" alt="RViz visualization of robot model" src="https://github.com/user-attachments/assets/683f18fc-6d16-411f-b299-9145c7861ba3" />

## Setup & Run
 
```bash
sudo apt update
sudo apt install ros-jazzy-ros-gz-sim ros-jazzy-ros-gz-bridge ros-jazzy-urdf-tutorial ros-jazzy-xacro
 
colcon build --packages-select ro_description
source install/setup.bash
 
ros2 launch ro_description sim.launch.py
```
 
## Usage
 
Visualize just the robot model (without full Gazebo sim):
 
```bash
ros2 launch urdf_tutorial display.launch.py model:=<path-to>/ro_description/urdf/robots/rosmaster_x3.urdf.xacro
```
 
Drive the robot with your keyboard:
 
```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```
