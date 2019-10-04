<!-- ---
layout: page
title: Multi- Robot System for Bomb Disposal
description: Funded by The Boeing Company
img: /assets/img/projects/abhyast/phase_robots.jpg
---

*Duration:* July’16 – March’17

*Supervisors:* [Prof. Shantanu Bhattacharya](http://home.iitk.ac.in/~bhattacs/), [Prof. S. Kamle](http://www.iitk.ac.in/new/dr-s-kamle)


Aerial and ground robots together form a 'symbiotic' relationship in which they help overcome each others limitations and leverage their capabilities. Although research has made steady progress over the years on this, most of the work is limited to laboratory settings and is not sufficient for real world challenges.

In this project, we built a multi-robot autonomus system that is capable of performing operations such as bomb- disposal. Considering the severity of the challenges, we are focused on solving our problem for indoor environments.

<p align="center">
    <a class="button" href="/assets/documents/projects/Abhyast_Plan.jpg" target="_blank">View Postor </a>
    <a class="button" href="https://github.com/Boeing-Abhyast/Phase-VII" target="_blank">View Code</a>
    <a class="button" href="http://www.iitk.ac.in/dord/boeing/public/" target="_blank">Visit Website</a>
</p>

### Ground robot: **Alpha**

My work centerd around the system integration and perception parts for the ground robot. Using *Alpha*, a two- wheeled differential drive robot manufactured by us, I implemented various SLAM algorithms such as GMapping, and RGBD-SLAM on it. Through the [navigation](http://wiki.ros.org/navigation) package on ROS, I applied the relaxed A* algorithm to traverse an optimal path to a specified goal. We tested our approach simulation as well as in real world.

I also trained the real-time object detection model [YOLOv2](https://pjreddie.com/darknet/yolov2/) to detect suspect objects from monocular camera inputs, and projected the location of these objects on to a map using the corresponding depth images

<div>
    <img class="col three" height="50%" width="50%" src="{{ site.baseurl }}/assets/img/projects/abhyast/alpha_rviz.png" alt="" title="URDF of Alpha"/>
</div> -->
