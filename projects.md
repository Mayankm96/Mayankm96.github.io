---
layout: page
permalink: /projects/
title: Projects
---
## Predicting Landing Sites from Aerial Images of Disaster Scenes

<p style="text-align:left;"> DAAD Research Intern <span style="float:right;"><small>May - July 2017</small></span></p>
Supervisors: [Prof. Dr. Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/), [Abhinav Valada](http://www2.informatik.uni-freiburg.de/~valada/)

<img style="float: left; padding: 0px 6px 0px 6px" src="/images/Projects/DAAD/alufr.png" >

The project aims to design a novel solution to detect landing sites for a drone in a hostile environment by only using the input from a ground facing camera mounted on it. We use Convolutional Neural Networks in our approach for segmentation of the landing sites into landable and non-landable sites. The model is trained using a synthetic dataset created on Unreal Engine, using Microsoft's drone simulator AirSim.

<hr>

## Bomb Disposal Using Multi-Robot System

<p style="text-align:left;"> Funded by The Boeing Company <span style="float:right;"><small>July 2016- December 2016</small></span></p>
Supervisors: [Prof. Shantanu Bhattacharya](http://home.iitk.ac.in/~bhattacs/), [Prof. S. Kamle](http://www.iitk.ac.in/new/dr-s-kamle)

<img style="float: left; padding: 0px 6px 0px 6px" src="/images/Projects/Boeing/Phase bots.jpg" width="45%">

We are building an aerial and ground vehicle team of autonomus robots that shall perform the operation of bomb- disposal squad. The system leverages the capabilities of the the two robotics to help overcome their limitations and perform the task efficiently.

My work focussed on the system integration and perception part of the ground robot. Using a two- wheeled differential drive robot designed by the team, we compared various SLAM algorithms such as GMapping, Hector-SLAM and RGBD-SLAM on it. I implemented the real-time object detection model YOLO9000 to detect suspect objects like bags, trash cans, and bottles, and used ROS to show the location of these objects on a 2D map created by the robot during its exploration.
<p align="center">
    <a class="btn btn-primary" href="../documents/Abhyast Plan.pdf" target="_blank">View Postor </a>
    <a class="btn btn-primary" href="https://github.com/Boeing-Abhyast/Phase-VII" target="_blank">View Code</a>
    <a class="btn btn-primary" href="http://www.iitk.ac.in/dord/boeing/public/" target="_blank">Visit Website</a>
</p>

<hr>

## Autonomous Underwater Vehicle (AUV)

<p style="text-align:left;"> Funded by Dean of Research and Development, IIT Kanpur <span style="float:right;"><small>November 2014- ongoing</small></span></p>
Supervisors: [Prof. K. S. Venkatesh](http://home.iitk.ac.in/~venkats/), [Prof. Sachin Y. Shinde](http://www.iitk.ac.in/new/sachin-y-shinde)

<img style="float: left; padding: 0px 6px 0px 6px" src="/images/Projects/AUV/AUV water.jpg" width="45%">

Initiated in 2014 by a team of undergraduates, as a project in Robotics Club, we aim to build an AUV as a platform for research in underwater robotics. The team has been divided into three sub-systems namely the mechanical, electrical and software subsystems, of which my major contributions has been towards the former two.

We participated at the National Student Autonomous Vehicle (SAVe) Competition held at Chennai in December 2016, and achieved a second position on our debut.

<p align="center">
    <a class="btn btn-primary" href="../documents/AUV-IITK Report.pdf" target="_blank">View Report </a>
    <a class="btn btn-primary" href="https://github.com/auv-iitk/" target="_blank">View Code</a>
    <a class="btn btn-primary" href="http://auviitk.com/" target="_blank">Visit Website </a>
</p>

<hr>

## Reviewing Techniques for SLAM Implementation

<p style="text-align:left;">Mentor: <a href="http://engineering.nyu.edu/people/farshad-khorrami">Prof. Farshad Khorrami</a>
 <span style="float:right;"><small>May-June 2016</small></span></p>

The project involved reviewing various Bayesian filters and Least Squares optimization for Simulataneous Localization and Mapping (SLAM), keeping in mind its applicability to underwater robots.

Towards the end of the project, I implmented the Extended Kalman Filter algorithm on a Pioneer 3dx robot using the robot simulator V-REP and MATLAB, in order to deepen my understanding of the various elements involved in the SLAM problem such as data association, and scan alignment.

<p align="center">
<a href="/documents/NYU-RTE_Report_Mayank.pdf" class="btn btn-primary" target="_blank">View Report</a>
</p>

<hr>

## Finite Element Analysis in Electromagnetism

<p style="text-align:left;">Mentor: <a href="http://iitk.ac.in/new/rathish-kumar-b-v">Prof. B. V. Rathish Kumar</a>
 <span style="float:right;"><small>December 2015</small></span></p>

<img style="float: left; padding:0px 6px 0px 6px" src="/images/Projects/FEM.PNG" width="45%">

The motivation of the project lied in understanding the math behind Electrical Impedence Tomography (EIT), a medical imaging technique in which electrical conductivity across a part/tissue of the body is used to reconstruct a cross- section image of that part.

My work required reviewing the two popular Finite Element Analysis (FEA) methods- Ritz and Glarenkin, and to solve boundary value problems in electromagnetism  in two- dimensions using adaptive mesh techniques. For instance, the image to the left is a simulation done using the tool FreeFEM++ to solve a two- dimensional axisymmetric problem in electromagnetism.

<p align="center">
    <a href="../documents/NPDE-TCA FEM.pdf" class="btn btn-primary" target="_blank">View Notes</a>
</p>
