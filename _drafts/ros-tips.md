---
title: Useful Tips for ROS Newbies
layout: post
date:   2017-10-07
comments: true
categories: tutorials
---

Earlier people had to write a large amount of code ranging from low-level driver functions to high level control algorithms. This often made the code reuse nontrivial, and could make changing of even one sensor in the system a daunting task. The Robot Operating System (ROS) modular structure makes the hardware-software integration a piece of cake, and since it is open sourced it provdies a nice base to kick-off with implementation of several novel algorithms into your project.

<img align="right" src="../images/Blog/ros-tips/copy-paste-meme.jpg">

Currently I am using the ROS framework extensively and developing a better comprehension of the entire [robot software architecture](http://www.ni.com/white-paper/13929/en/), all thanks to my recent projects. While I had started learning ROS through its tutorials [here](http://wiki.ros.org/ROS/Tutorials), I felt that it merely introduces the various core concepths in ROS such as the functioning of `master`, `nodes`, and `topics`. Even after going through all of them it took a while for me to write the first ROS node on my own. (It could also be I am a slow learner? :P ) Having said that, the post is mainly to highlight a few interesting ROS concepts and packages that a beginner should find useful.


https://blog.acolyer.org/2015/11/02/ros-an-open-source-robot-operating-system/

## 1. Implement. Imeplment. Implement

This can't be emphasized enough but claiming to know ROS by just having done the tutorials is equivalent to saying that one has learned how to code after just seeing the syntax of a programming language. Learning can be faster is you have an application in mind. If you don't already, consider the following challenges:

* __For Hardware Lovers__: Using  your favorite microcontroller (say, Arduino), and write an arduino node that shall subscribe to a topic and use the information published there to perform some event such as actuation of a motor using PWM signals from the controler. (*Hint:* Take a look at the [rosserial_arduino](http://wiki.ros.org/rosserial) package)
* __For Computer Vision Lovers:__ Using the OpenCV library, write a node which publishes the image frames from a camera onto a topic and then visualize the data being published through the image_view package. (*Hint:* Take a look at the [cv_bridge](http://wiki.ros.org/cv_bridge) package)

__NOTE:__ The above list is open to additions. If you would like to add more to it, feel free to comment below on this post.

## 2. Miss the GUIs?

Running ROS commands through the terminal isn't really a bad practice. However, if you are like me, then you'd prefer GUIs more any particular day. ROS actually provides its on Qt-based GUI tool called [rqt](http://wiki.ros.org/rqt). In the rqt_gui, various plugins can be imported to do a variety of things. The ones available include publishing to a topic, visualizing on rviz, robot monitor and many other given [here](http://wiki.ros.org/rqt/Plugins). In fact, if required you could design your own rqt plugin by following the tutorial [here](http://wiki.ros.org/rqt/Tutorials/Create%20your%20new%20rqt%20plugin).

Well, the one which I grew a fancy for is particularly the [`node_manager_fkie`](http://wiki.ros.org/node_manager_fkie). The interface makes it easier to launch bodes and monitor their health, and view the topics, services and parameters being published. Thus, saving the time to write terminal commands everytime.

<img align="center" src="../images/Blog/ros-tips/node-manager.png">

## 3. Running Commands through a Checklist

The [`screerun`](http://wiki.ros.org/screenrun) package in ROS enables 

I encountered this one rather recently. The package helps in >>>>>>>>>>>>>>>>>>>>>

3. ros::spin vs ros::spinonce
4. actionlib vs puglinlib
5. topics vs services
6. rqt
7. nodes vs nodelets
8. ROS Network
9. message::filters
10. diagnostic for your robot
11. usb_cam package
12. Using header stamps
