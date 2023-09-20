---
layout: page
title: Predicting Landing Sites from Aerial Images
description: DAAD Research Internship
img: /assets/img/projects/deeplanding/outdoor_testrun.jpeg
---

*Duration:* May'17 - August'18

*Supervisors:* [Dr. Abhinav Valada](https://rl.uni-freiburg.de/people/valada), [Prof. Wolfram Burgard](http://www2.informatik.uni-freiburg.de/~burgard/)

Unmanned Aerial Vehicles (UAVs) equipped with bioradars are a life-saving technology that can enable identification of survivors under collapsed buildings in the aftermath of natural disasters such as earthquakes or gas explosions. However, these UAVs have to be able to autonomously land on debris piles in order to accurately locate the survivors. This problem is extremely challenging as the structure of these debris piles is often unknown and no prior knowledge can be leveraged. In this work, we propose a computationally efficient system that is able to reliably identify safe landing sites and autonomously perform the landing maneuver.

### Detection Algorithm

Our algorithm computes costmaps based on several hazard factors including terrain flatness, steepness, depth accuracy and energy consumption information. We first estimate dense candidate landing sites from the resulting costmap and then employ clustering to group neighboring sites into a safe landing region. Finally, a minimum-jerk trajectory is computed for landing considering the surrounding obstacles and the UAV dynamics. We demonstrate the efficacy of our system using experiments from a city scale hyperrealistic simulation environment and in real-world scenarios with collapsed buildings.

<div>
    <img class="col three" height="50%" width="50%" src="{{ site.baseurl }}/assets/img/projects/deeplanding/landing_algo.svg" alt="" title="Landing Algorithm"/>
</div>
