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

I am a graduate student in the Robotics, Systems, and Controls program at ETH Zurich.
As a part of the [Robotic Systems Lab](https://rsl.ethz.ch/), headed by
[Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911),
I work on learning robot control for mobile manipulators.

Over the past few years, I have been fortunate to work on a variety of robotic systems. Most of my time
during my undergrad was spent developing autonomous underwater vehicles and co-founding the institute's [AUV team](https://auviitk.com).
During the summer of 2017, I worked with [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/) and [Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/) at the University of Freiburg, Germany on building autonomous aerial systems for urban search and rescue. Most recently, my internship at [NNAISENSE](https://nnaisense.com/) involved safe-grasping of objects using manipulators.

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
