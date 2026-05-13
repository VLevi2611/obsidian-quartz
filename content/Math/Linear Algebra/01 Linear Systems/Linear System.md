---
tags:
  - concept
  - math
  - linear-algebra
---
## Overview

A **linear system** is a combination of two or more equation that shares the same variables.
For each number of equations they can take a different [[Geometric Interpretation]]:
- $\mathbb{R}^2$ - 2 equations representing 2 lines.
- $\mathbb{R}^3$ - 3 equations representing 3 planes.
- $\mathbb{R}^n$ - $n$ equations representing $n$ hyperplanes.
For each case, we want to solve for the variables inside.
There can be 3 different ways a system can behave:
1. It has one [[Unique Solution]].
2. It has infinitely many solutions.
3. It has no solution.
---
A linear system can be represented in a few different ways.
1. with curly brackets that unite some equations:
$$
\begin{cases}
3x + 2y - z = 1 & (1) \\
2x - 2y + 4z = -2 & (2) \\
-x + \frac{1}{2}y - z = 0 & (3)
\end{cases}
$$
2. in a [[Matrix Representation]]:
$$A \vec x = \vec b$$
Where $A$ is the coefficients [[Matrix]], $\vec x$ is the variable [[Vector]] and $\vec b$ is the results vector.

