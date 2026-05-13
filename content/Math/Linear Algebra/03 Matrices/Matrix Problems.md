---
tags:
  - problem
  - easy
  - math
  - linear-algebra
---
## [[Matrix Vector Multiplication]]

### Question 1

Whats the product of $\mathbf{A} \vec x$
#### Given

$$
\begin{aligned}
\mathbf{A} &= \begin{pmatrix}
1 & 3 & 2 \\
2 & 2 & 1 \\
0 & 2 & 4
\end{pmatrix} \\
\vec x &= (1,0,1)^T
\end{aligned}
$$
#### Solution

To multiply a [[Matrix]] and a [[Vector]], do a [[Dot Product]] for each row with the vector
$$
\mathbf{A} \vec x = \begin{pmatrix}
1 \times 1 + 3 \times 0 + 2 \times 1 \\
2 \times 1 + 2 \times 0 + 1 \times 1 \\
0 \times 1 + 2 \times 0 + 4 \times 1
\end{pmatrix} =
\begin{pmatrix}
3 \\
3 \\
4
\end{pmatrix}
$$

## [[Matrix Multiplication]]

### Question 1

Whats the product of $\mathbf{AB}$

#### Given

$$
\begin{aligned}
\mathbf{A} &= \begin{pmatrix}
1 & 3 \\
2 & 1
\end{pmatrix} \\
\mathbf{B} &= \begin{pmatrix}
2 & 2 \\
0 & 1
\end{pmatrix}
\end{aligned}
$$
#### Solution

To multiply 2 matrix, multiply $\mathbf{A}$ by each column of $\mathbf{B}$
$$
\begin{aligned}
\mathbf{AB} &= \begin{pmatrix}
(1 \times 2) + (3 \times 0) & (1 \times 2) + (3 \times 1) \\
(2 \times 2) + (1 \times 0) & (2 \times 2) + (1 \times 1)
\end{pmatrix} \\
\mathbf{AB} &= \begin{pmatrix}
2 & 5 \\
4 & 5
\end{pmatrix}
\end{aligned}
$$

## [[Determinant]]

### Question 1

What is the determinant of $\mathbf{A}$

#### Given

$$
\mathbf{A} = \begin{pmatrix}
1 & 2 \\
4 & 4
\end{pmatrix}
$$
#### Solution

To calculate the determinant of a $2 \times 2$ matrix
$$
\begin{aligned}
|\mathbf{A}| = a_{11} a_{22} - a_{21} a_{12} \\
\begin{vmatrix}
1 & 2 \\
4 & 4
\end{vmatrix} = 
4 - 8 = -4
\end{aligned}$$

### Question 2

What is the determinant of $\mathbf{A}$

#### Given

$$\mathbf{A} = \begin{pmatrix}
1 & 2 & 3 \\
4 & 4 & 2 \\
2 & 1 & 2
\end{pmatrix}$$
#### Solution

To calculate the determinant of a $3 \times 3$ matrix
1. calculate the determinant of its minors
2. multiply each determinant with the component of that minor
3. sum all of them
$$\begin{array}{l}
\begin{vmatrix}
1 & 2 & 3 \\
4 & 4 & 2 \\
2 & 1 & 2 
\end{vmatrix} = 
1 \times \begin{vmatrix}
4 & 2 \\
1 & 2
\end{vmatrix}
+ 2 \times \begin{vmatrix}
4 & 2 \\
2 & 2
\end{vmatrix}
+ 3 \times \begin{vmatrix}
4 & 4 \\
2 & 1
\end{vmatrix} \\
\begin{vmatrix}
1 & 2 & 3 \\
4 & 4 & 2 \\
2 & 1 & 2 
\end{vmatrix} = 6 + 8 - 12 = 2
\end{array}$$

## [[Inverse Matrix]]

### Question 1

Whats the inverse of the matrix $\mathbf{A}$

#### Given

$$\mathbf{A} = \begin{pmatrix}
1 & 3 \\
3 & 2
\end{pmatrix}$$
#### Solution

To solve for the inverse
1. check if the determinant is not 0
2. create an augmented matrix (the matrix on the left and the [[Identity Matrix]] on the right)
3. manipulate the matrix to create the identity matrix on the left
4. the inverse is the matrix on the right
$$\begin{array}{l}
\begin{vmatrix}
1 & 3 \\
3 & 2
\end{vmatrix} = -7 \not =0 \\
\left (
\begin{array}{cc|cc}
1 & 3 & 1 & 0 \\
3 & 2 & 0 & 1
\end{array}
\right ) \\
\left (
\begin{array}{cc|cc}
1 & 3 & 1 & 0 \\
0 & -7 & -3 & 1
\end{array}
\right ) \\
\left (
\begin{array}{cc|cc}
1 & 3 & 1 & 0 \\
0 & 1 & \frac{3}{7} & \frac{1}{7}
\end{array}
\right ) \\
\left (
\begin{array}{cc|cc}
1 & 0 & -\frac{2}{7} & -\frac{3}{7} \\
0 & 1 & \frac{3}{7} & \frac{1}{7}
\end{array}
\right ) \\
\mathbf{A}^{-1} = \frac{1}{7} \begin{pmatrix} 
-2 & -3 \\
3 & 1
\end{pmatrix}
\end{array}$$

## [[Cramer's Rule]]

### Question 1

Find $\mathbf{x}$ in $\mathbf{Ax=b}$
#### Given

$$\begin{array}{l}
\mathbf{A} = \begin{pmatrix}
1 & 3 \\
1 & 2
\end{pmatrix} \\
\mathbf{b} = \begin{pmatrix}
2 \\
1
\end{pmatrix}
\end{array}$$
#### Solution

Using Cramer's rule $$\begin{array}{l}
x_i = \frac{\det \mathbf{A}_i}{\det \mathbf{A}} \\
\det \mathbf{A} = 2 - 3 = -1 \\
\det \mathbf{A}_1 = \begin{vmatrix}
2 & 3 \\
1 & 2
\end{vmatrix} = 1 \\
\det \mathbf{A}_2 = \begin{vmatrix}
1 & 2 \\
1 & 1
\end{vmatrix} = -1 \\
x_1 = -1 \\
x_2 = 1
\end{array}$$