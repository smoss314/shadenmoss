---
title: "Extended Kalman Filter for SLAM"
permalink: /projects/ekf-slam/
layout: single
tags: SLAM
author_profile: false
---

<p align="center">
  <img src="{{ site.baseurl }}/assets/images/ekf-task-1.gif" width="600" alt="EKF SLAM Demo">
</p>

In a Simultaneous Localization And Mapping (SLAM) course I implemented an Extended Kalman Filter (EKF) in simulation using python. The first figure belowshows a scenario in which a robot (light blue circle) is given inputs to follow a path corrupted by noise. As the robot moves it gets data from simulated sensors picking up landmarks. The simulation uses an EKF to estimate the robot's position within an ellipse measuring a 3-sigma confidence interval (yellow ellipse). The algorithm also identifies the location of each landmark within a 3-sigma confidence interval (red elipses). Notice how closely the EKF estimate follows the true position and how the certainty of both robot position and landmark position increase as the first loop is completed (i.e. when the robot gets around to seeing landmark 2 for the second time).

The video below shows the same algorithm adjusted to run on the popular Victoria Park SLAM data set, where obstacles are identified as stars. The figure afterward highlights the portion of the original Victoria Park data set corresponding to this simulation. Please note that the simulation and the figure are not rotationally aligned.

<iframe width="720" height="405" 
        src="https://www.youtube.com/embed/IKZ6lQ8pQ8k" 
        frameborder="0" 
        allowfullscreen>
</iframe>

<p align="center">
  <img src="{{ site.baseurl }}/assets/images/VictoriaParkHighlight.png" width="600" alt="Victoria Park Highlight">
</p>
