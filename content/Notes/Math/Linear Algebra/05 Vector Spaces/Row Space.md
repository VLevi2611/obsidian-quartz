---
tags:
  - concept
  - math
  - linear-algebra
---
## Definition

A row space of a [[Matrix]] is a [[Span]] of its [[Row Vector]]s. Similarly to [[Column Space]].

Let $K$ be a [[Field]] of [[Scalar]]s. Let $\mathbf{A}$ be an $m \times n$ matrix, with row vectors $\mathbf{v_1,v_2,...,v}_n$.
A [[Linear Combination]] of these vectors is any vector of the form
$$c_1\mathbf{v}_1+c_2\mathbf{v}_2+...+c_n\mathbf{v}_n$$ The [[Set]] of all possible linear combination is called the row space of $\mathbf{A}$.

## Example

Given $\mathbf{A}=\begin{bmatrix}1 & 0  & 2 \\ 0 & 1 & 0 \end{bmatrix}$
Then the row vectors are $\mathbf{v_1}=\begin{bmatrix} 1 & 0 & 2 \end{bmatrix}$ and $\mathbf{v_2}=\begin{bmatrix} 0 & 1 & 0 \end{bmatrix}$. A linear combination of them is any vector of the form $c_1\begin{bmatrix} 1 & 0 & 2 \end{bmatrix}+c_2\begin{bmatrix} 0 & 1 & 0 \end{bmatrix}=\begin{bmatrix} c_1 & c_2 & 2c_1 \end{bmatrix}$

