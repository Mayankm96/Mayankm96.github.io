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
As a part of the [Robotic Systems Lab](https://rsl.ethz.ch/), headed by
[Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911),
I work on various aspects of robot learning. My research interests lie at the
intersection of reinforcement learning, controls, and computer vision.

I completed my undergraduate studies at IIT Kanpur. Most of my time there was spent developing
autonomous underwater vehicles and co-founding the [AUV team](https://auviitk.com).
In the summer of 2017, I worked with [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/) and [Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/) at the University of Freiburg, Germany on autonomous UAV system for urban search and rescue.

If you have any questions or would like to collaborate, feel free to reach out through
[email](mailto:mittalma@ethz.ch)!

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
