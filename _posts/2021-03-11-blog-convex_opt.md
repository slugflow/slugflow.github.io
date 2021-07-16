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
### Quadratic programming (QP)
General form of QP:
$$\underset{x} {\text{min}} \quad x^TGx+x^Tc$$
subject to:
$$a_i^Tx=b_i, i \in \mathcal{E}$$
$$a_j^Tx \geq b_j, j \in \mathcal{I}$$
i.e., a quadratic objective and linear constraints.

With KKT conditions, we can find the optimal solution by solving the linear equations (the derivative of quadratic equations). There exist efficient solvers for linear equations, thus QP is popular and important??


### Sequential Quadratic Programming (SQP)
SQP is a special case of SCP. Core idea: approximation by QP, and iteratively solve a sequence of QP until convergence.
1. At the current solution, approximate the objective with a quadratic function (if it is not), and linearize the nonlinear constraints (keep the linear ones). In addition to the original constraints, we have the trust region constraints to ensure the approximation is reasonable.
2. Solve the approximated QP to obtain a new solution, the solution is the start for the next iteration.
3. Repeat (1) and (2) at the new solution until some convergence criteria is satisfied.


### Convex optimization:
1. Objective function is convex.
2. Constraint functions are convex.


### Convex optimization properties: 
1. A local minima is guaranteed to be a global minima. 
2. A certificate of infeasibility is provided when a feasible solution does not exist.
3. The runtime complexity is polynomial in the problem size <cite>[1]</cite>. Convex optimization in general is NP hard <cite>[2]</cite>?

If the objective function is convex but constraint functions are not, then we can not guarantee a local minima to be a global minima due to the feasible region defined by the nonconvex constraints.

The following figure illustrates the optimization for a convex objective function. The white regions are defined by convex constraints and the red region is defined by nonconvex constraints. Intuitively, we understand the local minima within the red region (feasible region of nonconvex constraints) is not necessarily a global minima.

<img src='/images/posts/convex_opt.png' height = 300>
<img src='/images/posts/nonlinear_constraints.png' height = 300>

<span style="color:blue">To be continued...</span>

#### Reference
[1] Danylo Malyuta, et. al, "Convex Optimization for Trajectory Generation"
[2] Manyem, Prabhu. "Duality Gap, Computational Complexity and NP Completeness: A Survey." arXiv preprint arXiv:1012.5568 (2010).
