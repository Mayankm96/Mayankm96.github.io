---
layout: page
title: Learning Locomotion-Manipulation Control
description: Semester Thesis
img: /assets/img/projects/rsl-alma/raisim_alma_rendered.png
---

*Duration:* March'19 - July'19

*Supervisors:* Vassilios Tsounis, David Hoeller, [Prof. Marco Hutter](https://rsl.ethz.ch/the-lab/people/person-detail.html?persid=121911)

Although a lot of work has been towards the autonomy of mobile robots and manipulators, developments in the field of mobile manipulators have been slower mainly due to the complexity of these robots. In the last few years, deep reinforcement learning (RL) has emerged a promising solution for such kind of complex problems and have shown to work well even in high-dimensional continuous domains.  

This work considers the problem of learning policies for a mobile manipulator in partially observable domains. We consider the robot ALMA, a completely torque-controlled quadrupedal robot with six degrees of freedom robotic arm mounted on it. We formulated the learning problem as a cooperative multi-agent system comprising of the quadrupedal robot and the robotic arm, and extend the single-agent deep RL algorithm based on policy gradients to this setting. Specifically, we examined the centralized and decentralized multi-agent system designs without any explicit communication between the agents. We showed that learning based on a completely decentralized multi-agent system tends to outperform a centralized multi-agent system on a suite of cooperative control tasks that we propose in this work. These tasks were designed in order to train command conditioned policies for the robot. We considered the base velocity command for the mobile platform and the desired end-effector position of the manipulator as the set of commands for learning a holistic controller.

<p align="center">
  <img style="vertical-align:middle" src="{{ site.baseurl }}/assets/img/projects/rsl-alma/alma.gif" alt="" title="Random end-effector and base velocity commands"/>
</p>

<!-- <div>
    <img class="col three" height="50%" width="50%" src="{{ site.baseurl }}/assets/img/projects/rsl-alma/summary_obs_actions.png" alt="" title="Overview of Agent's Observations and Actions"/>
</div> -->
