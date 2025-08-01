PPO_GRU_Delta_LiDAR 🛸
PPO-GRU + Delta-LiDAR for UAV Navigation
Enhanced Memory-Augmented Deep Reinforcement Learning for UAV Navigation in Partially Observable Environments using PPO + GRU and ΔLiDAR

🧠 Summary
This project implements autonomous drone navigation in a 3D simulated environment using Proximal Policy Optimization (PPO) combined with Gated Recurrent Units (GRU) and ΔLiDAR data (LiDAR frame differencing). The agent learns to navigate through static and dynamic obstacles toward a predefined target using only LiDAR information and internal memory (GRU) for better temporal awareness.

📦 Package Name
drone_ppogru_delta_nav

🚀 Features
✅ PPO + GRU-based Deep Reinforcement Learning agent

✅ ΔLiDAR input for capturing motion over time

✅ Memory-augmented navigation in partially observable 3D environments

✅ Full integration with ROS Noetic, Gazebo 11, PX4 SITL, and MAVROS

✅ Collision reset, reward shaping, goal-checking

✅ Generalization to unseen dynamic environments

🧭 System Overview
Component	Description
Simulator	Gazebo 11
Flight Controller	PX4 Autopilot (Software-In-The-Loop)
Middleware	MAVROS + ROS Noetic
DRL Algorithm	PPO + GRU (via Stable-Baselines3)
Sensor	720° 2D LiDAR (with frame differencing Δ)
Input Topic	/scan


📂 Folder Structure
bash
Copy
drone_ppogru_delta_nav/
├── launch/         # Simulation launch files
├── models/         # Drone + LiDAR robot model
├── worlds/         # Custom Gazebo world with dynamic obstacles
├── Media/          # Screenshots and demo videos
├── CMakeLists.txt
├── package.xml
└── README.md



⚙️ Dependencies
Make sure you have the following installed:

ROS & Simulator

ROS Noetic

Gazebo 11

PX4 Autopilot (SITL)

MAVROS & mavros_extras



Python packages:
pip install stable-baselines3[extra] torch gymnasium

Also install system dependencies:
sudo apt install ros-noetic-mavros ros-noetic-mavros-extras


🧠 Training the Agent
To start training, run:

rosrun drone_ppogru_delta_nav train_gru_recurrentppo.py

The drone will:

Arm and take off in Gazebo

Switch to OFFBOARD mode

Receive ΔLiDAR input

Learn via PPO to reach the goal while avoiding collisions


📊 Evaluation Scenarios
✅ Performance in Training Environment

🧩 Generalization to Unseen Layouts

🔄 Robustness in Dynamic Obstacle Scenarios

Watch demo videos:
https://github.com/Maryamallawi96/PPO_GRU_Delta_LiDAR/blob/main/Media2/Test%20(front%20view).MOV
https://github.com/Maryamallawi96/PPO_GRU_Delta_LiDAR/blob/main/Media2/Test(%20Top%20view).MOV
https://github.com/Maryamallawi96/PPO_GRU_Delta_LiDAR/blob/main/Media2/Training%20Environments.png
https://github.com/Maryamallawi96/PPO_GRU_Delta_LiDAR/blob/main/Media2/unseen%20env.tunnel.png


👩‍💻 Author
Maryam Allawi
✉️ Email: pgs.maryam.allawi@uobasrah.edu.iq
🌐 GitHub: Maryamallawi96


