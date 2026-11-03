---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** [[Sets and Functions]]
**Up Next:** [[Bounds and completeness]]

___
## 1. Number System Hierarchy & Construction of Rational Numbers ($\mathbb{Q}$)

The real line $\mathbb{R}$ is constructed hierarchically by resolving the structural deficiencies of simpler number systems:

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$$
### The Set of Rational Numbers

Formally, $\mathbb{Q}$ is defined as the set of equivalence classes of ordered pairs $(p, q)$ under the equivalence relation $(p_1, q_1) \sim (p_2, q_2) \iff p_1 q_2 = p_2 q_1$:

$$\mathbb{Q} = \left\{ \frac{p}{q} \;\middle\vert{}\; p, q \in \mathbb{Z},\, q \neq 0 \right\}$$


- **Arithmetic Closure:** $\mathbb{Q}$ forms an algebraic field; it is closed under addition ($+$), subtraction ($-$), multiplication ($\cdot$), and division ($\div$) by non-zero elements.
- **Density Property:** $\mathbb{Q}$ is dense in itself. For any $a, b \in \mathbb{Q}$ with $a < b$, there exists $c \in \mathbb{Q}$ such that $a < c < b$ (e.g., $c = \frac{a+b}{2}$).
---

## 2. Incompleteness of $\mathbb{Q}$ & Discovery of Irrationals

Despite density, $\mathbb{Q}$ contains "holes" or metric gaps. It lacks the property required to represent continuous geometric lengths (e.g., the diagonal of a unit square).

### Rigorous Proof: Irrationality of $\sqrt{2}$

1. **Assumption (Contradiction Setup):**
    Suppose $\sqrt{2} \in \mathbb{Q}$. Then there exist coprime integers $p, q \in \mathbb{Z}$ with $q \neq 0$ such that:
    $$\sqrt{2} = \frac{p}{q} \quad \text{where } \gcd(p, q) = 1$$
    
2. Squaring both sides and multiplying by $q^2$:
    $$2 = \frac{p^2}{q^2} \implies p^2 = 2q^2 \quad \text{--- (Equation 1)}$$
    
3. Since $p^2 = 2q^2$, $p^2$ is an even integer.
    > **Lemma:** If $n^2$ is even for $n \in \mathbb{Z}$, then $n$ must be even.
    > _Proof of Lemma:_ If $n$ were odd, $n = 2k + 1 \implies n^2 = 4k^2 + 4k + 1 = 2(2k^2 + 2k) + 1$, which is odd. By contrapositive, if $n^2$ is even, $n$ is even.
    
    Applying the lemma, $p$ is even. Thus, write $p = 2k$ for some integer $k \in \mathbb{Z}$.
    
4. Substitute $p = 2k$ into Equation 1:
    $$(2k)^2 = 2q^2 \implies 4k^2 = 2q^2 \implies q^2 = 2k^2$$
    
    By the same lemma, since $q^2$ is even, **$q$ must also be even**.
    
1. **Contradiction:**
    If both $p$ and $q$ are even, $2$ divides both $p$ and $q$ ($\gcd(p, q) \ge 2$), directly contradicting the initial condition that $\gcd(p, q) = 1$.

$$\therefore \sqrt{2} \notin \mathbb{Q} \quad \text{i.e., } \sqrt{2} \text{ is irrational.}$$

### The Metric Gap in $\mathbb{Q}$

Consider the set $A = \{ x \in \mathbb{Q} \mid x > 0 \text{ and } x^2 < 2 \}$. While $A$ is bounded above in $\mathbb{Q}$ (e.g., by $2$), **there is no rational number $m \in \mathbb{Q}$ that serves as the precise "least upper bound" for $A$**. This deficit necessitates the construction of $\mathbb{R}$.

---

## 3. The Ordered Field Structure of $\mathbb{R}$

The real numbers $\mathbb{R}$ are defined algebraically as an **Ordered Field** $(\mathbb{R}, +, \cdot, <)$.
### A. Field Axioms

$\mathbb{R}$ possesses two binary operations $+: \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ and $\cdot: \mathbb{R} \times \mathbb{R} \to \mathbb{R}$ satisfying:

  

| **Axiom**         | **Addition (+)**                                      | **Multiplication (⋅)**                                              |
| ----------------- | ----------------------------------------------------- | ------------------------------------------------------------------- |
| **Closure**       | $\forall a, b \in \mathbb{R},\; a + b \in \mathbb{R}$ | $\forall a, b \in \mathbb{R},\; a \cdot b \in \mathbb{R}$           |
| **Associativity** | $(a + b) + c = a + (b + c)$                           | $(a \cdot b) \cdot c = a \cdot (b \cdot c)$                         |
| **Commutativity** | $a + b = b + a$                                       | $a \cdot b = b \cdot a$                                             |
| **Identity**      | $\exists 0 \in \mathbb{R} \text{ s.t. } a + 0 = a$    | $\exists 1 \in \mathbb{R} \text{ s.t. } 1 \neq 0, \; a \cdot 1 = a$ |
| **Inverses**      | $\forall a, \exists (-a) \text{ s.t. } a + (-a) = 0$  | $\forall a \neq 0, \exists a^{-1} \text{ s.t. } a \cdot a^{-1} = 1$ |
**distributivity** $a \cdot (b + c) = a \cdot b + a \cdot c$

### B. Order Axioms

There exists a strict total order relation $<$ on $\mathbb{R}$ satisfying:

1. **Trichotomy:** For any $a, b \in \mathbb{R}$, exactly one of the following holds:
	$$a < b, \quad a = b, \quad \text{or} \quad a > b$$
    
2. **Transitivity:**
    $$\forall a, b, c \in \mathbb{R}, \quad (a < b \land b < c) \implies a < c$$
    
3. **Additive Compatibility:**
    $$\forall a, b, c \in \mathbb{R}, \quad a < b \implies a + c < b + c$$
    
4. **Multiplicative Compatibility:**
    $$\forall a, b, c \in \mathbb{R}, \quad (a < b \land c > 0) \implies a \cdot c < b \cdot c$$
    

## 4. Absolute Value, Metrics & Fundamental Inequalities

### Formal Definition of Absolute Value

The absolute value function $\vert{}\cdot\vert{}: \mathbb{R} \to [0, \infty)$ measures distance on the real line:

  

$$\vert{}x\vert{} = \begin{cases} x & \text{if } x \ge 0 \\ -x & \text{if } x < 0 \end{cases}$$

### Key Operational Properties

1. **Non-negativity:** $\vert{}x\vert{} \ge 0$, and $\vert{}x\vert{} = 0 \iff x = 0$
    
      
    
2. **Multiplicativity:** $\vert{}x \cdot y\vert{} = \vert{}x\vert{} \cdot \vert{}y\vert{}$
    
      
    
3. **Symmetry:** $\vert{}x - y\vert{} = \vert{}y - x\vert{}$
    
      
    

### Triangle Inequalities & Algebraic Proofs

1. **Standard Triangle Inequality:**
    
      
    
    $$\forall a, b \in \mathbb{R}, \quad \vert{}a + b\vert{} \le \vert{}a\vert{} + \vert{}b\vert{}$$
    
    _Proof:_ Since $-\vert{}a\vert{} \le a \le \vert{}a\vert{}$ and $-\vert{}b\vert{} \le b \le \vert{}b\vert{}$, add the inequalities to get:
    
      
    
    $$-(\vert{}a\vert{} + \vert{}b\vert{}) \le a + b \le \vert{}a\vert{} + \vert{}b\vert{} \iff \vert{}a + b\vert{} \le \vert{}a\vert{} + \vert{}b\vert{}$$
    
2. **Reverse Triangle Inequality:**
    
      
    
    $$\forall a, b \in \mathbb{R}, \quad \vert{}\vert{}a\vert{} - \vert{}b\vert{}\vert{} \le \vert{}a - b\vert{}$$
    
    _Proof:_ Express $\vert{}a\vert{} = \vert{}(a - b) + b\vert{} \le \vert{}a - b\vert{} + \vert{}b\vert{} \implies \vert{}a\vert{} - \vert{}b\vert{} \le \vert{}a - b\vert{}$.
    
      
    
    Similarly, $\vert{}b\vert{} = \vert{}(b - a) + a\vert{} \le \vert{}a - b\vert{} + \vert{}a\vert{} \implies -(\vert{}a\vert{} - \vert{}b\vert{}) \le \vert{}a - b\vert{}$.
    
      
    
    Combining these yields $\vert{}\vert{}a\vert{} - \vert{}b\vert{}\vert{} \le \vert{}a - b\vert{}$.
    
      
    

### Bernoulli's Inequality (Inductive Proof)

For any real number $x \ge -1$ and any integer $n \in \mathbb{N} \cup \{0\}$:

  

$$(1 + x)^n \ge 1 + nx$$

  

- **Base Case ($n = 0$):** $(1 + x)^0 = 1 \ge 1 + 0(x) = 1$. (Holds true).
    
      
    
- **Inductive Hypothesis:** Assume $(1 + x)^k \ge 1 + kx$ holds for some $k \ge 0$.
    
      
    
- **Inductive Step:** Prove for $n = k + 1$. Since $x \ge -1$, we have $(1 + x) \ge 0$:
    
      
    
    $$(1 + x)^{k+1} = (1 + x)^k (1 + x) \ge (1 + kx)(1 + x)$$
    
    Expanding the right side:
    
      
    
    $$(1 + kx)(1 + x) = 1 + x + kx + kx^2 = 1 + (k + 1)x + kx^2$$
    
    Since $k \ge 0$ and $x^2 \ge 0$, the term $kx^2 \ge 0$. Dropping it preserves or weakens the inequality:
    
      
    
    $$1 + (k + 1)x + kx^2 \ge 1 + (k + 1)x$$
    
    $$\therefore (1 + x)^{k+1} \ge 1 + (k + 1)x$$
    
    By induction, Bernoulli's inequality holds for all $n \ge 0$.
    
      
    

## 🔗 Related Notes & Links

- **Previous Topic:** `[[Sets-and-Functions]]`
    
      
    
- **Next Topic:** `[[Bounds-and-Completeness]]` (Supremum, Infimum, Archimedean Property, and Completeness Axiom)
    
      
    
- **Folder Location:** `Math/Calculus/00-Foundations/The-Real-Numbers`
    
      
    

Would you like to move on to creating the next note in the sequence—`[[Bounds-and-Completeness]]`—or tweak any section in this expanded template first?