---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** [[Sets and Functions]]
**Up Next:** [[Bounds and Completeness]]

___

## 1. Number Systems & Rational Numbers ($\mathbb{Q}$)

The system of real numbers $\mathbb{R}$ is constructed hierarchically by resolving the structural and algebraic deficiencies of simpler number sets:

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$$

### Formal Construction of $\mathbb{Q}$

Formally, the set of rational numbers $\mathbb{Q}$ is defined as the set of equivalence classes of ordered pairs $(p, q)$ under the equivalence relation $(p_1, q_1) \sim (p_2, q_2) \iff p_1 q_2 = p_2 q_1$:

$$\mathbb{Q} = \left\{ \frac{p}{q} \;\middle\vert{}\; p, q \in \mathbb{Z},\, q \neq 0 \right\}$$


- **Arithmetic Closure:** $\mathbb{Q}$ forms an algebraic field; it's closed under the operations of addition $(+)$, subtraction $(-)$, multiplication $(\cdot)$, and division $(\div)$ by non-zero elements.
- **Density Property:** $\mathbb{Q}$ is dense in itself. Between any two distinct rational numbers $a, b \in \mathbb{Q}$ with $a < b$, there exists a rational number $c \in \mathbb{Q}$ such that $a < c < b$.

#### **Example: Midpoint Construction for Density**

> Let $a = \frac{1}{3}$ and $b = \frac{1}{2}$.
> Taking their arithmetic mean yields:
> $$c = \frac{a + b}{2} = \frac{\frac{1}{3} + \frac{1}{2}}{2} = \frac{\frac{5}{6}}{2} = \frac{5}{12}$$
> Since $5, 12 \in \mathbb{Z}$, $c = \frac{5}{12} \in \mathbb{Q}$, and $\frac{1}{3} < \frac{5}{12} < \frac{1}{2}$.

## 2. Incompleteness of $\mathbb{Q}$: Proof of the Irrationality of $\sqrt{2}$

Despite its density, $\mathbb{Q}$ contains "metric gaps." It lacks the necessary elements to measure continuous geometric lengths, such as the diagonal of a unit square.

### Rigorous Proof (by Contradiction)

> **Proof: $\sqrt{2} \notin \mathbb{Q}$** 
> **Assumption:** Suppose $\sqrt{2} \in \mathbb{Q}$. Then there exist coprime integers $p, q \in \mathbb{Z}$($q \neq 0$) such that:
>    $$\sqrt{2} = \frac{p}{q} \quad \text{where } \gcd(p, q) = 1$$ 
> Squaring both sides and multiplying by $q^2$:
>    $$2 = \frac{p^2}{q^2} \implies p^2 = 2q^2 \quad \text{--- (Equation 1)}$$
> Since $p^2 = 2q^2$, $p^2$ is an even integer.
>    - **Lemma:** If $n^2$ is even for $n \in \mathbb{Z}$, then $n$ must be even.
>        - _Proof of Lemma:_ If $n$ were odd ($n = 2k + 1$), then $n^2 = (2k+1)^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$, which is odd. By contrapositive, if $n^2$ is even, $n$ must be even.
>     
>    Applying the lemma, $p$ is even. Thus, we write $p = 2k$ for some integer $k \in \mathbb{Z}$.
>    
> Substitute $p = 2k$ back into Equation 1:
>    $$(2k)^2 = 2q^2 \implies 4k^2 = 2q^2 \implies q^2 = 2k^2$$
>    By the same lemma, since $q^2$ is even, **$q$ must also be even**.
>    
> **Contradiction:** Because both $p$ and $q$ are even, $2$ divides both $p$ and $q$ ($\gcd(p, q) \ge 2$), directly contradicting the initial condition that $\gcd(p, q) = 1$.
> 	$$\therefore \sqrt{2} \notin \mathbb{Q} \quad (\text{i.e., } \sqrt{2} \text{ is irrational})$$

> [!tip] The metric gap in $\mathbb{Q}$ can be formally illustrated by considering the set $A = \{ x \in \mathbb{Q} \mid x > 0 \text{ and } x^2 < 2 \}$. Although $A$ is bounded above in $\mathbb{Q}$ (e.g., by $2$), there is **no rational number** $m \in \mathbb{Q}$ that acts as the precise "least upper bound" (supremum) for $A$. This deficiency directly motivates the construction of $\mathbb{R}$.
> 
>   

___

## 3. The Real Number Field $\mathbb{R}$ as an Ordered Field

The real numbers $\mathbb{R}$ are formally defined as an **Ordered Field** $(\mathbb{R}, +, \cdot, <)$.
### Field Axioms

$\mathbb{R}$ is equipped with two binary operations $+: \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ and $\cdot: \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ satisfying:

| **Axiom**          | **Addition (+)**                                      | **Multiplication (⋅)**                                              |
| ------------------ | ----------------------------------------------------- | ------------------------------------------------------------------- |
| **Closure**        | $\forall a, b \in \mathbb{R},\; a + b \in \mathbb{R}$ | $\forall a, b \in \mathbb{R},\; a \cdot b \in \mathbb{R}$           |
| **Associativity**  | $(a + b) + c = a + (b + c)$                           | $(a \cdot b) \cdot c = a \cdot (b \cdot c)$                         |
| **Commutativity**  | $a + b = b + a$                                       | $a \cdot b = b \cdot a$                                             |
| **Identity**       | $\exists 0 \in \mathbb{R} \text{ s.t. } a + 0 = a$    | $\exists 1 \in \mathbb{R} \text{ s.t. } 1 \neq 0, \; a \cdot 1 = a$ |
| **Inverses**       | $\forall a, \exists (-a) \text{ s.t. } a + (-a) = 0$  | $\forall a \neq 0, \exists a^{-1} \text{ s.t. } a \cdot a^{-1} = 1$ |
| **Distributivity** | $a \cdot (b + c) = a \cdot b + a \cdot c$}            |                                                                     

### Order Axioms

There exists a strict total order relation $<$ on $\mathbb{R}$ satisfying:

1. **Trichotomy:** For any $a, b \in \mathbb{R}$, exactly one of $a < b$, $a = b$, or $a > b$ holds.    
2. **Transitivity:** $(a < b \land b < c) \implies a < c$.
3. **Additive Compatibility:** $a < b \implies a + c < b + c$.
4. **Multiplicative Compatibility:** $(a < b \land c > 0) \implies a \cdot c < b \cdot c$.

___

## 4. Absolute Value & Fundamental Inequalities

### Absolute Value Definition

The absolute value function $\vert{}\cdot\vert{}: \mathbb{R} \to [0, \infty)$ measures distance on the real number line:

$$\vert{}x\vert{} = \begin{cases} x & \text{if } x \ge 0 \\ -x & \text{if } x < 0 \end{cases}$$

### Key Operational Properties

1. **Non-negativity:** $\vert{}x\vert{} \ge 0$, and $\vert{}x\vert{} = 0 \iff x = 0$
2. **Multiplicativity:** $\vert{}x \cdot y\vert{} = \vert{}x\vert{} \cdot \vert{}y\vert{}$
3. **Symmetry:** $\vert{}x - y\vert{} = \vert{}y - x\vert{}$

### Triangle Inequalities

> **Proof: Triangle Inequality ($\vert{}a + b\vert{} \le \vert{}a\vert{} + \vert{}b\vert{}$)**
> 
> From the definition of absolute value, $-\vert{}a\vert{} \le a \le \vert{}a\vert{}$ and $-\vert{}b\vert{} \le b \le \vert{}b\vert{}$.
> 
> Adding these two inequalities together:
> $$-(\vert{}a\vert{} + \vert{}b\vert{}) \le a + b \le \vert{}a\vert{} + \vert{}b\vert{} \iff \vert{}a + b\vert{} \le \vert{}a\vert{} + \vert{}b\vert{}$$
> **Proof: Reverse Triangle Inequality ($\vert{}\vert{}a\vert{} - \vert{}b\vert{}\vert{} \le \vert{}a - b\vert{}$)**
> 
> 1. Express $\vert{}a\vert{} = \vert{}(a - b) + b\vert{}$. Applying the triangle inequality:
>    $$\vert{}a\vert{} \le \vert{}a - b\vert{} + \vert{}b\vert{} \implies \vert{}a\vert{} - \vert{}b\vert{} \le \vert{}a - b\vert{}$$ 
> 2. Similarly, express $\vert{}b\vert{} = \vert{}(b - a) + a\vert{}$:
>    $$\vert{}b\vert{} \le \vert{}a - b\vert{} + \vert{}a\vert{} \implies -(\vert{}a\vert{} - \vert{}b\vert{}) \le \vert{}a - b\vert{}$$
> 3. Combining both results gives:
>    $$-\vert{}a - b\vert{} \le \vert{}a\vert{} - \vert{}b\vert{} \le \vert{}a - b\vert{} \iff \vert{}\vert{}a\vert{} - \vert{}b\vert{}\vert{} \le \vert{}a - b\vert{}$$ 

### Bernoulli's Inequality

For any real number $x \ge -1$ and integer $n \ge 0$:

$$(1 + x)^n \ge 1 + nx$$

> **Proof: Bernoulli's Inequality (via Induction)**
>  
> - **Base Case ($n = 0$):**
>    $(1 + x)^0 = 1$ and $1 + 0(x) = 1$. Since $1 \ge 1$, the base case holds.
>     
> - **Inductive Hypothesis:** Assume $(1 + x)^k \ge 1 + kx$ holds for an integer $k \ge 0$.
>     
> - **Inductive Step:** Prove $(1 + x)^{k+1} \ge 1 + (k + 1)x$.
>     Since $x \ge -1$, it follows that $(1 + x) \ge 0$. Multiply both sides of the inductive hypothesis by $(1 + x)$:
>     $$(1 + x)^{k+1} = (1 + x)^k (1 + x) \ge (1 + kx)(1 + x)$$
>     Expanding the right-hand side:
> 	   $$(1 + kx)(1 + x) = 1 + x + kx + kx^2 = 1 + (k + 1)x + kx^2$$
>     Since $k \ge 0$ and $x^2 \ge 0$, the term $kx^2 \ge 0$. Dropping $kx^2$ yields:
>     $$1 + (k + 1)x + kx^2 \ge 1 + (k + 1)x$$
>     $$\therefore (1 + x)^{k+1} \ge 1 + (k + 1)x$$
>     By induction, Bernoulli's inequality holds for all $n \ge 0$.

> [!tip] Bernoulli's inequality is a fundamental analytic estimate used extensively in limits and sequence analysis to establish bound convergence without computing full binomial expansions.