---
title: Wheeled Robot Movement Modeling and Control
summary: This project focuses on the modeling and control of wheeled robots, including three sub-projects I have completed at different times. They are autonomous taxiing of aircraft on the runway, crawler chassis locomotion for excavators, and a robotic guide dog for vision impaired people.
tags:
  - Wheeled Robot
  - Trajectory Optimization
  - Simulation Environment
  - Robot Platform
date: '2023-01-24T00:00:00Z'

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

This project focuses on the modeling and control of wheeled robots, including three sub-projects I have completed at different times. They are autonomous taxiing of aircraft on the runway, crawler chassis locomotion for excavators, and a robotic guide dog for vision impaired people.

The core of this task involves deriving the kinematics model for wheeled robots. For aircraft taxiing, I chose a model similar to that of autonomous cars. For excavator move base, I utilized a differential drive model for dual wheels. In the case of the robotic guide dog, I derived a joint model for the robot and the visually impaired person, and published relevant [articles](https://lywang1016.github.io/publication/navdog-robotic-navigation-guide-dog-via-model-predictive-control-and-human-robot-modeling/) on the subject.

The control algorithm used for all three sub-projects is Model Predictive Control (MPC). And the solve used is a QP solver called [OSQP](https://osqp.org/).

From experiments, using RTK for localization, the position error is centimeter level for both aircraft taxiing and excavator base moving. This is very impressive results since the aircraft and the excavator‘s size is at 10 meters level. The robotic guide dog is proved collision free for both human and robot.