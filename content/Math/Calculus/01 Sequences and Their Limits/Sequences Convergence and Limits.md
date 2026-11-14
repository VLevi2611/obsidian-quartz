---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** [[Bounds and Completeness]]
**Up Next:** [[Bolzano-Weierstrass Theorem]]
___

## 1. Formal Definition of a Sequence & Convergence

A real sequence is an ordered list of real numbers indexed by the natural numbers. Formally, a sequence $(a_n)_{n=1}^\infty$ is a function $a: \mathbb{N} \to \mathbb{R}$, where $a(n) = a_n$.

### Formal Limit Definition ($\epsilon-N$ Definition)

A sequence $(a_n)$ converges to a real limit $L \in \mathbb{R}$ (written $\lim_{n \to \infty} a_n = L$ or $a_n \to L$) if:

$$\forall \epsilon > 0, \; \exists N \in \mathbb{N} \text{ such that } \forall n > N, \; \vert{}a_n - L\vert{} < \epsilon$$

- **Geometric Interpretation:** For any given margin of error $\epsilon > 0$, there exists a cutoff index $N$ beyond which all terms $a_n$ are trapped within the open interval $(L - \epsilon, L + \epsilon)$.
- **Divergence:** A sequence is divergent if it fails to approach any finite limit $L$.
- **Divergence to Infinity ($\pm\infty$):**
$$\lim_{n \to \infty} a_n = \infty \iff \forall M > 0, \; \exists N \in \mathbb{N} \text{ such that } \forall n > N, \; a_n > M$$
 $$\lim_{n \to \infty} a_n = -\infty \iff \forall M > 0, \; \exists N \in \mathbb{N} \text{ such that } \forall n > N, \; a_n < -M$$


#### **Example:** **$\epsilon-N$ Proof of Convergence**

>Prove using the $\epsilon-N$ definition that $\lim_{n \to \infty} \frac{2n + 1}{n + 3} = 2$.
>**Proof:** Let $\epsilon > 0$ be given. We analyze the distance $\vert{}a_n - L\vert{}$:
$$\vert{}a_n - 2\vert{} = \left\vert{} \frac{2n + 1}{n + 3} - 2 \right\vert{} = \left\vert{} \frac{2n + 1 - (2n + 6)}{n + 3} \right\vert{} = \left\vert{} \frac{-5}{n + 3} \right\vert{} = \frac{5}{n + 3}$$>
>
>We require $\frac{5}{n + 3} < \epsilon \iff n + 3 > \frac{5}{\epsilon} \iff n > \frac{5}{\epsilon} - 3$. By the Archimedean Property, choose $N = \left\lceil \frac{5}{\epsilon} - 3 \right\rceil$ (or $N = \lfloor \frac{5}{\epsilon} \rfloor$). For all $n > N$, we have $n > \frac{5}{\epsilon} - 3 \implies \frac{5}{n+3} < \epsilon \implies \left\vert{}\frac{2n+1}{n+3} - 2\right\vert{} < \epsilon$.$\therefore \lim_{n \to \infty} \frac{2n+1}{n+3} = 2$.


>[!tip] **Finding the threshold $N$:** Always work backward from $\vert{}a_n - L\vert{} < \epsilon$ to isolate $n$, then use the Archimedean Property to choose $N(\epsilon) \in \mathbb{N}$.

  ___
## 2. Limit Arithmetic & Basic Properties

### Core Structural Properties

1. **Uniqueness of Limits:** If a sequence converges, its limit is unique.
    
	**Proof of Uniqueness:** Assume $a_n \to L_1$ and $a_n \to L_2$ with $L_1 \neq L_2$. Choose $\epsilon = \frac{\vert{}L_1 - L_2\vert{}}{2} > 0$.
	By convergence, $\exists N_1$ s.t. (Such that) $\forall n > N_1, \vert{}a_n - L_1\vert{} < \epsilon$, and $\exists N_2$ s.t. $\forall n > N_2, \vert{}a_n - L_2\vert{} < \epsilon$. For $n > \max(N_1, N_2)$, the triangle inequality gives: $$\vert{}L_1 - L_2\vert{} = \vert{}(L_1 - a_n) + (a_n - L_2)\vert{} \le \vert{}a_n - L_1\vert{} + \vert{}a_n - L_2\vert{} < \epsilon + \epsilon = \vert{}L_1 - L_2\vert{}$$
    This yields $\vert{}L_1 - L_2\vert{} < \vert{}L_1 - L_2\vert{}$, a contradiction. Thus $L_1 = L_2$.   
    
2. **Boundedness of Convergent Sequences:** Every convergent sequence is bounded.


>[!tip] The converse is false: bounded sequences are not necessarily convergent (example: $a_n = (-1)^n$ is bounded by $1$ but diverges due to oscillation).

  
### Algebraic Limit Laws

If $\lim_{n \to \infty} a_n = L$ and $\lim_{n \to \infty} b_n = M$:

- **Sum / Difference:** $\lim_{n \to \infty} (a_n \pm b_n) = L \pm M$
- **Scalar Multiple:** $\lim_{n \to \infty} (c \cdot a_n) = c \cdot L$ for any constant $c \in \mathbb{R}$
- **Product Rule:** $\lim_{n \to \infty} (a_n \cdot b_n) = L \cdot M$
- **Quotient Rule:** $\lim_{n \to \infty} \left(\frac{a_n}{b_n}\right) = \frac{L}{M}$, provided $M \neq 0$ and $b_n \neq 0$ for all $n$

### Order Preservation

If $a_n \le b_n$ for all $n \ge N_0$ and both limits exist, then $\lim_{n \to \infty} a_n \le \lim_{n \to \infty} b_n$.

---

## 3. Strategic Master Guide: Visual Cues & Core Limit Methods

Choosing the right tool for limits of sequences can feel like guessing if you don't know what to look for. Every limit problem leaves specific visual "fingerprints" or cues that tell you exactly which method to deploy:

### 1. Multiplying by the Conjugate

- **Visual Cue:** You see a subtraction sign between two square roots: $\sqrt{A} - \sqrt{B}$ (often leading to an indeterminate form like $\infty - \infty$).

- **When to Use:** Whenever algebraic manipulation or factoring won't easily cancel out square roots. This forces the roots into a difference of squares ($a^2 - b^2$), eliminating the square roots in the numerator.

- **The Trick:** If it looks like $\sqrt{\text{expr}} - \sqrt{\text{expr}}$, treat it as a fraction over $1$ and multiply the numerator and denominator by $\left(\sqrt{A} + \sqrt{B}\right)$.

### 2. Factoring Out the Dominant Term

- **Visual Cue:** You are dealing with polynomials divided by polynomials, or multiple exponential/power terms added together inside an $n$-th root (e.g., $\sqrt[n]{87^n + 17^n}$).

- **When to Use:**  
    - For rational functions, divide everything by the highest power of $n$ in the denominator.
    - For $n$-th roots of sums, factor out the term with the largest base or highest growth rate from inside the radical.

- **The Trick:** Look at the bases of exponents (e.g., $87^n$ vs $17^n$) or the highest degrees of $n$. The "strongest" term completely overpowers the others, sending fractions like $\left(\frac{17}{87}\right)^n$ straight to $0$.

### 3. The Squeeze (Sandwich) Theorem

- **Visual Cue:** You see a sum of $n$ terms where the denominator changes with $k$ (e.g., $\sum_{k=1}^n \frac{1}{48n^2 + 15k}$), or a complex expression you can't algebraically simplify directly.

- **When to Use:** When a direct limit is impossible because terms depend on a running index $k$, or when you need to rigorously prove a limit by trapping it between two simpler functions.

- **The Trick:**  
    - _For sums:_ To find the lower bound, replace every term with the smallest possible term (largest denominator) and multiply by $n$. To find the upper bound, replace every term with the largest possible term (smallest denominator) and multiply by $n$.
    - Both bounds must converge to the exact same number.

### 4. The Bounded $\times$ Infinitesimal Rule

- **Visual Cue:** You spot a trigonometric function like $\sin(n)$, $\cos(n)$, or an exponential trig term like $e^{\sin(n)}$ multiplied by or divided by an algebraic expression containing $n$.

- **When to Use:** Whenever a term oscillates infinitely and has no limit on its own (like sine).

- **The Trick:** Do not panic when you see $\sin$ or $\cos$. Separate the expression into two parts:  
    1. The oscillating part, which you state is bounded (e.g., $-1 \le \sin(n) \le 1$).
    2. The algebraic fraction, which you evaluate as $n \to \infty$. If the fraction goes to $0$, the whole limit automatically equals $0$ (Bounded $\times$ Zero = Zero).

---
## 4. Monotonic Sequences & Key Standard Limits

### Monotone Convergence Theorem (MCT)

Every monotonic sequence of real numbers that is bounded converges to a finite limit.

- **Non-decreasing:** If $a_{n+1} \ge a_n$ for all $n$ and $a_n \le M$, then $\lim_{n \to \infty} a_n = \sup\{a_n \mid n \in \mathbb{N}\}$.

- **Non-increasing:** If $a_{n+1} \le a_n$ for all $n$ and $a_n \ge m$, then $\lim_{n \to \infty} a_n = \inf\{a_n \mid n \in \mathbb{N}\}$.


### Construction of Euler's Constant ($e$)

Consider the sequence $a_n = \left(1 + \frac{1}{n}\right)^n$.

1. **Monotonicity:** By Bernoulli's inequality or AM-GM, $(a_n)$ is strictly increasing: $a_{n+1} > a_n$.

2. **Boundedness:** By expanding via the Binomial Theorem:
$$\left(1 + \frac{1}{n}\right)^n = \sum_{k=0}^n \binom{n}{k} \frac{1}{n^k} = 1 + 1 + \sum_{k=2}^n \frac{1}{k!} \left(1 - \frac{1}{n}\right)\dots\left(1 - \frac{k-1}{n}\right) < 1 + 1 + \sum_{k=2}^n \frac{1}{2^{k-1}} < 3$$
3. By MCT, the limit exists and defines Euler's constant:
$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n \approx 2.71828\dots$$

### Benchmark Limit Hierarchy

| **Sequence Limit**             | **Formula**                           | **Condition / Value**                                                                                                                                   |     |
| ------------------------------ | ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | --- |
| **Geometric Sequence**         | $\lim_{n \to \infty} q^n$             | $\begin{cases} 0 & \text{if } \Vert{}q\Vert{} < 1 \\ 1 & \text{if } q = 1 \\ \infty & \text{if } q > 1 \\ \text{DNE} & \text{if } q \le -1 \end{cases}$ |     |
| **Constant Root**              | $\lim_{n \to \infty} \sqrt[n]{c}$     | $1 \quad (\forall c > 0)$                                                                                                                               |     |
| **Root of $n$**                | $\lim_{n \to \infty} \sqrt[n]{n}$     | $1$                                                                                                                                                     |     |
| **Polynomial vs. Exponential** | $\lim_{n \to \infty} \frac{n^k}{a^n}$ | $0 \quad (\forall k > 0, a > 1)$                                                                                                                        |     |
| **Exponential vs. Factorial**  | $\lim_{n \to \infty} \frac{a^n}{n!}$  | $0 \quad (\forall a \in \mathbb{R})$                                                                                                                    |     |
| **Factorial vs. Power Scale**  | $\lim_{n \to \infty} \frac{n!}{n^n}$  | $0$                                                                                                                                                     |     |

>[!tip] **Asymptotic Growth Scale** (from slowest to fastest growth as $n \to \infty$):
$$\ln(n) \ll n^k \ll a^n \ll n! \ll n^n \quad (\text{for } k > 0, a > 1)$$

---
## 5. Subsequences & Structural Theorems

### Subsequence Definition & Inheritance

Given a sequence $(a_n)$, a subsequence $(a_{n_k})_{k=1}^\infty$ is formed by choosing an infinite subset of indices using a strictly increasing index sequence $n_1 < n_2 < n_3 < \dots$

- **Subsequence Inheritance Property:** If $(a_n)$ converges to $L$, then **every** subsequence $(a_{n_k})$ also converges to $L$.

- **Divergence Criterion:** If a sequence $(a_n)$ contains two subsequences that converge to different limits, $(a_n)$ diverges.
