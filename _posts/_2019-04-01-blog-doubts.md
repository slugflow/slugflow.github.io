---
title: 'Doubts'
date: 2019-04-01
permalink: /posts/blog_collection/
tags:
  - research
---

* The papers on motion planning for autonomous vehicles usually do not mention the nonholonomic constraints, for example: <cite>[1] Trajectory planning for bertha—a local, continuous method</cite>, <cite>[2] A real-time motion planner with trajectory optimization for autonomous vehicles</cite>, why??
> Is that because the planned trajectory is smooth, and it is implicitly assumed that there exist a controller to steer the car to follow the trajectory. (as long as the path curvture is within the limit of the car's max/min steering angle)

> Or because the front wheels and rear wheels have different orientation. $\dot{x_r}sin\theta_r - \dot{y_r}cos\theta_r=0$ only describe the nonholonomic constraint on rear wheels (or car body, since their orientations are the same), here $x_r,y_r,\theta_r$ are the position of some point on rear wheel axis, and the orientation of rear wheel. For the front wheels, $\dot{x_f}sin\theta_f - \dot{y_f}cos\theta_f=0$ should hold, $x_f,y_f,\theta_f$ are the position of some point on front wheel axis, and the orientation of front wheel. Notice that $x_r \neq x_f, y_r \neq y_f$.
* 