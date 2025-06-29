# turtlebot3
Project: Autonomous turtlebot3
# TurtleBot3 Autonomous Navigation with ROS 2

This project implements autonomous navigation for a TurtleBot3 in simulation using ROS 2 and Cartographer.  
The robot explores, maps the environment, and navigates from a given start pose to a goal pose while dynamically avoiding obstacles.

---

## ✅ **Project Overview**

- **Platform:** TurtleBot3 Burger
- **Simulation:** Gazebo
- **Mapping:** Cartographer SLAM
- **Path planning & control:** ROS 2 Navigation Stack (Nav2)
- **Local planner:** DWB local planner
- **Trajectory visualization:** Global and local paths in RViz
- **Costmaps:** Local & global costmaps configured for obstacle avoidance

---

## ⚙️ **Steps performed**

1. Installed **ROS 2** on Ubuntu  
2. Installed **Gazebo** simulator  
3. Setup TurtleBot3 with necessary packages and model files  
4. Installed and configured **Cartographer**  
5. Created **two occupancy grid maps** using SLAM  
6. Tweaked `tb3_nav_params.yaml` to adjust:
   - Costmap parameters (resolution, robot radius, plugins)
   - Inflation layer and obstacle layer settings
   - Sampling & obstacle range for better obstacle avoidance
7. Created launch file to:
   - Start map server
   - Start planner server
   - Launch costmaps and controller server
   - Enable autonomous navigation from "2D Pose Estimate" to "Goal" in RViz
8. Verified continuous generation of:
   - Global path (from start to goal)
   - Local path (short-term trajectory following)
9. Confirmed robot navigates to goal while dynamically avoiding obstacles using:
   - **DWB local planner** for real-time trajectory control
   - Local and global costmaps to evaluate obstacle proximity


---

## 📍 **How to run**

ros2 launch autonomous_tb3 navigation.launch.py
In RViz:
◦ Set "2D Pose Estimate" to initialize pose
◦ Set "2D Nav Goal" to define target goal
◦ Watch robot navigate while dynamically avoiding obstacles

🛠 Tools & Packages Used
    • ROS 2 (Humble)
    • Gazebo simulator
    • Nav2 stack (planner_server, controller_server, map_server)
    • Cartographer
    • RViz

✏️ Author
    • Anubhav Kumar
