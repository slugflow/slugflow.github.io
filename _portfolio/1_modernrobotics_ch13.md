---
title: "Modern Robotics: Mechanics, Planning, and Control (Chapter 13)"
# excerpt: "Notes on RRT-connect paper<br/><img src='/images/500x300.png'>"
collection: portfolio
---

Wheeled mobile robots may be classified in two major categories, omnidirectional and nonholonomic. We focus on nonholonomic mobile robots in the rest of the note.

### Modeling of nonholonomic wheeled mobile robots
* Unicycle 
* Differential-drive robots: **Note that both the bicycle model and diff-drive mobile robot have two non-omnidirectional wheels, but the former has two independent nonholonomic constraints (for front and rear wheels) while the later only has one. Because the two wheels are aligned along the same axis, two nonholonomic constraints on two wheels are equivalent.**
* Car-like robots

### Controlability
**Definition:** A robot is controllable from $q$ if, for any $q_{goal}$, there exists a control trajectory $u(t)$ that drives the robot from $q$ to $q_{goal}$ in finite time $T$. The robot is small-time locally accessible (STLA) from $q$ if, for any dimensional subset of the configuration space. The robot is small-time locally time $T > 0$ and any neighborhood $W$, the reachable set $R^W (q, ≤ T)$ is a full- controllable (STLC) from $q$ if, for any time $T > 0$ and any neighborhood W, the reachable set $R^W(q, ≤ T)$ is a neighborhood of $q$.

Given a time T > 0 and a neighborhood $W$ of an initial
configuration $q$, the reachable set of configurations from $q$ at time $T$ by feasible trajectories remaining inside W is defined as $R^W(q, T)$, and the reachable set is defined as:

$R^W(q, ≤ T)=\bigcup_{0 \leq t \leq T} R^W(q, t)$

### Motion planning


#### Reference
[1] Lynch, Kevin M., and Frank C. Park. Modern Robotics. Cambridge University Press, 2017.

[2] Siegwart, Roland, Illah Reza Nourbakhsh, and Davide Scaramuzza. Introduction to autonomous mobile robots. MIT press, 2011.

<span style="color:blue">To be continued...</span>