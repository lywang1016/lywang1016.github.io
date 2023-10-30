---
title: "Real-time filtering method for low-cost MEMS gyroscope"
authors:
- admin
- Kunpeng Zhai
- Wentao He
- Chengyan Ma
# author_notes:
# - "Equal contribution"
# - "Equal contribution"
date: "2015-04-01T00:00:00Z"
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: "2015-04-01T00:00:00Z"

# Publication type.
# Accepts a single type but formatted as a YAML list (for Hugo requirements).
# Enter a publication type from the CSL standard.
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Application of Electronic Technique"
publication_short: ""

abstract: In this work, we aimed to find a general method suitable for coping in real time with stochastic error  which  is  a main  feature of most of low  cost Micro Electro Mechanical Systems(MEMS) gyroscope. First of all, Allan variance was utilized to analyze the drift error of MEMS gyroscope. According to its characteristic, we  designed  a  real  time  average  estimate  algorithm  to  eliminate  gross  error.  Then,  the  least  square  algorithm was  applied  to  extrapolate  the  predicted  value  of  next  step  through  the  previous  output  values.  Based  on  the aforementioned works, we finally worked out a Kalman filter which efficiently reduces angle random walk and variance of output. This method can be applied to most of low cost MEMS gyros cope because the least square algorithm avoided the problem of being difficult to accurately model drift error. Testing results demonstrate that this  method  is  available  both  in  static  and  angular  rate  variation  situations.  After  filtering,  quite  a  bit  of improvement is obtained, part of constant drift rate was compensated; raw measurement variance is reduced by more than 99 percent; random walk also has been effectively removed from random drift error.

# Summary. An optional shortened abstract.
summary: This work presents a method to mitigate stochastic errors in low-cost MEMS gyroscopes using Allan variance analysis, real-time averaging, least square extrapolation, and a Kalman filter. The method effectively reduces errors, compensates for constant drift, and minimizes measurement variance, making it suitable for various MEMS gyroscopes in static and dynamic scenarios.

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
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
# slides: example
---
