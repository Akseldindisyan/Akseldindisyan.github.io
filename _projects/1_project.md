---
layout: page
title: How can a robot place an item on a cluttered desk 
description: Spatial optimization and trajectory planning for a Baxter service robot.
img: assets/img/BaxterRobot.jpg
importance: 1
category: Academic Research
---

**TL;DR:** Developed and implemented spatial optimization and trajectory planning algorithms to enable a Baxter service robot to autonomously evaluate and place items on a cluttered 2D surface.

![Baxter Robot performing pick-and-place](/assets/img/BaxterRobot.jpg) 

### Technologies & Methodology
* **Hardware:** Baxter Service Robot (Dual 7-DOF arms).
* **Software & Frameworks:** ROS (Kinetic/Noetic), MoveIt! trajectory planning, Gazebo 11 simulation environment, Python.
* **Algorithms Investigated:** Greedy Packing, AABB (Axis-Aligned Bounding Box) Trees, and Gridization-Based Hierarchical Placement.

### Key Contributions & Results
* Transformed the physical desk environment into a 2D coordinate system and approximated items as rectangle bounding boxes to efficiently frame the task as a packing problem.
* Engineered a recursive blank space detection algorithm and a greedy packing algorithm that selects optimal placements using Candidate Corner-Occupying Actions (CCOA) to minimize computational overhead.
* Successfully planned and executed collision-free pick-and-place kinematics in both Gazebo simulations and on the physical Baxter hardware using MoveIt!.
