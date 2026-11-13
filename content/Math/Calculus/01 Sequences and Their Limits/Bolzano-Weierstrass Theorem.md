---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** [[Sequences Convergence and Limits]]
**Up Next:** [[Cauchy Criterion]]

---

## Definition

The Bolzano-Weierstrass Theorem is a fundamental result in real analysis and calculus. It states that every infinite, bounded sequence of real numbers has at least one convergent subsequence. This theorem is a cornerstone for understanding the topology of the real line and acts as a bridge between boundedness and convergence. 

#### Core Equation

**Formal Statement:**
Let $(a_n)$ be a sequence in $\mathbb{R}$. If there exists a real number $M > 0$ such that for all $n \in \mathbb{N}$:
$$ |a_n| \leq M $$
Then there exists a subsequence $(a_{n_k})$ and a real number $L \in \mathbb{R}$ such that:
$$ \lim_{k \to \infty} a_{n_k} = L $$

#### Properties

* **Reliance on Completeness:** The theorem is deeply tied to the completeness of the real numbers. It would not hold in the rational numbers ($\mathbb{Q}$), as a bounded sequence of rationals might converge to an irrational number (like $\sqrt{2}$), meaning the limit doesn't exist within $\mathbb{Q}$.
* **Proof by Bisection:** The standard proof relies on the Nested Intervals Theorem, repeatedly dividing the bounded interval $[ -M, M ]$ in half and picking the half that contains infinitely many terms of the sequence, effectively "trapping" a subsequence into a converging point.
* **Higher Dimensions:** The theorem generalizes to $\mathbb{R}^n$. A sequence of vectors in $\mathbb{R}^n$ that is bounded in magnitude will also have a convergent subsequence.

