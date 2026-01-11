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
\mathbf{A}=\begin{pmatrix}
1 & 3 & 2 \\
2 & 2 & 1 \\
0 & 2 & 4
\end{pmatrix} \\
\mathbf{x}=(1,0,1)^T
\end{array}$$
#### Solution

To multiply a [[Matrix]] and a [[Vector]], do a [[Dot Product]] for each row with the vector
$$\mathbf{Ax}=\begin{pmatrix}
1 \times 1 + 3 \times 0 + 2 \times 1 \\
2 \times 1 + 2 \times 0 + 1 \times 1 \\
0 \times 1 + 2 \times 0 + 4 \times 1
\end{pmatrix}$$