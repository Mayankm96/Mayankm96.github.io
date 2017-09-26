---
title: Qt Inetrface with ROS and Python
layout: post
date:   2017-9-26
comments: true
categories: tutorials
---

After having used ROS for quite a while, it became an almost mundane task to have to run commands on the [gnome-terminal](https://help.gnome.org/users/gnome-terminal/stable/) for executing launch files and checking whether the nodes were running properly or not. During one of my procrastination breaks, I stumbled upon the utility [`node_manager`](http://wiki.ros.org/node_manager_fkie) which is a graphical interface to run and configure various ROS nodes. I tried it out instantly and loved the intuitive feel it gave over the entire ROS experience. From then on, I felt an urge to repace the monotonic terminal screen with a self- designed user interface for the projects I had been working on.

Since the `node_manager_fkie` application was written using [PySide](https://wiki.qt.io/PySide) (an alternate to PyQt), one of the early things I came across was [qt_ros](http://wiki.ros.org/qt_ros?distro=kinetic) which didn't really appeal to me much since I, in general, prefer C++ over python for most of my projects. Nonetheless, since a lot of developers prefer python due to its easy maintainence and "faster" development time, for this blog post I would mainly be elucidating on creating a PyQt interface which displays the messages being published on a particular topic that can be selected using a drop down list.

# Setup Instructions

*Requirements:* [Ubuntu 16.04](http://releases.ubuntu.com/16.04/) with [`ros-kinetic-desktop-full`](http://wiki.ros.org/kinetic/Installation/Ubuntu) installed

## Installing the ROS Qt Creator Plug-in

 ```
 sudo add-apt-repository ppa:levi-armstrong/qt-libraries-xenial  
 sudo add-apt-repository ppa:levi-armstrong/ppa  
 sudo apt update && sudo apt install qt57creator
 sudo apt install qt57creator-plugin-ros
 echo "source /opt/qt57/bin/qt57-env.sh" >> ~/.bashrc
 ```
