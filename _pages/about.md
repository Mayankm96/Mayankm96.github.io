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
years: [2023, 2022, 2021, 2020, 2019, 2018]
---

_How can a robot learn from its own interactions?_  
_What abstractions are necessary to describe a task?_  
_When does a robot even know that the task is now completed?_  

In a quest to find answers to the above questions, I am currently a PhD student at [ETH Zurich](https://ethz.ch/en.html) advised by [Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911), and a Research Scientist at [NVIDIA Research](https://www.nvidia.com/en-us/research/). I also closely collaborate with [Animesh Garg](https://animesh.garg.tech/) at the [University of Toronto](https://web.cs.toronto.edu/).

Over the past few years, I have had the opportunity to work with some amazing robotic groups.
I have been a visiting student researcher at [Vector Institute](https://vectorinstitute.ai/),
a research intern at [NNAISENSE](https://nnaisense.com/), and a part-time research engineer
at [ETH Zurich](https://ethz.ch/en.html). During my undergrad at [IIT Kanpur](http://www.iitk.ac.in/ee/), I was a visiting student at
University of Freiburg, Germany, working closely with [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/) and [Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/).

I am incredibly thankful to my collaborators and mentors, and enjoy exploring new domains through collaborations. If you have questions or would like to work together, feel free to reach out through
[email](mailto:mittalma@ethz.ch)!

<!-- _Shameless promotion:_  
For undergrad/graduate students at [ETH Zurich](https://ethz.ch/en.html): In case you are looking for semester projects or master thesis, please check [here](https://rsl.ethz.ch/education-students.html) for available projects with me and other amazing people in our group! -->

<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

## __research interests__

I am primarily interested in the decision-making and control of robots in human environments.
These days, my efforts are focused on designing perception-based systems for contact-rich manipulation tasks, such as articulated object interaction with mobile manipulators and in-hand manipulation.
Other areas of interest include hierarchical reinforcement learning, optimal control, and 3D vision.

---

{: #publications}
## __publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}
