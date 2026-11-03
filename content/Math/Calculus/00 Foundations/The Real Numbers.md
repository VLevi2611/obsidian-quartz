---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** [[Sets and Functions]]  
**Up Next:** [[Bounds and completeness]]  

---

## 1. Number Systems & Rational Numbers ($\mathbb{Q}$)

The system of real numbers $\mathbb{R}$ builds on simpler number sets:

$$\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R}$$

### The Set of Rational Numbers
A rational number is defined as the quotient of two integers:

$$\mathbb{Q} = \left\{ \frac{p}{q} \;\middle|\; p, q \in \mathbb{Z},\, q \neq 0 \right\}$$

* **Arithmetic Closure:** $\mathbb{Q}$ is closed under addition, subtraction, multiplication, and division by non-zero elements.
* **Density Property:** Between any two distinct rational numbers, there exists another rational number (e.g., their average).

---

## 2. Incompleteness of $\mathbb{Q}$: Proof of the Irrationality of $\sqrt{2}$

Despite its density, $\mathbb{Q}$ contains "gaps." There is no rational number whose square equals $2$.

### Proof (by Contradiction)
1. **Assumption:** Suppose $\sqrt{2} \in \mathbb{Q}$. Then it can be written as a reduced fraction:
   $$\sqrt{2} = \frac{p}{q} \quad \text{where } p, q \in \mathbb{Z},\; q \neq 0, \text{ and } \gcd(p, q) = 1 \text{ (coprime)}$$

2. Squaring both sides yields:
   $$2 = \frac{p^2}{q^2} \implies p^2 = 2q^2$$

3. Since $p^2 = 2q^2$, $p^2$ is even. This implies that **$p$ must be even** (if $p$ were odd, $p^2$ would be odd).
   Since $p$ is even, write $p = 2k$ for some integer $k$.

4. Substitute $p = 2k$ back into the equation:
   $$(2k)^2 = 2q^2 \implies 4k^2 = 2q^2 \implies q^2 = 2k^2$$

5. Since $q^2 = 2k^2$, $q^2$ is even, which implies **$q$ must also be even**.

6. **Contradiction:**
   Both $p$ and $q$ are even, so they share a common factor of $2$. This contradicts the initial condition that $\gcd(p, q) = 1$.

$$\therefore \sqrt{2} \notin \mathbb{Q} \quad (\text{i.e., } \sqrt{2} \text{ is irrational})$$

---

## 3. The Real Number Field $\mathbb{R}$ as an Ordered Field

The real numbers $\mathbb{R}$ form an **ordered field**—a set equipped with two binary operations ($+$ and $\cdot$) and an order relation ($<$) satisfying specific axioms:

### Field Axioms
For all $a, b, c \in \mathbb{R}$:
* **Associativity:** $(a + b) + c = a + (b + c)$ and $(a \cdot b) \cdot c = a \cdot (b \cdot c)$
* **Commutativity:** $a + b = b + a$ and $a \cdot b = b \cdot a$
* **Distributivity:** $a \cdot (b + c) = a \cdot b + a \cdot c$
* **Identities:** $a + 0 = a$ and $a \cdot 1 = a$
* **Inverses:** $a + (-a) = 0$, and if $a \neq 0$, $a \cdot a^{-1} = 1$

### Order Axioms
For an order relation $<$:
* **Trichotomy:** For any $a, b \in \mathbb{R}$, exactly one of $a < b$, $a = b$, or $a > b$ holds.
* **Transitivity:** $a < b$ and $b < c \implies a < c$.
* **Compatibility with Operations:**
  * $a < b \implies a + c < b + c$
  * $a < b$ and $c > 0 \implies a \cdot c < b \cdot c$

---

## 4. Absolute Value & Inequalities

### Absolute Value Definition
The absolute value $|x|$ represents the distance of $x$ from $0$ on the real line:

$$|x| = \begin{cases} x & \text{if } x \ge 0 \\ -x & \text{if } x < 0 \end{cases}$$

### Key Properties & Triangle Inequalities
1. **Non-negativity:** $|x| \ge 0$, and $|x| = 0 \iff x = 0$
2. **Multiplicativity:** $|x \cdot y| = |x| \cdot |y|$
3. **Triangle Inequality:**
   $$|a + b| \le |a| + |b|$$
4. **Reverse Triangle Inequality:**
   $$||a| - |b|| \le |a - b|$$

### Bernoulli's Inequality
For any real number $x \ge -1$ and integer $n \ge 0$:

$$(1 + x)^n \ge 1 + nx$$


---

## 🔗 Related Notes & Links
* **Previous Topic:** `[[Sets-and-Functions]]`
* **Next Topic:** `[[Bounds-and-Completeness]]` (Supremum, Infimum, and the Completeness Axiom)[cite: 2]
* **Folder Location:** `Math/Calculus/00-Foundations/The-Real-Numbers`