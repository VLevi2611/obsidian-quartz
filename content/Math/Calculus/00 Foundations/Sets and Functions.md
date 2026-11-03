---
tags:
  - concept
  - math
  - calculus
---
**Up Next:** [[The Real Numbers]]  

---

## 1. Mathematical Logic & Set Operations

### Fundamental Logic Symbols
* **Universal Quantifier ($\forall$):** "For all" or "for every".
* **Existential Quantifier ($\exists$):** "There exists at least one".
* **Implication ($\implies$):** Statement $A$ implies statement $B$.
* **Logical Equivalence / Biconditional ($\iff$):** "If and only if".

### Standard Number Sets ($\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$)
* **$\mathbb{N}$ (Natural Numbers):** $\{1, 2, 3, \dots\}$
* **$\mathbb{Q}$ (Rational Numbers):** $\left\{ \frac{p}{q} \;\middle|\; p, q \in \mathbb{Z},\, q \neq 0 \right\}$
* **$\mathbb{R}$ (Real Numbers):** All continuous values along the number line.
* **$\mathbb{C}$ (Complex Numbers):** Numbers of the form $a + bi$ where $i^2 = -1$.

### Set Operations
For two sets $A$ and $B$:
* **Union ($A \cup B$):** $\{ x \mid x \in A \lor x \in B \}$
* **Intersection ($A \cap B$):** $\{ x \mid x \in A \land x \in B \}$
* **Set Difference ($A \setminus B$):** $\{ x \mid x \in A \land x \notin B \}$
* **Complement ($A^c$ or $A'$):** $\{ x \in U \mid x \notin A \}$ where $U$ is the universal set.

---

## 2. Mathematical Induction & Binomial Theorem

### Mathematical Induction
Used to prove a statement $P(n)$ for all natural numbers $n \ge n_0$:
1. **Base Case:** Prove $P(n_0)$ holds true.
2. **Inductive Hypothesis:** Assume $P(k)$ is true for an arbitrary integer $k \ge n_0$.
3. **Inductive Step:** Prove that $P(k) \implies P(k+1)$.

### Newton's Binomial Theorem
For any real numbers $a, b$ and non-negative integer $n$:
$$(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^k$$
Where the binomial coefficient is defined as:
$$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$

---

## 3. Core Concept: Functions

### Formal Definition & Representation
A function $f: X \to Y$ is a rule that assigns to **each** input $x$ in the domain $X$ **exactly one** output $y = f(x)$ in the range/codomain $Y$[cite: 1].

A function is represented in three primary ways:
1. **Formula:** $y = f(x)$ (e.g., $y = x^2$ or $y = 2^x$)[cite: 1].
2. **Graph:** Set of pairs $(x, y)$ plotted on coordinate axes[cite: 1].
3. **Input-Output Pairs / Mapping:** Formal mapping of domain inputs to range outputs[cite: 1].