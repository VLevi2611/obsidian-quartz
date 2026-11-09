---
tags:
  - summary
  - math
  - calculus
---
### 01 Sequences and Their Limits

**Module:** 01 Sequences and Their Limits

  

**Previous Topic:** [[Bounds and Completeness]]

  

**Up Next:** [[Limits of Functions]]

  

**Parent Hub:** [[Calculus]]

  

#### 1. Formal Definition of a Sequence & Convergence

A real sequence is an ordered list of real numbers indexed by the natural numbers. Formally, a sequence $(a_n)_{n=1}^\infty$ is a function $a: \mathbb{N} \to \mathbb{R}$, where $a(n) = a_n$.

  

##### Formal Limit Definition ($\epsilon-N$ Definition)

A sequence $(a_n)$ converges to a real limit $L \in \mathbb{R}$ (written $\lim_{n \to \infty} a_n = L$ or $a_n \to L$) if:

  

$$\forall \epsilon > 0, \; \exists N \in \mathbb{N} \text{ such that } \forall n > N, \; \vert{}a_n - L\vert{} < \epsilon$$

- **Geometric Interpretation:** For any given margin of error $\epsilon > 0$, there exists a cutoff index $N$beyond which all terms $a_n$ are trapped within the open interval $(L - \epsilon, L + \epsilon)$.
    
      
    
- **Divergence:** A sequence is divergent if it fails to approach any finite limit $L$.
    
      
    
- **Divergence to Infinity ($\pm\infty$):**
    
      
    
    $$\lim_{n \to \infty} a_n = \infty \iff \forall M > 0, \; \exists N \in \mathbb{N} \text{ such that } \forall n > N, \; a_n > M$$
    
    $$\lim_{n \to \infty} a_n = -\infty \iff \forall M > 0, \; \exists N \in \mathbb{N} \text{ such that } \forall n > N, \; a_n < -M$$
    

> **Worked Example: $\epsilon-N$ Proof of Convergence**
> 
>   
> 
> Prove using the $\epsilon-N$ definition that $\lim_{n \to \infty} \frac{2n + 1}{n + 3} = 2$.
> 
>   
> 
> _Proof:_ Let $\epsilon > 0$ be given. We analyze the distance $\vert{}a_n - L\vert{}$:
> 
>   
> 
> $$\vert{}a_n - 2\vert{} = \left\vert{} \frac{2n + 1}{n + 3} - 2 \right\vert{} = \left\vert{} \frac{2n + 1 - (2n + 6)}{n + 3} \right\vert{} = \left\vert{} \frac{-5}{n + 3} \right\vert{} = \frac{5}{n + 3}$$
> 
> We require $\frac{5}{n + 3} < \epsilon \iff n + 3 > \frac{5}{\epsilon} \iff n > \frac{5}{\epsilon} - 3$.
> 
>   
> 
> By the Archimedean Property, choose $N = \left\lceil \frac{5}{\epsilon} - 3 \right\rceil$ (or $N = \lfloor \frac{5}{\epsilon} \rfloor$).
> 
>   
> 
> For all $n > N$, we have $n > \frac{5}{\epsilon} - 3 \implies \frac{5}{n+3} < \epsilon \implies \left\vert{}\frac{2n+1}{n+3} - 2\right\vert{} < \epsilon$.
> 
>   
> 
> $\therefore \lim_{n \to \infty} \frac{2n+1}{n+3} = 2$.
> 
>   

> [!tip] Finding the threshold $N$: Always work backward from $\vert{}a_n - L\vert{} < \epsilon$ to isolate $n$, then use the Archimedean Property to choose $N(\epsilon) \in \mathbb{N}$.
> 
>   

#### 2. Limit Arithmetic & Basic Properties

##### Core Structural Properties

1. **Uniqueness of Limits:** If a sequence converges, its limit is unique.
    
      
    
    > **Proof of Uniqueness:** Assume $a_n \to L_1$ and $a_n \to L_2$ with $L_1 \neq L_2$. Choose $\epsilon = \frac{\vert{}L_1 - L_2\vert{}}{2} > 0$.
    > 
    >   
    > 
    > By convergence, $\exists N_1$ s.t. $\forall n > N_1, \vert{}a_n - L_1\vert{} < \epsilon$, and $\exists N_2$s.t. $\forall n > N_2, \vert{}a_n - L_2\vert{} < \epsilon$.
    > 
    >   
    > 
    > For $n > \max(N_1, N_2)$, the triangle inequality gives:
    > 
    >   
    > 
    > $$\vert{}L_1 - L_2\vert{} = \vert{}(L_1 - a_n) + (a_n - L_2)\vert{} \le \vert{}a_n - L_1\vert{} + \vert{}a_n - L_2\vert{} < \epsilon + \epsilon = \vert{}L_1 - L_2\vert{}$$
    > 
    > This yields $\vert{}L_1 - L_2\vert{} < \vert{}L_1 - L_2\vert{}$, a contradiction. Thus $L_1 = L_2$.
    > 
    >   
    
2. **Boundedness of Convergent Sequences:** Every convergent sequence is bounded.
    
      
    
    > [!tip] The converse is false: bounded sequences are not necessarily convergent (e.g., $a_n = (-1)^n$ is bounded by $1$ but diverges due to oscillation).
    > 
    >   
    

##### Algebraic Limit Laws

If $\lim_{n \to \infty} a_n = L$ and $\lim_{n \to \infty} b_n = M$:

  

- **Sum / Difference:** $\lim_{n \to \infty} (a_n \pm b_n) = L \pm M$
    
      
    
- **Scalar Multiple:** $\lim_{n \to \infty} (c \cdot a_n) = c \cdot L$ for any constant $c \in \mathbb{R}$
    
      
    
- **Product Rule:** $\lim_{n \to \infty} (a_n \cdot b_n) = L \cdot M$
    
      
    
- **Quotient Rule:** $\lim_{n \to \infty} \left(\frac{a_n}{b_n}\right) = \frac{L}{M}$, provided $M \neq 0$ and $b_n \neq 0$ for all $n$
    
      
    

##### Order Preservation

If $a_n \le b_n$ for all $n \ge N_0$ and both limits exist, then $\lim_{n \to \infty} a_n \le \lim_{n \to \infty} b_n$.

  

#### 3. Core Limit Theorems

##### 1. The Sandwich (Squeeze) Theorem

If $a_n \le b_n \le c_n$ for all $n \ge N_0$, and $\lim_{n \to \infty} a_n = \lim_{n \to \infty} c_n = L$, then $\lim_{n \to \infty} b_n = L$.

  

> **Worked Example: Squeeze Theorem**
> 
>   
> 
> Evaluate $\lim_{n \to \infty} \frac{\sin(n)}{n^2 + 1}$.
> 
>   
> 
> Since $-1 \le \sin(n) \le 1$ for all $n \in \mathbb{N}$, we construct the lower and upper bounds:
> 
>   
> 
> $$-\frac{1}{n^2 + 1} \le \frac{\sin(n)}{n^2 + 1} \le \frac{1}{n^2 + 1}$$
> 
> Since $\lim_{n \to \infty} \left(-\frac{1}{n^2 + 1}\right) = 0$ and $\lim_{n \to \infty} \frac{1}{n^2 + 1} = 0$, by the Squeeze Theorem:
> 
>   
> 
> $$\lim_{n \to \infty} \frac{\sin(n)}{n^2 + 1} = 0$$

##### 2. Null Sequence $\times$ Bounded Sequence Theorem

If $\lim_{n \to \infty} a_n = 0$ (a null sequence) and $(b_n)$ is bounded (i.e., $\vert{}b_n\vert{} \le M$ for all $n$), then $\lim_{n \to \infty} (a_n \cdot b_n) = 0$.

  

##### 3. D'Alembert Ratio Test for Sequences

Let $(a_n)$ be a sequence of positive terms ($a_n > 0$) such that $\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = L$:

  

- If $L < 1$, then $\lim_{n \to \infty} a_n = 0$.
    
      
    
- If $L > 1$, then $\lim_{n \to \infty} a_n = \infty$.
    
      
    
- If $L = 1$, the test is inconclusive.
    
      
    

##### 4. Ratio-to-Root Theorem

If $a_n > 0$ for all $n$ and $\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = L$, then $\lim_{n \to \infty} \sqrt[n]{a_n} = L$.

  

> [!tip] The Ratio-to-Root Theorem provides a convenient shortcut for evaluating difficult $n$-th root limits like $\lim \sqrt[n]{n!/n^n}$ by calculating the ratio limit instead.
> 
>   

#### 4. Monotonic Sequences & Key Standard Limits

##### Monotone Convergence Theorem (MCT)

Every monotonic sequence of real numbers that is bounded converges to a finite limit.

  

- **Non-decreasing:** If $a_{n+1} \ge a_n$ for all $n$ and $a_n \le M$, then $\lim_{n \to \infty} a_n = \sup\{a_n \mid n \in \mathbb{N}\}$.
    
      
    
- **Non-increasing:** If $a_{n+1} \le a_n$ for all $n$ and $a_n \ge m$, then $\lim_{n \to \infty} a_n = \inf\{a_n \mid n \in \mathbb{N}\}$.
    
      
    

##### Construction of Euler's Constant ($e$)

Consider the sequence $a_n = \left(1 + \frac{1}{n}\right)^n$.

  

1. **Monotonicity:** By Bernoulli's inequality or AM-GM, $(a_n)$ is strictly increasing: $a_{n+1} > a_n$.
    
      
    
2. **Boundedness:** By expanding via the Binomial Theorem:
    
      
    
    $$\left(1 + \frac{1}{n}\right)^n = \sum_{k=0}^n \binom{n}{k} \frac{1}{n^k} = 1 + 1 + \sum_{k=2}^n \frac{1}{k!} \left(1 - \frac{1}{n}\right)\dots\left(1 - \frac{k-1}{n}\right) < 1 + 1 + \sum_{k=2}^n \frac{1}{2^{k-1}} < 3$$
    
3. By MCT, the limit exists and defines Euler's constant:
    
      
    
    $$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n \approx 2.71828\dots$$
    

##### Benchmark Limit Hierarchy

|**Sequence Limit**|**Formula**|**Condition / Value**|
|---|---|---|
|**Geometric Sequence**|$\lim_{n \to \infty} q^n$|$\begin{cases} 0 & \text{if } \Vert{}q\Vert{} < 1 \\ 1 & \text{if } q = 1 \\ \infty & \text{if } q > 1 \\ \text{DNE} & \text{if } q \le -1 \end{cases}$|
|**Constant Root**|$\lim_{n \to \infty} \sqrt[n]{c}$|$1 \quad (\forall c > 0)$|
|**Root of $n$**|$\lim_{n \to \infty} \sqrt[n]{n}$|$1$|
|**Polynomial vs. Exponential**|$\lim_{n \to \infty} \frac{n^k}{a^n}$|$0 \quad (\forall k > 0, a > 1)$|
|**Exponential vs. Factorial**|$\lim_{n \to \infty} \frac{a^n}{n!}$|$0 \quad (\forall a \in \mathbb{R})$|
|**Factorial vs. Power Scale**|$\lim_{n \to \infty} \frac{n!}{n^n}$|$0$|

> [!tip] Asymptotic Growth Scale (from slowest to fastest growth as $n \to \infty$):
> 
>   
> 
> $$\ln(n) \ll n^k \ll a^n \ll n! \ll n^n \quad (\text{for } k > 0, a > 1)$$

#### 5. Subsequences & Structural Theorems

##### Subsequence Definition & Inheritance

Given a sequence $(a_n)$, a subsequence $(a_{n_k})_{k=1}^\infty$ is formed by choosing an infinite subset of indices using a strictly increasing index sequence $n_1 < n_2 < n_3 < \dots$

  

- **Subsequence Inheritance Property:** If $(a_n)$ converges to $L$, then **every** subsequence $(a_{n_k})$also converges to $L$.
    
      
    
- **Divergence Criterion:** If a sequence $(a_n)$ contains two subsequences that converge to different limits,$(a_n)$ diverges.
    
      
    

##### Bolzano-Weierstrass Theorem

Every bounded sequence of real numbers contains at least one convergent subsequence.

  

> **Proof Sketch:** Let $(a_n)$ be bounded in $[a, b]$. Divide $[a, b]$ into two equal subintervals. At least one subinterval contains infinitely many terms of $(a_n)$. Select this subinterval $[a_1, b_1]$ and choose $a_{n_1} \in [a_1, b_1]$. Bisection repeatedly constructs nested intervals $[a_k, b_k]$ of length $\frac{b-a}{2^k} \to 0$. By Cantor's Lemma, the endpoints converge to a single real point $c$, forcing $a_{n_k} \to c$.
> 
>   

##### Cantor's Nested Interval Lemma

Let $([a_n, b_n])_{n=1}^\infty$ be a sequence of closed, bounded intervals such that:

  

1. $[a_{n+1}, b_{n+1}] \subseteq [a_n, b_n]$ for all $n \in \mathbb{N}$ (nested).
    
      
    
2. $\lim_{n \to \infty} (b_n - a_n) = 0$ (interval lengths shrink to zero).
    
      
    

Then there exists **exactly one** real number $c \in \mathbb{R}$ contained in every interval:

  

$$\bigcap_{n=1}^\infty [a_n, b_n] = \{c\}$$

#### 6. Cauchy Criterion, Limit Superior ($\limsup$) & Limit Inferior ($\liminf$)

##### Cauchy Sequences

A sequence $(a_n)$ is a **Cauchy sequence** if terms become arbitrarily close to each other as indices grow:

  

$$\forall \epsilon > 0, \; \exists N \in \mathbb{N} \text{ such that } \forall n, m > N, \; \vert{}a_n - a_m\vert{} < \epsilon$$

##### Cauchy Convergence Criterion

In the real number system $\mathbb{R}$, a sequence converges if and only if it is a Cauchy sequence.

  

$$\text{Convergence in } \mathbb{R} \iff \text{Cauchy Criterion}$$

> [!tip] The Cauchy Criterion allows proving that a sequence converges **without knowing the limit value $L$ in advance**. This completeness property holds in $\mathbb{R}$ but fails in $\mathbb{Q}$.
> 
>   

##### Partial Limits (Limit Points)

A value $L \in \mathbb{R} \cup \{-\infty, \infty\}$ is a **partial limit** (or limit point) of $(a_n)$ if there exists a subsequence $(a_{n_k})$ such that $\lim_{k \to \infty} a_{n_k} = L$. Let $S$ denote the set of all partial limits of $(a_n)$.

  

##### Limit Superior ($\limsup$) and Limit Inferior ($\liminf$)

- **Limit Superior ($\limsup$):** The supremum of the set of partial limits $S$:
    
      
    
    $$\limsup_{n \to \infty} a_n = \overline{\lim}_{n \to \infty} a_n = \sup S = \lim_{n \to \infty} \left( \sup_{k \ge n} a_k \right)$$
    
- **Limit Inferior ($\liminf$):** The infimum of the set of partial limits $S$:
    
      
    
    $$\liminf_{n \to \infty} a_n = \underline{\lim}_{n \to \infty} a_n = \inf S = \lim_{n \to \infty} \left( \inf_{k \ge n} a_k \right)$$
    

##### Master Convergence Test via $\limsup / \liminf$

A real sequence $(a_n)$ converges to $L \in \mathbb{R}$ if and only if:

  

$$\limsup_{n \to \infty} a_n = \liminf_{n \to \infty} a_n = L$$

> **Worked Example: Finding $\limsup$ and $\liminf$**
> 
>   
> 
> Consider $a_n = (-1)^n + \frac{1}{n}$.
> 
>   
> 
> - Even indices ($n = 2k$): $a_{2k} = 1 + \frac{1}{2k} \to 1$.
>     
>       
>     
> - Odd indices ($n = 2k-1$): $a_{2k-1} = -1 + \frac{1}{2k-1} \to -1$.
>     
>       
>     
> 
> Set of partial limits: $S = \{-1, 1\}$.
> 
>   
> 
> Thus, $\limsup_{n \to \infty} a_n = 1$ and $\liminf_{n \to \infty} a_n = -1$. Since $\limsup \neq \liminf$, the sequence diverges.