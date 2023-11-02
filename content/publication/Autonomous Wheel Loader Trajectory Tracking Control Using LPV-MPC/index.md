---
title: "Autonomous Wheel Loader Trajectory Tracking Control Using LPV-MPC"
authors:
- Ruitao Song
- Zhixian Ye
- admin
- Tianyi He
- Liangjun Zhang
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2022-06-08T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2022-06-08T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "2022 American Control Conference"
publication_short: "ACC 2022"

abstract: In this paper, we present a systematic approach for high-performance and efficient trajectory tracking control of autonomous wheel loaders. With the nonlinear dynamic model of a wheel loader, nonlinear model predictive control (MPC) is used in offline trajectory planning to obtain a high-performance state-control trajectory while satisfying the state and control constraints. In tracking control, the nonlinear model is embedded into a Linear Parameter Varying (LPV) model and the LPV-MPC strategy is used to achieve fast online computation and good tracking performance. To demonstrate the effectiveness and the advantages of the LPV-MPC, we test and compare three model predictive control strategies in the high-fidelity simulation environment. With the planned trajectory, three tracking control strategies LPV-MPC, nonlinear MPC, and LTI-MPC are simulated and compared in the perspectives of computational burden and tracking performance. The LPV-MPC can achieve better performance than conventional LTI-MPC because more accurate nominal system dynamics are captured in the LPV model. In addition, LPV-MPC achieves slightly worse tracking performance but tremendously improved computational efficiency than nonlinear MPC.

# Summary. An optional shortened abstract.
summary: This paper outlines an approach for efficient trajectory tracking control of autonomous wheel loaders, employing nonlinear model predictive control for trajectory planning and a Linear Parameter Varying (LPV) model for enhanced computational efficiency, leading to better performance and reduced computational burden compared to conventional methods.

tags:
- All Publications
featured: false

# links:
# - name: ""
#   url: ""
url_pdf: ''
# url_code: 'https://github.com/wowchemy/wowchemy-hugo-themes'
# url_dataset: ''
# url_poster: ''
# url_project: ''
# url_slides: 'https://docs.google.com/presentation/d/17MiRPsFw8iized7m4K3Ad8J7KvCzSgLO/edit?usp=sharing&ouid=109493805994328969677&rtpof=true&sd=true'
# url_source: ''
# url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
image:
  caption: ''
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: ['Excavator Autonomous Driving']

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---
