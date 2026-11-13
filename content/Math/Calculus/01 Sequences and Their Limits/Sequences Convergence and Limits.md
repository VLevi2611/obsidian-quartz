---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** [[Bounds and Completeness]]
**Up Next:** [[Bolzano-Weierstrass Theorem]] 

---

## Definition

A **sequence** $(a_n)$ is a function whose domain is the set of natural numbers. It **converges** to a real number $L$ if, for every arbitrarily small positive tolerance $\epsilon > 0$, there exists a corresponding integer index $N$ such that for all terms where $n > N$, the distance between $a_n$ and $L$ is strictly less than $\epsilon$. If a sequence does not approach a finite, unique limit, it **diverges** (either to $\pm\infty$ or by oscillating). 

#### Core Equation

**Formal $\epsilon-N$ Definition:**
$$ \forall \epsilon > 0, \exists N \in \mathbb{N} \text{ such that } n > N \implies |a_n - L| < \epsilon $$

**Cauchy Sequence Definition:**
A sequence converges if and only if its terms become arbitrarily close to each other as the sequence progresses (in the real numbers, every Cauchy sequence is convergent):
$$ \forall \epsilon > 0, \exists N \in \mathbb{N} \text{ such that } \forall m,n > N \implies |a_m - a_n| < \epsilon $$

#### Properties

* **Uniqueness:** If $\lim_{n \to \infty} a_n = L_1$ and $\lim_{n \to \infty} a_n = L_2$, then $L_1 = L_2$.
* **Boundedness:** Every convergent sequence is bounded above and below by real numbers. However, a bounded sequence is not necessarily convergent (e.g., $a_n = (-1)^n$).
* **Monotone Convergence Theorem:** Every bounded, monotonic (strictly non-decreasing or non-increasing) sequence converges to a limit. 
* **Algebra of Limits:** If $a_n \to L$ and $b_n \to M$:
  * **Addition/Subtraction:** $\lim_{n \to \infty} (a_n \pm b_n) = L \pm M$
  * **Multiplication:** $\lim_{n \to \infty} (a_n \cdot b_n) = L \cdot M$
  * **Division:** $\lim_{n \to \infty} \left(\frac{a_n}{b_n}\right) = \frac{L}{M}$, provided $M \neq 0$ and $b_n \neq 0$.
* **Squeeze (Sandwich) Theorem:** If $a_n \leq b_n \leq c_n$ for all $n \geq N$, and $\lim_{n \to \infty} a_n = \lim_{n \to \infty} c_n = L$, then $\lim_{n \to \infty} b_n = L$.
* **Subsequences:** If a sequence converges to $L$, every subsequence extracted from it also converges to $L$.

#### Evaluation Techniques

* **Continuous Analog (L'Hôpital's Rule):** If $f(n) = a_n$ and $f(x)$ is a differentiable continuous function, you can evaluate $\lim_{x \to \infty} f(x)$ using L'Hôpital's rule. If the continuous limit equals $L$, the sequence limit equals $L$.
* **Ratio Test for Sequences:** If $\lim_{n \to \infty} \left| \frac{a_{n+1}}{a_n} \right| = c < 1$, then $a_n \to 0$.
* **Root Limit:** $\lim_{n \to \infty} \sqrt[n]{n} = 1$ and $\lim_{n \to \infty} x^{1/n} = 1$ (for $x > 0$).

