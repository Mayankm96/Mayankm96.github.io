---
title: Useful Tips for ROS Newbies
layout: post
date:   2017-10-07
comments: true
categories: tutorials
description: Getting pass a beginner's understanding of ROS quickly and properly.
---

Earlier people had to write a large amount of code ranging from low-level driver functions to high level control algorithms. This often made code reuse nontrivial, and changing even one sensor in the system could be a daunting task. The Robot Operating System (ROS) modular structure simplifies hardware-software integration. Moreover, thanks to the large open sourced community, ROS provdies a nice base to start implementating several novel algorithms into your project.

Although the [ROS tutorials]((http://wiki.ros.org/ROS/Tutorials)) introduces various core concepts of ROS, it takes a bit of hard work to develop a better comprehension of the entire [robot software architecture](http://www.ni.com/white-paper/13929/en/). Even after going through all of them, I struggled to write my first ROS node. *(Could be I am a slow learner? :P )* Having said that, the post highlights a few interesting ROS concepts and packages that a beginner might find useful in his journey as a robotic developer.

## 1. Implement? Imeplment. Implement!

This can't be emphasized enough but claiming to know ROS by just having done the tutorials is equivalent to saying that one has learned how to code after just seeing the syntax of a programming language. Learning can be faster is you have an application in mind. If you don't already, consider the following challenges:

<div class="img_raw">
<img class="wrap one" src="{{ site.baseurl }}/assets/img/blog/ros-tips/copy-paste-meme.jpg" alt="" title="How to become a Developer?"/>
</div>

* __For Hardware Lovers__: Using  your favorite microcontroller (say, Arduino), and write an arduino node that shall subscribe to a topic and use the information published there to perform some event such as actuation of a motor using PWM signals from the controler. (*Hint:* Take a look at the [rosserial_arduino](http://wiki.ros.org/rosserial) package)
* __For Computer Vision Lovers:__ Using the OpenCV library, write a node which publishes the image frames from a camera onto a topic and then visualize the data being published through the image_view package. (*Hint:* Take a look at the [cv_bridge](http://wiki.ros.org/cv_bridge) package)

__NOTE:__ The above list is open to additions. If you would like to add more to it, feel free to comment below on this post.

## 2. Miss the GUIs?

Running ROS commands through the terminal isn't really a bad practice. However, if you are like me, then you'd prefer GUIs more any particular day. ROS actually provides its on Qt-based GUI tool called [rqt](http://wiki.ros.org/rqt). In the rqt_gui, various plugins can be imported to do a variety of things. The ones available include publishing to a topic, visualizing on rviz, robot monitor and many other given [here](http://wiki.ros.org/rqt/Plugins). In fact, if required you could design your own rqt plugin by following the tutorial [here](http://wiki.ros.org/rqt/Tutorials/Create%20your%20new%20rqt%20plugin).

Well, the one which I grew a fancy for is particularly the [`node_manager_fkie`](http://wiki.ros.org/node_manager_fkie). The interface makes it easier to launch bodes and monitor their health, and view the topics, services and parameters being published. Thus, saving the time to write terminal commands everytime.

<div class="img_true">
    <img class="col three" src="{{ site.baseurl }}/assets/img/blog/ros-tips/node-manager.png" alt="" title="Node Manager GUI"/>
</div>

## 3. Running via commands checklist

Yes, it is possibe to do this through the [`screerun`](http://wiki.ros.org/screenrun) package in ROS. What it actually does is parse over the commands written in a YAML file and push them onto a *virtual* terminal, similar to as if you have typed them. Only those commands that end with `\015` (the octal literal for `Enter`) are executed.

This comes in handy when you have to deal with large project repostiories. Although running nodes by using a launch files is really common (and recommended), the `screenrun` package seem to provide more flexibility over the general terminals commands that one might need to execute.

A sample config file `config.yaml` is as follows:
```yaml
programs:
  -
    name: 2d-mapping
    commands:
      - roscd alpha_master
      - roslaunch alpha_master sim_alpha_slam.launch\015
  -
    name: 2d-navigation
    commands:
      - roslaunch alpha_move_base move_base.launch\015
  -
    name: bag
    commands:
      - rosbag record --duration=30 /map /particlecloud /tf

```

To run the package you could either use `rosrun screenrun screenrun [b]` or launch it through a launch file:
```xml
<launch>
  <node name="screenrun" pkg="screenrun" type="screenrun" args="b" output="screen">
    <rosparam file="$(find <package-name>)/screenrun/config.yaml" command="load"/>
  </node>
</launch>
```

The argument `b` is optional. If `b` is passed, [byobu](http://byobu.co/) is used instead of [screen](https://www.gnu.org/software/screen/).

## 4. `ros::spin` vs `ros::spinonce`

To read more about this you can check the answer over here or the ROS documentation here.

4. actionlib vs puglinlib
5. topics vs services
6. rqt
7. nodes vs nodelets
8. ROS Network
9. message::filters
10. diagnostic for your robot
11. usb_cam package
12. Using header stamps
