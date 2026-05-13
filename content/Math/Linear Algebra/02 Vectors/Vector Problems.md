---
tags:
  - problem
  - easy
  - math
  - linear-algebra
---
## [[Vector Addition]]

### Question 1

What's the sum of $\vec a+ \vec b+ \vec c=$ 

#### Given

$$
\begin{aligned}
\vec a &= (1,2,5) \\
\vec b &= (-2,3,3) \\
\vec c &= (0,1,2)
\end{aligned}
$$
#### Solution

To sum vectors, sum their corresponding components
$$
\vec a+\vec b+\vec c
=
(1-2+0,\;2+3+1,\;5+3+2)
=
(-1,6,10)
$$

## [[Scalar Multiplication]]

### Question 1

What's the product $5 \vec x$ 
#### Given

$$
\vec x = (2,3,3)
$$
#### Solution

To multiply a vector by a scalar, multiply each component by that scalar
$$
\begin{aligned}
a \vec x &= \sum_{i = 1}^{n} a x_i \\
5 \vec x &= (5 \times 2, 5 \times 3, 5 \times 3) = (10,15,15)
\end{aligned}
$$

## [[Dot Product]]

### Question 1

What's the dot product $\vec a \cdot \vec b$
#### Given

$$\begin{aligned}
\vec a &= (9,5,-4,2) \\ 
\vec b &= (-3,-2,7,-1)
\end{aligned}$$
#### Solution

To solve a dot product, multiply the corresponding components and sum them.
$$\begin{aligned}
\vec a \cdot \vec b &= \sum_{i = 1} a_i b_i \\
\vec a \cdot \vec b &= -27 - 10 - 28 - 2 = -67
\end{aligned}$$

### Question 2

What's the dot product $\mathbf{a \cdot b}$ 

#### Given

Given the size of $\mathbf{a,b}$, and the size of the angle between them is $\theta$  
$$\begin{array}{l}
|\mathbf{a}| = 5 \\
|\mathbf{b}| = \frac{3}{7} \\
\theta = \frac{\pi}{12}
\end{array}$$
#### Solution

Recall the other way to solve a dot product
$$\begin{array}{l}
\mathbf{a \cdot b} = |\mathbf{a}| |\mathbf{b}| \cos(\theta) \\
\mathbf{a \cdot b} = 5 \times \frac{3}{7} \times \cos (\frac{\pi}{12}) = 2.0698
\end{array}$$

## [[Orthogonal Vectors]]

### Question 1

Check if $\mathbf{x,y}$ are orthogonal

#### Given

$$\begin{array}{l}
\mathbf{x} = (1,2) \\
\mathbf{y} = (-1,2)
\end{array}$$
#### Solution

2 vectors are orthogonal if their dot product is 0 
$$\begin{array}{l}
\mathbf{x \cdot y} = 1 \times -1 + 2 \times 2 = 3 \\
\mathbf{x \not \perp y}
\end{array}$$

## [[Length (Norm)]]

### Question 1

What is the length of $\mathbf{x}$

#### Given

$$\mathbf{x} = (1,2,3,7)$$
#### Solution

Length of a vector is calculated by the square root of the dot product with itself
$$\begin{array}{l}
|\mathbf{x}| = \sqrt{\mathbf{x \cdot x}} \\
|\mathbf{x}| = \sqrt{1^2 + 2^2 + 3^2 + 7^2} = \sqrt{63}
\end{array}$$