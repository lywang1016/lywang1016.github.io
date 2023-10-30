---
title: Tic Tac Toe
summary: This is a personal project. Aim to learn and apply Tabular Reinforcement Learning on the game of Tic Tac Toe.
tags:
  - Reinforcement Learning
  - Just for Fun
date: '2022-03-24T00:00:00Z'

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
url_code: 'https://github.com/lywang1016/RL-for-TicTacToe'
url_pdf: ''
url_slides: ''
url_video: 'https://youtu.be/KqAJFFEyUSM'

# # Slides (optional).
# #   Associate this project with Markdown slides.
# #   Simply enter your slide deck's filename without extension.
# #   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
# #   Otherwise, set `slides = ""`.
# slides: example
---

This project is a personal endeavor aimed at learning and applying Tabular Reinforcement Learning. The chosen experimental domain is the game of Tic Tac Toe. 

I have implemented three algorithms in Python: SARSA, Q-learning, and double Q-learning. Additionally, I've created a game framework that supports human vs. human, human vs. AI, and AI vs. AI gameplay.

Due to the limited number of states in the Tic Tac Toe game, Tabular Reinforcement Learning is sufficient for implementation. I've trained both the first player and the second player as two separate agents, and they do not share values between them.

Through experiments, regardless of the algorithm used (SARSA, Q-learning, and double Q-learning), the agents have been trained to the point where they can never lose. The best result for human player is tie, and if human make any mistake the AI will win.

You are very welcomed to click the [Code](https://github.com/lywang1016/RL-for-TicTacToe) link to github, and deploy on your own computer to play. Also please checkout the [Video](https://youtu.be/KqAJFFEyUSM) for your reference.