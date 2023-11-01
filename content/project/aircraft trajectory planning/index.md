---
title: Aircraft Trajectory Planning with Multi-Objectives
summary: This project aims to research and develop a four-dimensional trajectory planning method for aircraft. The trajectory's constraint conditions include avoidance of no-fly zones and terrain obstacles, collision avoidance with surrounding moving aircraft, trajectory smoothness, and constraints on aircraft speed and acceleration. The optimization goals for the trajectory include minimizing the trajectory duration and maximizing comfort.
tags:
  - Reinforcement Learning
  - Trajectory Optimization
  - Simulation Environment
date: '2023-09-15T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

image:
  caption: ''
  focal_point: Smart

# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# # Slides (optional).
# #   Associate this project with Markdown slides.
# #   Simply enter your slide deck's filename without extension.
# #   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
# #   Otherwise, set `slides = ""`.
# slides: example
---

This project aims to research and develop a four-dimensional trajectory planning method for aircraft. The trajectory's constraint conditions include avoidance of no-fly zones and terrain obstacles, collision avoidance with surrounding moving aircraft, trajectory smoothness, and constraints on aircraft speed and acceleration. The optimization goals for the trajectory include minimizing the trajectory duration and maximizing comfort.

Due to the high-dimensional space complexity, directly optimizing to satisfy all constraints and enhance optimization goals in 4D space is highly challenging and time-consuming. Therefore, I decomposed the problem into 3 sequential path planning problems in 2D space.

First, a path planning is conducted in the horizontal plane (x-y coordinate system or latitude/longitude) from the given starting point to the destination. Using the RRT* algorithm, B-Spline smoothing, and STOMP optimizer, a relatively short and smooth path that avoids no-fly zones is found. This step ensures smoothness, avoidance of static obstacles (no-fly zones) in horizontal, satisfies horizontal turning radius, and achieves a relatively shorter duration (short path length) objective. The outputs of this step is a sequence of (x, y) coordinates.

Second, the total horizontal distance is calculated for the obtained (x, y) sequence of paths. A Cartesian coordinate system is established with the horizontal distance as the x-axis and altitude as the y-axis. Combining height-direction physical constraints such as terrain databases and adverse weather, the height information for each point on the x-axis is read, and obstacles representing height constraints are placed in the generated 2D space. Then, in this 2D space, a path is found using Dijkstra or A* algorithms, B-Spline smoothing, and the STOMP optimizer to avoid high mountains, tall buildings, clouds that should not be penetrated, and achieve a relatively short, smooth path that complies with climb and descent gradients. This step ensures smoothness, compliance with climb and descent constraints, and avoidance of static obstacles in the vertical direction (high mountains, tall buildings, clouds that should not be penetrated), enhancing the objective of relatively shorter duration (short path length). The output of this step is a sequence in (x, y, z) coordinates.

Third, and finally, a Cartesian coordinate system is established with time as the x-axis, and the total distance calculated for the obtained (x, y, z) sequence of paths as the y-axis. Based on the future trajectories of surrounding moving aircraft, an analysis is conducted to determine during which time intervals each aircraft will occupy which distance segments of the planned flight path. Using this analysis, rectangular obstacles can be marked in the coordinate system to obtain a distance-time graph. Moving obstacles in 3D space are represented as static obstacles in the 2D space represented by the distance-time graph. In this 2D space, path planning is performed to obtain velocity profile. The velocity profile must satisfy constraints on aircraft speed, acceleration, moving obstacle avoidance, and optimize objectives for shorter duration and higher comfort. The output of this step is the desired (x, y, z, t) sequence.

The research part of this project mainly focuses on the third step, which is velocity profile planning. Currently, I have implemented a baseline using a Breadth-First Search (BFS) algorithm. Simultaneously, I am researching the implementation using Deep Reinforcement Learning (DRL) algorithms. Compared to the baseline, it has advantages in terms of comfort and computational efficiency. Please check out the relevant publication for more details. At this moment, there is still significant room for improvement in terms of on-line computational efficiency, and this research is ongoing.