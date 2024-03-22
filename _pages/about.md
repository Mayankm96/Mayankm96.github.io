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
years: [2024, 2023, 2022, 2021, 2020, 2019, 2018]
---

_How can a robot learn to use its different parts for interactions?_  
_How can we go beyond proprioception for robust mobile manipulation?_  
_What abstractions are necessary to describe multiple tasks?_ 

To find *some* answers to the above questions, I am currently a PhD student at [ETH Zurich](https://ethz.ch/en.html) advised by [Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911), and a Research Scientist at [NVIDIA Research](https://www.nvidia.com/en-us/research/).

Over the span of my career, I have had the opportunity to work with some amazing robotic groups
on many different robotic platforms.
I have been a visiting student researcher at [Vector Institute](https://vectorinstitute.ai/),
a research intern at [NNAISENSE](https://nnaisense.com/), and a part-time research engineer
at [ETH Zurich](https://ethz.ch/en.html). During my undergrad at [IIT Kanpur](http://www.iitk.ac.in/ee/), I was a visiting student at
University of Freiburg, Germany, working closely with [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/) and [Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/).
I also founded the [AUV-IITK](https://auv-iitk.github.io/#/landing-page) team, where I worked on different
hardware and software aspects of building an autonomous underwater vehicle.

If you have questions or would like to discuss ideas, feel free to reach out through
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
## __publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
