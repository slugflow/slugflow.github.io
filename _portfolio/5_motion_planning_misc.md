---
title: "Motion planning and control Misc."
# excerpt: "Notes on RRT-connect paper<br/><img src='/images/500x300.png'>"
collection: portfolio
---

* The notion of configuration space is the key insight to Lagrangian mechanics of rigid bodies, as it allows dynamics to be expressed using the precise degrees of freedom of a body. [1]

* Why are bidirectional RRTs better for getting out of "bug trap"? [1] Intuitively, extending the nearest node in the sampled nodes (most of them are within the trap) to $q_{rand}$, is very likely to hit the "bug trap" wall (convex), but extending from another side (concave) will be easier. Because the trap looks differently (opposite) from another side.
* **Linear-quadratic regulator**. A continuous-time linear system:
  $$\dot{x}=Ax+Bu$$
  with a quadratic cost function defined as:
  $$J=x^T(t_1)F(t_1)x(t_1)+\int_{t_0}^{t_1}(x^TQx+u^Ru+2x^TNu)dt$$

* Breadth-first search: explores all the neighbor nodes at the present depth prior to moving on to the nodes at the next depth level. Depth-first search: explores the node branch as far as possible before being forced to backtrack and expand other nodes.
* A*, D*
* Pfaffian constraints.
  
[1] Steven M. Lavalle. Motion Planning: The Essentials


<span style="color:blue">To be continued...</span>
