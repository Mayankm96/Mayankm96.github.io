---
layout: page
title: Multi- Robot System for Bomb Disposal
description: Funded by The Boeing Company
img: /assets/img/projects/abhyast/phase_robots.jpg
---

*Supervisors:* [Prof. Shantanu Bhattacharya](http://home.iitk.ac.in/~bhattacs/), [Prof. S. Kamle](http://www.iitk.ac.in/new/dr-s-kamle)

Aerial and ground robots together form a 'symbiotic' relationship in which they help overcome each others limitations and leverage their capabilities. Although research has made steady progress over the years on this, most of the work is limited to laboratory settings and is not sufficient for real world challenges.

In this project, we are building a multi- robot autonomus system that is capable of performing operations such as bomb- disposal. Considering the severity of the challenges, we are presently focusing our problem for indoor environments.

My work centers around the system integration and perception parts for the ground robot. Using *Alpha*, a two- wheeled differential drive robot manufactured by us, I implemented various SLAM algorithms such as GMapping, Hector-SLAM and RGBD-SLAM on it. Through the [navigation](http://wiki.ros.org/navigation) package on ROS, we applied the relaxed A* algorithm to traverse an optimal path to a specified goal.

I am curretnly implementing the real-time object detection model YOLO9000 to detect suspect objects from the on- board camera input, and showing the locations of these objects on the online map created during exploration by *Alpha*.

<p align="center">
    <a class="button" href="/assets/documents/projects/Abhyast_Plan.jpg" target="_blank">View Postor </a>
    <a class="button" href="https://github.com/Boeing-Abhyast/Phase-VII" target="_blank">View Code</a>
    <a class="button" href="http://www.iitk.ac.in/dord/boeing/public/" target="_blank">Visit Website</a>
</p>

#### References
1. Zoltán Beck, Luke Teacy, Alex Rogers, and Nicholas R. Jennings (2016). Online Planning for Collaborative Search and Rescue by Heterogeneous Robot Teams. In Proceedings of 2016 International Conference on Autonomous Agents \& Multiagent Systems (AAMAS '16), Richland, SC, 1024-1033.
2. Butzke, J., Gochev, K., Holden, B., Jung, E., \& Likhachev, M. (2016). Planning for a ground-air robotic system with collaborative localization. ICRA.
3. Joseph Redmon and (2016). YOLO9000: Better, Faster, Stronger. CoRR, abs/1612.08242, .
