---
layout: about
permalink: /
title: <strong>Mayank</strong> Mittal
description: Graduate Student | Department of Mechanical Engineering, ETH Zurich

profile:
  align: right
  image: prof_pic2.jpg
  address: #mention address

news: true
social: true
years: [2021, 2020, 2019, 2018]
---

___"People who are really serious about software should make their own hardware."___ - Alan Kay

I am a graduate student at [ETH Zurich](https://ethz.ch/en.html), advised by [Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911).
My research is focused on high-level reasoning and planning for mobile manipulation.
I also closely collaborate with [Animesh Garg](https://animesh.garg.tech/) at the University of Toronto.

Over the past few years, I have had the opportunity to work on various robotic systems with some amazing groups.
Most of my time during my undergraduate studies was spent developing autonomous underwater vehicles and co-founding the [institute's student team](http://auv-iitk.github.io/).
During the summer of 2017, I worked with [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/) and [Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/) at the University of Freiburg, Germany on building autonomous aerial systems for urban search and rescue.
My internship at [NNAISENSE](https://nnaisense.com/) involved safe-grasping of objects using manipulators.

If you have any questions or would like to collaborate, feel free to reach out through
[email](mailto:mittalma@ethz.ch)!

<!-- For available student projects with me at RSL, please check [here](https://rsl.ethz.ch/education-students.html). -->

<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

## __research interests__

I am primarily interested in decision-making and control for the operation of robots in human environments.
These days, my efforts are focused on designing perception-based systems for contact-rich manipulation tasks, such as articulated object interaction and in-hand manipulation.
Other areas of interest include hierarchical reinforcement learning, optimal control, and 3D vision.

---

{: #publications}
## __publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
