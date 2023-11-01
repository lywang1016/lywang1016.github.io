---
title: Aircraft Trajectory Planning with Multi-Objectives
summary: This project aims to research and develop a four-dimensional trajectory planning method for aircraft. The trajectory's constraint conditions include avoidance of no-fly zones and terrain obstacles, collision avoidance with surrounding moving aircraft, trajectory smoothness, and constraints on aircraft capabilities include speed and acceleration. The optimization goals for the trajectory include minimizing the trajectory duration and maximizing comfort.
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
url_slides: 'https://docs.google.com/presentation/d/1L-S7cjwy69E-vG037AO63rI6FB3Vih9L/edit?usp=sharing&ouid=109493805994328969677&rtpof=true&sd=true'
url_video: ''

# # Slides (optional).
# #   Associate this project with Markdown slides.
# #   Simply enter your slide deck's filename without extension.
# #   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
# #   Otherwise, set `slides = ""`.
# slides: example
---

This project aims to research and develop a four-dimensional trajectory planning method for aircraft. The trajectory's constraint conditions include avoidance of no-fly zones and terrain obstacles, collision avoidance with surrounding moving aircraft, trajectory smoothness, and constraints on aircraft capabilities include speed and acceleration. The optimization goals for the trajectory include minimizing the trajectory duration and maximizing comfort.

Due to the high-dimensional space complexity, directly optimizing to satisfy all constraints and enhance optimization goals in 4D space is highly challenging and time-consuming. Therefore, I decomposed the problem into 3 sequential path planning problems in 2D space. Initially, a path is planned in the horizontal plane using the RRT* algorithm and B-Spline smoothing to ensure a smooth and obstacle-free path, addressing static obstacles (no-fly zones) in the horizontal direction. The second step calculates the total horizontal distance and considers height constraints to create a 2D space with obstacles, ensuring a smooth and obstacle-free path that complies with climb and descent constraints. The third step establishes a distance-time graph, marking rectangular obstacles based on the future trajectories of surrounding aircraft, translating 3D moving obstacles into 2D static obstacles. Here, a velocity profile is generated that adheres to speed, acceleration, and moving obstacle avoidance constraints while optimizing for shorter duration and higher comfort. For more details, please checkout the [PDF](https://lywang1016.github.io/project/aircraft-trajectory-planning/aircraft%20trajectory%20planning.pdf) file.

The research part of this project focuses on the third step, which is velocity profile planning. Currently, I have implemented a baseline using a Breadth-First Search (BFS) algorithm. Simultaneously, I am researching the implementation using Deep Reinforcement Learning (DRL) algorithms. Compared to the baseline, it has advantages in terms of comfort and computational efficiency. Please check out my [relevant publication](https://lywang1016.github.io/publication/velocity-planning-with-multi-objectives-in-displacement-time-graphs-using-deep-reinforcement-learning/) for more details. At this moment, there is still significant room for improvement in terms of on-line computational efficiency, and this research is ongoing.

I conducted all aspects of this project independently, including conceptualizing and designing the experiments, developing the [simulation environment](https://docs.google.com/presentation/d/1L-S7cjwy69E-vG037AO63rI6FB3Vih9L/edit?usp=sharing&ouid=109493805994328969677&rtpof=true&sd=true) and generating data, implementing the algorithms, and writing the research paper.