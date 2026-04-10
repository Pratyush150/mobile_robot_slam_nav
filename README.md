# Mobile Robot with SLAM and Navigation (ROS2)

This project is a complete implementation of a mobile robot using ROS2, focused on simulation, localization, mapping, and autonomous navigation.

The goal of this project is to understand how a robot can move in an unknown environment, create a map, and then use that map to navigate safely to a target location.

---

## 🚀 What this project does

* Simulates a mobile robot in Gazebo
* Builds the robot model using URDF
* Uses SLAM to generate a map of the environment
* Applies localization to estimate robot position
* Implements Nav2 stack for autonomous navigation
* Includes a basic perception module (ball tracking)

---

## 📁 Project Structure

```
mobile_robot_slam_nav/
│── articubot_one/      # Main robot package (URDF, launch, configs)
│── ball_tracker/       # Simple perception module
│── CMakeLists.txt
│── package.xml
```

---

## ⚙️ Tech Stack

* ROS2 (Humble / Iron)
* Gazebo (Simulation)
* RViz (Visualization)
* Nav2 (Navigation stack)
* SLAM Toolbox / Cartographer (Mapping)
* OpenCV (for perception tasks)

---

## 🧠 How it works (Simple Flow)

1. The robot is defined using URDF
2. It is spawned inside a Gazebo simulation
3. Sensors (like LiDAR/camera) generate data
4. SLAM algorithm creates a map from sensor data
5. Localization estimates the robot’s position on the map
6. Nav2 plans a path and moves the robot to the goal

---

## ▶️ How to Run

### 1. Clone the repository

```bash
git clone https://github.com/Pratyush150/mobile_robot_slam_nav.git
cd mobile_robot_slam_nav
```

### 2. Build the workspace

```bash
colcon build
```

### 3. Source the workspace

```bash
source install/setup.bash
```

### 4. Launch simulation

```bash
ros2 launch articubot_one <your_launch_file>.launch.py
```

### 5. Run SLAM / Navigation

(Depends on your setup)

```bash
ros2 launch <slam_package> <slam_launch>.py
ros2 launch nav2_bringup navigation_launch.py
```

---

## 🎯 Future Improvements

* Add GPS-denied localization using vision
* Improve perception using deep learning models
* Integrate real robot hardware
* Optimize for edge devices (Jetson Nano)

---

## 👨‍💻 About this project

This project is part of my learning and development in robotics, focusing on real-world applications like autonomous navigation and delivery systems.

It helped me understand how different components like simulation, mapping, localization, and planning work together in a complete robotics pipeline.

---
