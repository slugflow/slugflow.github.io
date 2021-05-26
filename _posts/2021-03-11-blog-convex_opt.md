---
title: 'Why is convex optimization important?'
date: 2021-03-11
permalink: /posts/convex_optimization/
tags:
  - convex function
  - convex optimization
---

### Definition of convex function
> For all ${ 0\leq t \leq 1}$ and all ${ x_{1},x_{2}\in X,}$ 
> ${ f\left(tx_{1}+(1-t)x_{2}\right)~\leq ~tf\left(x_{1}\right)+(1-t)f\left(x_{2}\right).}$
### Quadratic forms and Convexity
> Quadratic form in variables ${ x_1,x_2..., x_n}$ is a polynomial function $Q$, where all the terms in $Q(x_1, x_2,..., x_n)$ have order two. Quadratic functions $\neq$ convex functions.
>
> Let $Q(x_1, x_2,..., x_n)=\boldsymbol{x}^TA\boldsymbol{x}$ be a quadratic form in n variables, $A$ is an sysmetric matrix, then:
> * $Q$ is convex/concave $\iff$ $A$ is positive/negative semidefinite
> * $Q$ is strictly convex/concave $\iff$ $A$ is positive/negative definite

### Convex optimization:
1. Objective function is convex.
2. Constraint functions are convex.


### Why is convex optimization fast? 
Although convex optimization in general is NP hard <cite>[1]</cite>..
1. A local minima is guaranteed to be a global minima. 
2. Separation Theorem?

If the objective function is convex but constraint functions are not, then we can not guarantee a local minima to be a global minima due to the feasible region defined by the nonconvex constraints.

The following figure illustrates the optimization for a convex objective function. The white regions are defined by convex constraints and the red region is defined by nonconvex constraints. Intuitively, we understand the local minima within the red region (feasible region of nonconvex constraints) is not necessarily a global minima.

<img src='/images/posts/convex_opt.png' height = 300>
<img src='/images/posts/nonlinear_constraints.png' height = 300>

<span style="color:blue">To be continued...</span>

#### Reference
[1] Manyem, Prabhu. "Duality Gap, Computational Complexity and NP Completeness: A Survey." arXiv preprint arXiv:1012.5568 (2010).
