---
title: 'Simulated Annealing'
date: 2020-03-28
permalink: /posts/rrt_efficient/
tags:
  - Simulated Annealing
  - Global optimization
---

Simulated Annealing is a **probabilistic** method for **approximating** the **global** optimum of a given function. It is helpful especially in the case of large search space.
* Make use of randomness, random walk on a search graph.
* Transition probabilities..
* Higher probability of accepting worse solutions in the begining (high temperature). 

Pseudocode
```python
Let s = s0 
For k = 0 through kmax (exclusive):
  T ← temperature( (k+1)/kmax )
  Pick a random neighbour, snew ← neighbour(s)
  If P(E(s), E(snew), T) ≥ random(0, 1):
      s ← snew
Output: the final state s
```

Reference:
---

[1] [Simulated Annealing From Scratch in Python](https://machinelearningmastery.com/simulated-annealing-from-scratch-in-python/)  
[2] [Wiki - Simulated annealing](https://en.wikipedia.org/wiki/Simulated_annealing)  
[3] [SA for TSP (code)](https://en.wikipedia.org/wiki/Simulated_annealing)

<span style="color:blue">To be continued...</span>