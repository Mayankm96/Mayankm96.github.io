---
layout: about
permalink: /
title: <strong>Mayank</strong> Mittal
description: Graduate Student | Robotics, Systems, and Control, ETH Zurich

profile:
  align: right
  image: prof_pic.jpg
  address: #mention address

news: true
social: true
years: [2020, 2019, 2018]
---

I am a graduate student in Robotics, Systems, and Controls program at ETH Zurich.
I consider myself a full-stack roboticist who loves working on unsolved challenges
in creating autonomous systems. My interests lie at the intersection of computer
vision, controls, and machine learning.

I am a part of the [Robotic Systems Lab](https://rsl.ethz.ch/), headed by
[Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911),
where I work closely with the RL team on sim-to-real transfer of locomotion and manipulation control.
Currently, I am working with [Marco Gallieri](https://www.linkedin.com/in/marco-gallieri-166a0421/)
at NNAISENSE on safe-learning and verification of controllers.

My endeavors in robotics started during my undergraduate studies. In the summer of 2017,
I worked under the guidance of [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/) and [Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/) at Freiburg, Germany. My work focused on developing
an autonomous UAV system with bio-radars for urban search and rescue missions. Out of self-motivation,
I also co-founded the [AUV team](https://auviitk.com), a platform for marine robotics, in my freshman year.
I spent most of my undergrad developing this technology and worked on various hardware and
software aspects of the system. This project is currently led by [Mangal Kothari](https://www.iitk.ac.in/aero/mangal/)
and I am now an advisor for the team.

Apart from my academic engagements, I enjoy playing lawn tennis, hiking, and running! *Occasionally I upload pictures
from my trips on [Instagram](https://www.instagram.com/mayankm155/).*

<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

{: #publications}
## __publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
