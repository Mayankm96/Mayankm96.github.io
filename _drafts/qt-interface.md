---
title: Qt Interface with ROS/C++
layout: post
date:   2017-9-26
comments: true
categories: tutorials
---

After having used ROS for quite a while, it became an almost mundane task to have to run commands on the [gnome-terminal](https://help.gnome.org/users/gnome-terminal/stable/) for executing launch files and checking whether the nodes are running properly or not. During one of my procrastination breaks, I stumbled upon the utility [`node_manager`](http://wiki.ros.org/node_manager_fkie) which is a great tool to run and configure various ROS nodes. I tried it out instantly and loved the intuitive feel it gave over the entire ROS experience. From then on, I felt an urge to replace the monotonic terminal screen with a self-designed user interface for the projects I have been working on. I must confess I am not an expert in making graphical interfaces, but I'll try to be as descriptive as I can in my explanations.

Since the `node_manager_fkie` application was written using [PySide](https://wiki.qt.io/PySide) (an alternate to PyQt), it didn't really appeal to me much since I, in general, prefer C++ over python for most of my projects. Thus, in this tutorial, we would be seeing on how to create a graphical interface using the Qt framework with ROS and C++.

__Pre-Requisites:__ It would be helpful if you have the working knowledge of [ROS (Robot Operating System)](http://www.ros.org/) and C++ (that is the basics of object-oriented programming).

<!-- Nonetheless, in this tutorial blog post we would be making a  would be since a lot of developers prefer python due to its easy maintenance and "faster" development time, for this blog post I would mainly be elucidating on creating a PyQt interface which displays the messages being published on a particular topic that can be selected using a drop-down list. -->

# A few Qt Concepts

For beginners, it might be useful to know a bit more about Qt before wanting to dive in and making your own graphical interfaces. The first and foremost fact is that Qt is pronounced as 'cute' and not 'cue-tee', although many tend to say the latter (including me).

[Qt](https://en.wikipedia.org/wiki/Qt_(software)) is essentially a C++ based cross-platform application framework, used to develop applications and graphical user interfaces (GUIs). Along similar lines is the term [QML](https://en.wikipedia.org/wiki/QML), which stands for "Qt Markup Language", is a highly readable, [JSON](http://www.json.org/)- like, [declarative](https://stackoverflow.com/questions/1784664/what-is-the-difference-between-declarative-and-imperative-programming) UI markup language that helps in describing UIs in terms of their visual components and how they interact and relate with one another. The  Qt QML module provides the QML language along with its engine infrastructure, more about which can be read [here](http://doc.qt.io/qt-5/qtqml-index.html).

Qt is built from [modules](http://doc.qt.io/qt-5/qtmodules.html) such as QtCore, QtGUI, QtWidgets, QtWebKit, QtOpenGL. Of these, the [Qt Quick](http://doc.qt.io/qt-5/qtquick-index.html) module provides the necessary framework required to build QML applications. A QML application's front-end, also called the declarative UI, is composed of tags called elements (`Item{...}`) imported from the Qt Quick module; these can be enhanced using JavaScript code. The other hand, the back-end, or the native functionality, is typically developed using Qt C++. This allows a degree of abstraction between the design-oriented developers and the functional developers for an application.


> __NOTE:__ In order to install Qt 5.7, you may follow this [Installation Guide](https://wiki.qt.io/Install_Qt_5_on_Ubuntu). In case, you are unable to find the examples on opening QtCreator, the following command would come handy: `sudo apt-get install qtbase5-examples qtbase5-doc-html`

I would recommend going through a few tutorials available [here](http://doc.qt.io/qt-5/qtquick-codesamples.html), or at least the [calculator](http://doc.qt.io/qt-5/qtquick-demos-calqlatr-example.html) one, in order to gain a better insight on how Qt Quick and Qt QML modules are used to make user interfaces. It is important to note the flow pattern present between various tags. Qt provides a well- maintained documentation of its modules, so most of the time just searching what exactly you need to implement, you'd find the required tags for it.

# Setup Instructions

*Requirements:* [Ubuntu 16.04LTS](http://releases.ubuntu.com/16.04/) with [ROS Kinetic](http://wiki.ros.org/kinetic/Installation/Ubuntu) installed

## Installing the ROS Qt Creator Plug-in

 ```bash
 # Install QtCreator 5.7
 sudo add-apt-repository ppa:levi-armstrong/qt-libraries-xenial  
 sudo add-apt-repository ppa:levi-armstrong/ppa  
 sudo apt update && sudo apt install qt57creator
 # Install ROS Plugin for QtCreator
 sudo apt install qt57creator-plugin-ros
# Setting up environemnt variables
 echo "source /opt/qt57/bin/qt57-env.sh" >> ~/.bashrc     # for bash users
 echo "source /opt/qt57/bin/qt57-env.sh" >> ~/.zshrc      # for zsh users
 ```
