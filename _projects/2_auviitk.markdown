---
layout: page
title: Autonomous Underwater Vehicle (AUV)
description: Funded by DoRD, IIT Kanpur
img: /assets/img/projects/auv/varun.jpg
---

*Duration:* November'14 - June'18

*Supervisors:* [Prof. Mangal Kothari](https://www.iitk.ac.in/aero/mangal/), [Prof. K. S. Venkatesh](http://home.iitk.ac.in/~venkats/)

As a student- initiated project at IIT Kanpur, the project aims to build marine systems to serve as a platform for research on underwater robotics in the institute and create affliations with industries looking for marine technology solutions. As one of the founding members of the team, I contributed towards various mechanical, electrical and software aspects of the project.

We participated with our first vehicle, *Varun*, at the __National Student Autonomous Vehicle (SAVe) Competition__ in December 2016, and achieved the runners-up position on our debut. Since then the project has been take over by next generation of students and the team has been participating at national and international events.

<p align="center">
    <a class="button" href="" target="_blank">View Code</a>
    <a class="button" href="http://auv-iitk.github.io/" target="_blank">Visit Website </a>
</p>


<p align="center">
  <img style="vertical-align:middle" src="{{ site.baseurl }}/assets/img/projects/auv/auv.gif" alt="" title="Autonomous Gate Detection and Navigation"/>
</p>

### Mechanical Work

Compared to other robotic systems, in AUVs we need to seal the robot enclosures for protection against water. The recommended ingress protection is referred to IP68 (or above) for all the enclosures. Failure to meet this requirement could lead to damaging of the electronics. In our vehicle *Varun*, we used O-rings and marine-grade expoxy for sealing.

Varun’s mechanical design comprises of an aluminum structural frame, enclosures for electronics and cameras, pneumatic system and electromagnetic actuators. The vehicle has 5 degrees of freedom and roll is stabilized by ensuring a symmetric design. I designed the main pressure hull and other casings, along with the marker dropper. All mechanical parts were first designed on Solidworks and then optimized for weight and structural strength using Ansys Workbench. Their fabrication was done using in-house available facilities at the institute.

<div>
    <img class="col three" height="50%" width="50%" src="{{ site.baseurl }}/assets/img/projects/auv/auv_labelled.png" alt="" title="Design of AUV Varun"/>
</div>

### Electrical Work

The vehicle is powered using Lithium Polymer batteries. I designed a power distribution board, comprising of buck and boost converters, to meet the different voltage and power requirements of various electonic components. I used off-the-shelf motor drivers to control brushed DC actuators through an Atmega microcontroller, and also worked on intergating the sensors with ROS.

<div>
    <img class="col three" height="50%" width="50%" src="{{ site.baseurl }}/assets/img/projects/auv/electrical_schematic.png" alt="" title="Design of AUV Varun"/>
</div>

### Software Work

The Software Architecture is based on the Robot Operating System (ROS) framework. We dvided the entire software stack into motion planning, controls, navigation and vision layers. I contributed mainly to the controls and navigation aspects of the vehicle. The code is open sourced and can be viewed over [here](https://github.com/auv-iitk/).
