---
title: "Sampling-based methods for motion planning with constraints"
date: 2021-03-25
# excerpt: "Notes on RRT-connect paper<br/><img src='/images/500x300.png'>"
collection: portfolio
---

This paper considers geometrical constraints that reduce the number of degrees of freedom. 

Such a constraint defines a lower dimensional manifold in the configuration space.
$$X = \{q \in Q|F(q)=0\}$$
$F(q)$ is the constraint function. An example of such constraint is keeping the EE at some orientation during the motion.

Since the constraint manifold is a lower dimensional space embedded in the C-space, the relative measure (volume) is zero compared to C-space. Therefore, randomly sampled configuration will not lie on the constraint manifold. Basically, there are mainly five approaches to handle the constraints:
* Relaxation: set a tolerance which increases the volume of constraint space. It's like adding additional dimensions to the constraint manifold.
* Projection: Use the Jacobian of $F(q)$ to reduce the error (distance) to the constraint manifold.
* Tangent space: Locally linearize the manifold at the current configuration.
* Atlas: Use a set of linearized planes to approximate the manifold?
* Reparameterization: Only applicable to some special cases.

To be continued...

### Reference
Kingston, Zachary, Mark Moll, and Lydia E. Kavraki. "Sampling-based methods for motion planning with constraints." Annual review of control, robotics, and autonomous systems 1 (2018): 159-185.
