---
layout: about
permalink: /
title: <strong>Mayank</strong> Mittal
description: Graduate Student | ETH Zurich | NVIDIA

profile:
  align: right
  image: prof_pic3.jpg
  address: #mention address

news: true
social: true
years: [2025, 2024, 2023, 2022, 2021, 2020, 2019, 2018]
---

I am currently a *final-year* PhD student at [ETH Zurich](https://ethz.ch/en.html), advised by [Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911), and a Research Scientist at [NVIDIA](https://www.nvidia.com/en-us/research/).

My research explores how robots can learn to reason about their bodies and surroundings to achieve more adaptive and
versatile behaviors. This includes whole-body control for mobile manipulation, reinforcement learning for contact-rich tasks, and integrating multi-modal sensing to enhance decision-making.

<!-- Over the span of my career, I have had the opportunity to work with some amazing robotic groups
on many different robotic platforms.
I have been a visiting intern at the [Vector Institute](https://vectorinstitute.ai/),
a research intern at [NNAISENSE](https://nnaisense.com/), and a part-time research engineer
at [ETH Zurich](https://ethz.ch/en.html). During my Bachelor's at [IIT Kanpur](http://www.iitk.ac.in/ee/), I worked
at University of Freiburg, Germany with [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/) and [Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/).
I also founded the [AUV-IITK](https://auv-iitk.github.io/#/landing-page) team. -->

If you have any questions or would like to discuss ideas, feel free to reach out via
[email](mailto:mittalma@ethz.ch)!

<!-- _Shameless promotion:_  
For undergrad/graduate students at [ETH Zurich](https://ethz.ch/en.html): In case you are looking for semester projects or master thesis, please check [here](https://rsl.ethz.ch/education-students.html) for available projects with me and other amazing people in our group! -->

<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

{: #publications}
## __selected publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
