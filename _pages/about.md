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
years: [2019, 2018]
---

I am a graduate student in Robotics, Systems and Controls program at [ETH Zurich](http://www.master-robotics.ethz.ch/). My research interests lie in designing learning-based systems for navigation and manipulation in unknown environments.

At ETH, I received the opportunity to work with [Prof. Marco Hutter](http://www.rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911) on learning locomotion-manipulation policies for arm-on-ANYmal. Currently I am working with [Dr. Marco Gallieri](https://www.linkedin.com/in/marco-gallieri-166a0421/) and [Dr. S.S.M. Salehian](https://ch.linkedin.com/in/seyed-sina-mirrazavi-salehian-11772856) on safe-grasping of unknown objects for manipulators.

I graduated from [IIT Kanpur](http://www.iitk.ac.in/) in May 2018 with a Bachelors in Electrical Engineering. In the summer of 2017, I worked with [Prof. Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/) on predicting landing sites from aerial images. During my undergraduate program, I co-founded the [AUV team](https://auviitk.com), a platform for research in marine robotics. We achieved the runners-up position at [SAVe-2017](http://www.niot.res.in/SAVe/) .

Apart from my academic engagements, I enjoy playing lawn tennis, and running! In my spare time, I often end up on GitHub _(a good replacement to other form of social media)_.

<div class="post">

  {% if page.news %}
    {% include news.html %}
  {% endif %}

</div>

---

## __publications__

{% for y in page.years %}
  {% bibliography -f papers -q @*[year={{y}}]* %}
{% endfor %}

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

##### At ETH Zurich

* Using Semantics to detect Camera Miscalibrations
* Multi-camera DeepTAM ([report](/assets/documents/projects/Multicam_Deeptam.pdf), [code](https://github.com/surirohit/multi-camera-deeptam))
* Verification of Neural Networks using Linear Programming ([report](/assets/documents/projects/RIAI_Manuel_Mayank.pdf), [code](https://github.com/Mayankm96/verify_neural_networks))
* Monocular Odometry with Bundle Adjustment ([report](/assets/documents/projects/VA4MR_Mini_Project.pdf), [video](https://www.youtube.com/watch?v=trbBh8Rjc4s&feature=youtu.be), [code](https://github.com/Mayankm96/Mono-Odometry))

##### At IIT Kanpur

* Survey on Variational Autoencoders for Bayesian Inference ([report](/assets/documents/projects/cs698-report.pdf))
* Multi- Robot System for Bomb Disposal ([poster](/assets/documents/projects/Abhyast_Plan.jpg), [code](https://github.com/Boeing-Abhyast/Phase-VII))
* Visual Odometry using careful Feature Selection and Tracking ([report](/assets/documents/projects/ee698-report.pdf), [code](https://github.com/Mayankm96/Stereo-Odometry-SOFT))
* MATLAB based GUI for Motion Planning ([code](https://github.com/Mayankm96/Motion-Planning-GUI))
* Failure Handling in Swarm of Quadrotors ([report](/assets/documents/projects/cs637-report.pdf))

### open source projects

* ROS package for AirSim simulator- in C++ ([code](https://github.com/Mayankm96/airsim_img_publisher))
* ROS package for AirSim simulator- in Python ([code](https://github.com/Mayankm96/airsim_ros_client))
* ROS package for saving data published from Zed Camera ([code](https://github.com/Mayankm96/extract_zed_data))
* ROS package for publishing data from Sparton AHRS8 sensor ([code](https://github.com/Mayankm96/sparton_ahrs8_driver))

---

## __teaching__

* (Winter 2017: TA, guest lecturer): [AE640A: Autonomous Navigation](https://ae640a.github.io) with [Mangal Kothari](https://www.iitk.ac.in/aero/mangal/)

    * preparing course materials and assignments
    * guest lecturer on system integration using ROS ([slides](/assets/documents/teaching/ae640a/ae640a_lecture1.pdf)), robot simulation using Gazebo ([slides](/assets/documents/teaching/ae640a/ae640a_lecture2.pdf)), mathematical foundation for Robotics ([slides](/assets/documents/teaching/ae640a/ae640a_lecture9.pdf)), and non-parametric filters for localization

### tutorials

* (Spring 2019): Hierarchical Reinforcement Learning ([slides](/assets/documents/talks/HRL_Part2_Mayank.pdf))
* (Summer 2018): Introduction to Robot Operating System ([slides](/assets/documents/talks/Intro_to_ROS.pdf), [tutorial](/assets/documents/talks/Tutorial-ROS.pdf), [post](/blog/2017/ros-tips/))
* (Fall 2016): Sensors and Actuators ([slides](/assets/documents/talks/sensors-and-actuators.pdf))
* (Fall 2016): Introduction to Robotics ([slides](/assets/documents/talks/intro-to-robotics.pdf))
