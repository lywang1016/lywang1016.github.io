---
title: "A K Nearest neighborhood-based wind estimation for rotary-wing VTOL UAVs"
authors:
- admin
- Gaurav Misra
- Xiaoli Bai
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2019-06-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2019-06-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "*Drones"
publication_short: ""

abstract: Wind speed estimation for rotary-wing vertical take-off and landing (VTOL) UAVs is challenging due to the low accuracy of airspeed sensors, which can be severely affected by the rotor’s down-wash effect. Unlike traditional aerodynamic modeling solutions, in this paper, we present a K Nearest Neighborhood learning-based method which does not require the details of the aerodynamic information. The proposed method includes two stages, an off-line training stage and an on-line wind estimation stage. Only flight data is used for the on-line estimation stage, without direct airspeed measurements. We use Parrot AR.Drone as the testing quadrotor, and a commercial fan is used to generate wind disturbance. Experimental results demonstrate the accuracy and robustness of the developed wind estimation algorithms under hovering conditions.

# Summary. An optional shortened abstract.
summary: This paper presents a K Nearest Neighborhood learning-based method for wind speed estimation in vertical take-off and landing UAVs. It offers robust and accurate wind estimation without the need for detailed aerodynamic information, addressing challenges posed by rotor down-wash effects.

tags:
- Source Themes
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
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/jdD8gXaTZsc)'
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---
