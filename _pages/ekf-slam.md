---
title: "Extended Kalman Filter for SLAM"
permalink: /projects/ekf-slam/
layout: single
tags: SLAM
author_profile: false
---

For an assignment in a course on SLAM I implemented an extended Kalman filter in simulation using python. The first figure shows a scenario in which a robot (light blue circle) is given inputs to follow a path (green line) corrupted by noise (dark blue line). As the robot moves it gets data from simulated sensors (light blue lines) picking up landmarks (numbered circles 0-15). The simulation uses an extended Kalman filter to estimate the robot's position (yellow line) within an ellipse measuring a 3-sigma confidence interval (yellow ellipse). The algorithm also identifies the location of each landmark (red elipses) and renders the expected position of the landmark relative to the robot (red lines). Notice how closely the EKF estimate follows the true position and how the uncertainty of both robot position and landmark position decrease as the first loop is completed (i.e. when the robot gets around to seeing landmark 2 for the second time).

<p align="center">
  <img src="{{ site.baseurl }}/assets/images/ekf-demo.gif" width="600" alt="EKF SLAM Demo">
</p>

The second figure shows the same algorithm running on the first several seconds of the popular Victoria Park SLAM data set, where obstacles are identified as stars. The third figure shows the portion of the original Victoria Park data set corresponding to this simulation.

embed gif

embed png
