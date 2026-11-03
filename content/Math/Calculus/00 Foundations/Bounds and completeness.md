---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** [[The Real Numbers]]
**Up Next:** [[01 Sequences and Their Limits]]
___
## 1. Bounded Sets & Extrema

When analyzing subsets of the real numbers $\mathbb{R}$, we need precise language to describe sets that are "constrained" from above or below.

### Boundedness Definitions

Let $S \subseteq \mathbb{R}$ be a non-empty set.

- **Bounded Above:** $S$ is bounded above if there exists a real number $M \in \mathbb{R}$ such that $x \le M$ for all $x \in S$. The number $M$ is called an **upper bound** for $S$.
- **Bounded Below:** $S$ is bounded below if there exists a real number $m \in \mathbb{R}$ such that $x \ge m$ for all $x \in S$. The number $m$ is called a **lower bound** for $S$.
- **Bounded Set:** $S$ is bounded if it is bounded both above and below (equivalently, $\exists K > 0$ such that $\vert{}x\vert{} \le K$ for all $x \in S$).

> [!tip] Upper and lower bounds are **not unique**. If $M$ is an upper bound for $S$, any number $M' > M$ is also an upper bound for $S$.   

### Maximum and Minimum Elements

- **Maximum ($\max S$):** If an upper bound $M$ of $S$ actually belongs to the set ($M \in S$), then $M$ is the **maximum** of $S$.
- **Minimum ($\min S$):** If a lower bound $m$ of $S$ actually belongs to the set ($m \in S$), then $m$ is the **minimum** of $S$.

> **Example:** 
> - For the closed interval $S_1 = [0, 1]$: $\max S_1 = 1$ and $\min S_1 = 0$.
> - For the open interval $S_2 = (0, 1)$: Upper bounds exist (e.g., $1, 2, 3$), but **there is no maximum**because $1 \notin S_2$. Similarly, lower bounds exist, but **there is no minimum** because $0 \notin S_2$.

---
## 2. Supremum & Infimum

To handle sets like $(0, 1)$ that are bounded but lack a maximum or minimum within themselves, we introduce the concept of the _least upper bound_ and _greatest lower bound_.

Let $S \subseteq \mathbb{R}$ be a non-empty set.

1. **Supremum ($\sup S$):** A real number $L = \sup S$ is the **supremum** (or least upper bound) of $S$ if:
    - $L$ is an upper bound of $S$: $\forall x \in S, \; x \le L$.
    - $L$ is the _smallest_ upper bound: If $M$ is any upper bound of $S$, then $L \le M$.
2. **Infimum ($\inf S$):** A real number $l = \inf S$ is the **infimum** (or greatest lower bound) of $S$ if:
    - $l$ is a lower bound of $S$: $\forall x \in S, \; x \ge l$.
    - $l$ is the _largest_ lower bound: If $m$ is any lower bound of $S$, then $l \ge m$.

### The $\epsilon$-Characterization of Supremum and Infimum

These characterizations convert the definition of bounds into actionable algebraic criteria for analysis and proofs:

- **Supremum Criterion:** $L = \sup S \iff$      
    1. $x \le L$ for all $x \in S$.
    2. For every $\epsilon > 0$, there exists at least one $x_\epsilon \in S$ such that $x_\epsilon > L - \epsilon$.
        
- **Infimum Criterion:** $l = \inf S \iff$
    1. $x \ge l$ for all $x \in S$.
    2. For every $\epsilon > 0$, there exists at least one $x_\epsilon \in S$ such that $x_\epsilon < l + \epsilon$.


> **Example: Supremum and Infimum of an Explicit Set**
> 
> Consider the set $S = \left\{ 1 - \frac{1}{n} \;\middle\vert{}\; n \in \mathbb{N} \right\} = \left\{ 0, \frac{1}{2}, \frac{2}{3}, \frac{3}{4}, \dots \right\}$.
> - **Infimum:** $\min S = 0 \implies \inf S = 0$.
> - **Supremum:** $\sup S = 1$.
>     
>    Proof that $\sup S = 1$:
>        For all $n \in \mathbb{N}$, $1 - \frac{1}{n} < 1$, so $1$ is an upper bound.
>        Given any $\epsilon > 0$, choose $n \in \mathbb{N}$ large enough such that $\frac{1}{n} < \epsilon$.
>        Then $1 - \frac{1}{n} > 1 - \epsilon$. Since $1 - \frac{1}{n} \in S$, $1$ is the least upper bound, so $\sup S = 1$. Note that $1 \notin S$, so $S$ has no maximum.

____

## 3. The Axiom of Completeness

The fundamental property that distinguishes $\mathbb{R}$ from $\mathbb{Q}$ (and makes calculus possible) is **Completeness**.

### The Completeness Axiom (Least Upper Bound Property)

Every non-empty set $S \subseteq \mathbb{R}$ that is bounded above has a **supremum in $\mathbb{R}$**($\sup S \in \mathbb{R}$).

### Why $\mathbb{Q}$ Fails Completeness

Recall the set $A = \{ x \in \mathbb{Q} \mid x > 0 \text{ and } x^2 < 2 \}$.
- In $\mathbb{R}$, $A$ is bounded above (e.g., by $2$), and its least upper bound is $\sqrt{2} \in \mathbb{R}$.
- In $\mathbb{Q}$, $A$ is bounded above by rational numbers like $1.5$ or $1.42$, but **it has no least upper bound in $\mathbb{Q}$** because $\sqrt{2} \notin \mathbb{Q}$.
- Thus, $\mathbb{Q}$ contains metric "holes", whereas $\mathbb{R}$ forms a unbroken continuum.
___

## 4. Fundamental Analytical Properties of $\mathbb{R}$

The Axiom of Completeness yields critical consequences that underpin limits and analysis.

### The Archimedean Property

The natural numbers $\mathbb{N}$ are not bounded above in $\mathbb{R}$.

$$\forall x \in \mathbb{R}, \; \exists n \in \mathbb{N} \text{ such that } n > x$$

#### Equivalent Form

$$\forall \epsilon > 0, \; \exists n \in \mathbb{N} \text{ such that } 0 < \frac{1}{n} < \epsilon$$

> **Proof of the Archimedean Property:**
> 
> Assume by contradiction that $\mathbb{N}$ is bounded above. By the Completeness Axiom, $\mathbb{N}$has a supremum $L = \sup \mathbb{N} \in \mathbb{R}$.
> By the $\epsilon$-characterization (choosing $\epsilon = 1$), there exists $m \in \mathbb{N}$ such that:
> $$m > L - 1 \implies m + 1 > L$$
> Since $m \in \mathbb{N}$, $m + 1 \in \mathbb{N}$. But $m + 1 > L$ contradicts the assumption that $L$ is an upper bound for $\mathbb{N}$.
> Therefore, $\mathbb{N}$ is unbounded above.

### Density Theorems

#### 1. Density of Rational Numbers ($\mathbb{Q}$) in $\mathbb{R}$

Between any two distinct real numbers, there exists at least one rational number.

$$\forall a, b \in \mathbb{R} \text{ with } a < b, \quad \exists q \in \mathbb{Q} \text{ such that } a < q < b$$

> **Proof Construction Idea:**
> 
> Since $b - a > 0$, by the Archimedean Property there exists $n \in \mathbb{N}$ such that $\frac{1}{n} < b - a \implies nb - na > 1$.
> 
> The interval $(na, nb)$ has a length greater than $1$, so it must contain an integer $m \in \mathbb{Z}$.
> 
> Thus, $na < m < nb \implies a < \frac{m}{n} < b$. Setting $q = \frac{m}{n} \in \mathbb{Q}$ completes the proof.  

#### 2. Density of Irrational Numbers ($\mathbb{R} \setminus \mathbb{Q}$) in $\mathbb{R}$

Between any two distinct real numbers, there exists at least one irrational number.

$$\forall a, b \in \mathbb{R} \text{ with } a < b, \quad \exists x \in \mathbb{R} \setminus \mathbb{Q} \text{ such that } a < x < b$$

> **Proof Construction Idea:**
> 
> Consider the real numbers $\frac{a}{\sqrt{2}}$ and $\frac{b}{\sqrt{2}}$. By the density of $\mathbb{Q}$, choose a non-zero rational $q \in \mathbb{Q}$ such that:
> $$\frac{a}{\sqrt{2}} < q < \frac{b}{\sqrt{2}} \implies a < q\sqrt{2} < b$$
> Since $q$ is a non-zero rational and $\sqrt{2}$ is irrational, $x = q\sqrt{2}$ is irrational, giving an irrational between $a$ and $b$.

## 5. Summary Comparison Table

|**Set S**|**Bounded Above?**|**Bounded Below?**|**supS**|**infS**|**maxS**|**minS**|
|---|---|---|---|---|---|---|
|$[a, b]$|Yes ($M \ge b$)|Yes ($m \le a$)|$b$|$a$|$b$|$a$|
|$(a, b)$|Yes ($M \ge b$)|Yes ($m \le a$)|$b$|$a$|None|None|
|$\{ \frac{1}{n} \mid n \in \mathbb{N} \}$|Yes|Yes|$1$|$0$|$1$|None|
|$\{ x \in \mathbb{Q} \mid x^2 < 2 \}$|Yes|Yes|$\sqrt{2}$|$-\sqrt{2}$|None|None|
|$\mathbb{N}$|No|Yes|None|$1$|None|$1$|
|$\mathbb{R}$|No|No|None|None|None|None|