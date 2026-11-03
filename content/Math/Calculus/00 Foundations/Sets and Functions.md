---
tags:
  - concept
  - math
  - calculus
---
**Up Next:** [[The Real Numbers]]

___
## 1. Mathematical Logic & Set Operations

### Fundamental Logic Symbols

- **Universal Quantifier ($\forall$):** "For all" or "for every".
- **Existential Quantifier ($\exists$):** "There exists at least one".
- **Implication ($A \implies B$):** Statement $A$ implies statement $B$ ($A$ is a _sufficient_ condition for $B$,$B$ is a _necessary_ condition for $A$).
- **Logical Equivalence / Biconditional ($A \iff B$):** "If and only if".

### Standard Number Systems ($\mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}$)

- **$\mathbb{N}$ (Natural Numbers):** $\{1, 2, 3, \dots\}$
- **$\mathbb{Z}$ (Integers):** $\{\dots, -2, -1, 0, 1, 2, \dots\}$
- **$\mathbb{Q}$ (Rational Numbers):** $\left\{ \frac{p}{q} \;\middle\vert{}\; p, q \in \mathbb{Z},\, q \neq 0 \right\}$
- **$\mathbb{R}$ (Real Numbers):** Continuous continuum of all rational and irrational values along the number line.
- **$\mathbb{C}$ (Complex Numbers):** Numbers of the form $a + bi$ where $a,b \in \mathbb{R}$ and $i^2 = -1$.

### Set Operations & Interval Notations

For two sets $A$ and $B$ within a universal set $U$:

- **Union ($A \cup B$):** $\{ x \mid x \in A \lor x \in B \}$
- **Intersection ($A \cap B$):** $\{ x \mid x \in A \land x \in B \}$
- **Set Difference ($A \setminus B$):** $\{ x \mid x \in A \land x \notin B \}$
- **Complement ($A^c$ or $A'$):** $\{ x \in U \mid x \notin A \}$.

#### Interval Notation Types:

- **Closed Interval $[a, b]$:** Endpoints included ($\{x \in \mathbb{R} \mid a \le x \le b\}$).
- **Open Interval $(a, b)$:** Endpoints excluded ($\{x \in \mathbb{R} \mid a < x < b\}$).
- **Half-Open / Infinite Intervals:** E.g., $[0, \infty)$ includes all non-negative real numbers $x \ge 0$.

## 2. Proof Techniques: Induction & Binomial Theorem

### Mathematical Induction

Used to prove a statement $P(n)$ for all integers $n \ge n_0$:
1. **Base Case:** Prove $P(n_0)$ holds true.
2. **Inductive Hypothesis:** Assume $P(k)$ is true for an arbitrary integer $k \ge n_0$.
3. **Inductive Step:** Prove that $P(k) \implies P(k+1)$.

> **Worked Example: Sum of the First $n$ Integers**
> 
> **Claim:** $P(n): \sum_{j=1}^n j = 1 + 2 + \dots + n = \frac{n(n+1)}{2}$.
> 
> - **Base Case ($n=1$):** $\sum_{j=1}^1 j = 1$. Using the formula: $\frac{1(1+1)}{2} = 1$. The base case holds.
>
> - **Inductive Hypothesis:** Assume $P(k)$ is true for $k \ge 1$:
>     $$1 + 2 + \dots + k = \frac{k(k+1)}{2}$$
> - **Inductive Step:** Show $P(k+1)$ is true:
>     $$\begin{aligned} > 1 + 2 + \dots + k + (k+1) &= \frac{k(k+1)}{2} + (k+1) \\ > &= (k+1)\left( \frac{k}{2} + 1 \right) \\ > &= (k+1)\left( \frac{k+2}{2} \right) = \frac{(k+1)((k+1)+1)}{2} > \end{aligned}$$
>     
>     Thus, $P(k) \implies P(k+1)$, completing the proof by induction.

### Newton's Binomial Theorem

For any non-negative integer $n$:

$$(a + b)^n = \sum_{k=0}^{n} \binom{n}{k} a^{n-k} b^k, \quad \text{where } \binom{n}{k} = \frac{n!}{k!(n-k)!}$$

## 3. Core Concept: Functions

### Formal Definition & Representations

A function $f: X \to Y$ is a rule that assigns to **each** input $x$ in the domain $X$ **exactly one** output $y = f(x)$in the range/codomain $Y$.

Three primary ways to represent a function:
1. **Formula:** Algebraic expression $y = f(x)$.
    
      
    
2. **Graph:** Visual plot of ordered pairs $(x, f(x))$ in the coordinate plane.
    
      
    
3. **Set of Ordered Pairs / Mapping:** The set $\{(x, y) \mid x \in X, y = f(x)\}$ where no first element $x$ is repeated.
    
      
    

```
  [ Input x ∈ Domain X ]  ───►  [ Rule f ]  ───►  [ Output y = f(x) ∈ Range Y ]
```

### Domain & Range Analysis

- **Domain ($X$):** The set of all valid input values.
    
      
    
- **Range ($Y$):** The set of all resulting output values.
    
      
    

> **Comparison Example: Linear vs. Quadratic vs. Exponential**
> 
>   
> 
> Consider the formulas $y_1 = 2x$, $y_2 = x^2$, and $y_3 = 2^x$:
> 
>   
> 
> - **$y = 2x$ (Linear):** Domain is $(-\infty, \infty)$; Range is $(-\infty, \infty)$.
>     
>       
>     
> - **$y = x^2$ (Square):** Domain is $(-\infty, \infty)$; Range is $[0, \infty)$ (squares cannot be negative).
>     
>       
>     
> - **$y = 2^x$ (Exponential):** Domain is $(-\infty, \infty)$; Range is $(0, \infty)$ (never reaches $0$ or becomes negative).
>     
>       
>     

### Key Functional Properties

- **Injectivity (One-to-One):** Distinct inputs produce distinct outputs.
    
      
    
    $$\forall x_1, x_2 \in X, \quad f(x_1) = f(x_2) \implies x_1 = x_2$$
    
    _Graphical Test:_ **Horizontal Line Test**—if any horizontal line intersects the graph more than once, the function is **not** injective.
    
      
    
- **Surjectivity (Onto):** Every element in the codomain $Y$ is mapped to by at least one element in domain $X$ (Range = Codomain).
    
      
    
    $$\forall y \in Y, \quad \exists x \in X \text{ such that } f(x) = y$$
    
- **Bijectivity:** A function that is both **injective** and **surjective**.
    
      
    

## 4. Function Composition & Invertibility

### Composition of Functions ($f \circ g$)

Given $g: X \to Y$ and $f: Y \to Z$, the composite function $(f \circ g)(x)$ is defined by:

  

$$(f \circ g)(x) = f(g(x))$$

_Order Matters:_ In general, $f(g(x)) \neq g(f(x))$.

  

> **Worked Example: Composition Breakdown**
> 
>   
> 
> Let $g(x) = x^3$ and $f(y) = y^4 + 1$.
> 
>   
> 
> - **$(f \circ g)(x) = f(g(x))$:** Substitute $g(x)$ into $f(y) \implies (x^3)^4 + 1 = x^{12} + 1$.
>     
>       
>     
> - **$(g \circ f)(x) = g(f(x))$:** Substitute $f(x)$ into $g(x) \implies (x^4 + 1)^3$.
>     
>       
>     

### Inverse Functions ($f^{-1}$)

A function $f: X \to Y$ has an inverse $f^{-1}: Y \to X$ **if and only if** $f$ is bijective (or restricted to a monotonic interval).

  

- **Core Relations:** $y = f(x) \iff x = f^{-1}(y)$.
    
      
    
- **Identity Cancellations:** $f^{-1}(f(x)) = x$ for all $x \in X$, and $f(f^{-1}(y)) = y$ for all $y \in Y$.
    
      
    
- **Domain-Range Flip:** $\text{Domain}(f^{-1}) = \text{Range}(f)$ and $\text{Range}(f^{-1}) = \text{Domain}(f)$.
    
      
    
- **Geometric Symmetry:** The graph of $y = f^{-1}(x)$ is the reflection of $y = f(x)$ across the line $y = x$.
    
      
    

> **Worked Example: Finding an Inverse**
> 
>   
> 
> Find $f^{-1}(y)$ for $y = f(x) = 3x - 6$:
> 
>   
> 
> 1. Solve the equation for $x$:
>     
>       
>     
>     $$y = 3x - 6 \implies y + 6 = 3x \implies x = \frac{1}{3}(y + 6)$$
>     
> 2. Express the inverse function:
>     
>       
>     
>     $$f^{-1}(y) = \frac{1}{3}y + 2 \quad \left(\text{or swapping variables: } f^{-1}(x) = \frac{1}{3}x + 2\right)$$
>     

> **Inverting a Chain Rule (Inverse of Composite Functions):**
> 
>   
> 
> The inverse of a composite function $(h \circ g)(x)$ reverses the order of operations:
> 
>   
> 
> $$(h \circ g)^{-1} = g^{-1} \circ h^{-1}$$

## 5. Primary Function Families in Calculus

|**Function Type**|**Formula y=f(x)y = f(x)y=f(x)**|**Domain**|**Range**|**Key Graphical / Calculus Properties**|
|---|---|---|---|---|
|**Power**|$y = x^n$($n \in \mathbb{N}$)|$(-\infty, \infty)$|$[0, \infty)$(even $n$)<br><br>  <br>  <br><br>$(-\infty, \infty)$ (odd $n$)|Symmetric about $y$-axis (even) or origin (odd). $\frac{d}{dx}[x^n] = n x^{n-1}$.|
|**Exponential**|$y = b^x$($b > 0, b \neq 1$)|$(-\infty, \infty)$|$(0, \infty)$|Monotonic growth ($b>1$) or decay ($0<b<1$). For $y=e^x$, rate of change equals value.|
|**Logarithmic**|$y = \log_b(x)$|$(0, \infty)$|$(-\infty, \infty)$|Vertical asymptote at $x=0$. Inverse of exponential ($y = \ln x \iff x = e^y$).|
|**Sine**|$y = \sin x$|$(-\infty, \infty)$|$[-1, 1]$|Periodic ($2\pi$), odd function: $\sin(-x) = -\sin x$.|
|**Cosine**|$y = \cos x$|$(-\infty, \infty)$|$[-1, 1]$|Periodic ($2\pi$), even function: $\cos(-x) = \cos x$.|
|**Restricted Inverse Sine**|$y = \sin^{-1} x$|$[-1, 1]$|$\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$|Restricted domain to enforce injectivity. Slope $\frac{dy}{dx} = \frac{1}{\sqrt{1-x^2}}$.|

## 🔗 Related Notes & Links

- **Prerequisites:** `[[General-Math-Terms]]`, `[[03 Set Symbols]]`
    
      
    
- **Next Topic:** `[[The-Real-Numbers]]` (Rationality, irrationality of $\sqrt{2}$, and ordered fields)
    
      
    
- **Folder Location:** `Math/Calculus/00-Foundations/Sets-and-Functions`
    
      
    

Would you like to continue to the next note, **`[[The-Real-Numbers]]`**, or refine any part of this foundation note?