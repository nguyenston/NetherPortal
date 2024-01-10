---
tags:
  - Analysis
title: Metric spaces
---
A metric space is an ordered pair $(M,d)$ where $M$ is a set and $d:M\times M\to \mathbb{R}$ is a distance measure (i.e. metric) on $M$. 
A distance measure satisfies the following conditions for all $x,y,z\in M$:
* $d(x,x)=0$
* If $x\neq y$, then $d(x,y)>0$
* $d(x,y)=d(y,x)$
* $d(x,z)\leq d(x,y)+d(y,z)$