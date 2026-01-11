---
tags:
  - problem
  - easy
  - medium
  - hard
  - exam-level
---
## [[Matrix Vector Multiplication]]

### Question 1

Whats the product of $\mathbf{Ax}$
#### Given

$$\begin{array}{l}
\mathbf{A} = \begin{pmatrix}
1 & 3 & 2 \\
2 & 2 & 1 \\
0 & 2 & 4
\end{pmatrix} \\
\mathbf{x} = (1,0,1)^T
\end{array}$$
#### Solution

To multiply a [[Matrix]] and a [[Vector]], do a [[Dot Product]] for each row with the vector
$$\mathbf{Ax}=\begin{pmatrix}
1 \times 1 + 3 \times 0 + 2 \times 1 \\
2 \times 1 + 2 \times 0 + 1 \times 1 \\
0 \times 1 + 2 \times 0 + 4 \times 1
\end{pmatrix}=
\begin{pmatrix}
3 \\
3 \\
4
\end{pmatrix}$$

## [[Matrix Multiplication]]

### Question 1

Whats the product of $\mathbf{AB}$

#### Given

$$\begin{array}{l}
\mathbf{A} = \begin{pmatrix}
1 & 3 \\
2 & 1
\end{pmatrix} \\
\mathbf{B} = \begin{pmatrix}
2 & 2 \\
0 & 1
\end{pmatrix}
\end{array}$$
#### Solution

To multiply 2 matrix, multiply $\mathbf{A}$ by each column of $\mathbf{B}$
$$\begin{array}{l}
\mathbf{AB} = \begin{pmatrix}
(1 \times 2) + (3 \times 0) & (1 \times 2) + (3 \times 1) \\
(2 \times 2) + (1 \times 0) & (2 \times 2) + (1 \times 1)
\end{pmatrix} \\
\mathbf{AB} = \begin{pmatrix}
2 & 5 \\
4 & 5
\end{pmatrix}
\end{array}$$

## [[Determinant]]

### Question 1

What is the determinant of $\mathbf{A}$

#### Given

$$\mathbf{A} = \begin{pmatrix}
1 & 2 \\
4 & 4
\end{pmatrix}$$
#### Solution

To calculate the determinant of a $2 \times 2$ matrix
$$\begin{array}{l}
|\mathbf{A}| = a_{11} a_{22} - a_{21} a_{12} \\
\begin{vmatrix}
1 & 2 \\
4 & 4
\end{vmatrix} = 
4 - 8 = -4
\end{array}$$

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
+ 3
\end{array}$$