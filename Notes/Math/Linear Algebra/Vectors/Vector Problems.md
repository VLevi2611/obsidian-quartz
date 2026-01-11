---
tags:
  - problem
  - easy
  - math
  - linear-algebra
---
## [[Vector Addition]]

### Question 1

whats the sum of $\mathbf{a+b+c}$ 

#### Given

$$\begin{array}{l}
\mathbf{a}=(1,2,5) \\
\mathbf{b}=(-2,3,3) \\
\mathbf{c}=(0,1,2)
\end{array}$$
#### Solution

To sum vectors, sum their corresponding components
$$\begin{array}{l}
\sum_{i=1}^{n}\mathbf{v}=\sum_{j=1}^{m}\mathbf{v}_{i,j} \\
\mathbf{a+b+c}=(1-2+0,2+3+1,5+3+2)=(-1)
\end{array}$$
## [[Dot Product]]

### Question 1

whats the dot product $\mathbf{a \cdot b}$
#### Given

$$\begin{array}{l}
\mathbf{a}=(9,5,-4,2) \\ 
\mathbf{b}=(-3,-2,7,-1)
\end{array}$$
#### Solution

To solve a dot product, multiply the corresponding components and sum them.
$$\begin{array}{l}
\mathbf{a \cdot b}=\sum_{i=1}^{4}a_ib_i \\
\mathbf{a \cdot b}=-27-10-28-2=67
\end{array}$$

### Question 2

whats the dot product $\mathbf{a \cdot b}$ 

#### Given

Given the size of $\mathbf{a,b}$, and the size of the angle between them is $\theta$  
$$\begin{array}{l}
|\mathbf{a}|=5 \\
|\mathbf{b}|=\frac{3}{7} \\
\theta=\frac{\pi}{12}
\end{array}$$
#### Solution

Recall the other way to solve a dot product
$$\begin{array}{l}
\mathbf{a \cdot b}=|\mathbf{a}||\mathbf{b}|\cos(\theta) \\
\mathbf{a \cdot b}=5 \times \frac{3}{7} \times \cos (\frac{\pi}{12})=2.0698
\end{array}$$