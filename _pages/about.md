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
---

I am a graduate student in Robotics, Systems and Controls program at [ETH Zurich](http://www.master-robotics.ethz.ch/). My research interests lie in designing learning-based systems for navigation and manipulation in unknown environments.

I graduated from [IIT Kanpur](http://www.iitk.ac.in/) in May 2018 with a Bachelors in Electrical Engineering. In the summer of 2017, I worked with [Prof. Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/) on predicting landing sites from aerial images. During my undergraduate program, I co-founded the [AUV team](https://auviitk.com) for marine robotics and worked on various mecahnical, electrical and software aspects of the project.

Apart from my academic engagements, I enjoy playing lawn tennis, swimming and trying out new cuisines! In my spare time, I often end up procrastinating on GitHub or reading about new hardware.

<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

## __projects__

{% for project in site.projects %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>
{% else %}

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}

### other relevant projects

* Survey on Variational Autoencoders for Bayesian Inference ([report](/assets/documents/projects/cs698-report.pdf))
* Visual Odometry using careful Feature Selection and Tracking ([report](/assets/documents/projects/ee698-report.pdf), [code](https://github.com/Mayankm96/Stereo-Odometry-SOFT))
* MATLAB based GUI for Motion Planning ([code](https://github.com/Mayankm96/Motion-Planning-GUI))
* Failure Handling in Swarm of Quadrotors ([report](/assets/documents/projects/cs637-report.pdf))

---

## __teaching__

* (Winter 2017: TA, guest lecturer): [AE640A: Autonomous Navigation](https://ae640a.github.io) with [Mangal Kothari](https://www.iitk.ac.in/aero/mangal/)

    * preparing course materials and assignments
    * guest lecturer on system integration using ROS ([slides](/assets/documents/teaching/ae640a/ae640a_lecture1.pdf)), robot simulation using Gazebo ([slides](/assets/documents/teaching/ae640a/ae640a_lecture2.pdf)), mathematical foundation for Robotics ([slides](/assets/documents/teaching/ae640a/ae640a_lecture9.pdf)), and non-parametric filters for localization

### tutorials

* (Summer 2018): Introduction to Robot Operating System ([slides](/assets/documents/talks/Intro_to_ROS.pdf), [tutorial](/assets/documents/talks/Tutorial-ROS.pdf), [post](/blog/2017/ros-tips/))
* (Fall 2016): Sensors and Actuators ([slides](/assets/documents/talks/sensors-and-actuators.pdf))
* (Fall 2016): Introduction to Robotics ([slides](/assets/documents/talks/intro-to-robotics.pdf))
