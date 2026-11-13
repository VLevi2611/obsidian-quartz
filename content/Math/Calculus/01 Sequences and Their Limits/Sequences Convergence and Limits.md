---
tags:
  - concept
  - math
  - calculus
---
**Previous Topic:** The Real Numbers
**Up Next:** Limit of a Function [[CAL1_002 גבול של פונקציה]]

  

1. Sequences & Formal Convergence Definition The concept of a sequence transitions mathematical analysis from continuous intervals into a discrete domain, laying the foundation for series and functions. A sequence $(a_n)$ is fundamentally a function whose domain is the natural numbers $\mathbb{N}$ and whose codomain is the real numbers $\mathbb{R}$.
    
      
    

Formal Definition of a Limit Formally, a sequence $(a_n)$ converges to a real number $L$ if, for every arbitrarily small positive tolerance $\epsilon > 0$, there exists a natural number index $N \in \mathbb{N}$ such that for all terms where $n > N$:$\lim_{n \to \infty} a_n = L \iff \forall \epsilon > 0, \exists N \in \mathbb{N} \text{ s.t. } n > N \implies \vert{}a_n - L\vert{} < \epsilon$

  

- Tolerance ($\epsilon$): Represents a strict bound on the distance between the sequence terms and the limit $L$.
    
      
    
- Index Threshold ($N$): The point in the sequence after which all subsequent terms are permanently "trapped" within the $\epsilon$-neighborhood of $L$.
    
      
    

Example: Formal Proof of Convergence Let $a_n = \frac{1}{n}$. Prove $\lim_{n \to \infty} a_n = 0$.

  

Proof: Let $\epsilon > 0$ be given. We must find $N \in \mathbb{N}$ such that for all $n > N$:$\left\vert{} \frac{1}{n} - 0 \right\vert{} < \epsilon \implies \frac{1}{n} < \epsilon \implies n > \frac{1}{\epsilon}$ By the Archimedean property of the real numbers, we can always choose an integer $N = \lfloor \frac{1}{\epsilon} \rfloor + 1$. For any $n > N$, it directly follows that $n > \frac{1}{\epsilon}$, which implies $\frac{1}{n} < \epsilon$.$\therefore \lim_{n \to \infty} \frac{1}{n} = 0$

  

2. Properties of Convergent Sequences: Uniqueness and Boundedness Despite containing infinitely many terms, a convergent sequence exhibits strict algebraic bounds and approaches exactly one specific value.
    
      
    

Rigorous Proof (by Contradiction): Uniqueness of a Limit Proof: If a sequence $(a_n)$ converges, its limit is unique (i.e., if $a_n \to L_1$ and $a_n \to L_2$, then $L_1 = L_2$).

  

Assumption: Suppose $a_n$ converges to two distinct limits, $L_1$ and $L_2$, where $L_1 \neq L_2$. Let the tolerance be half the distance between them: $\epsilon = \frac{\vert{}L_1 - L_2\vert{}}{2} > 0$. Since $a_n \to L_1$, there exists $N_1$ such that for all $n > N_1$: $\vert{}a_n - L_1\vert{} < \epsilon \quad \text{--- (Inequality 1)}$ Since $a_n \to L_2$, there exists $N_2$ such that for all $n > N_2$: $\vert{}a_n - L_2\vert{} < \epsilon \quad \text{--- (Inequality 2)}$ Let $N = \max(N_1, N_2)$. For any index $n > N$, both Inequality 1 and Inequality 2 hold simultaneously. Applying the Triangle Inequality ($\vert{}a + b\vert{} \le \vert{}a\vert{} + \vert{}b\vert{}$) [[Absolute Value]]: $\vert{}L_1 - L_2\vert{} = \vert{}L_1 - a_n + a_n - L_2\vert{} \le \vert{}L_1 - a_n\vert{} + \vert{}a_n - L_2\vert{}$ Substitute the $\epsilon$ boundaries from Inequalities 1 and 2: $\vert{}L_1 - L_2\vert{} < \epsilon + \epsilon = 2\epsilon$ Recall our initial definition of $\epsilon = \frac{\vert{}L_1 - L_2\vert{}}{2}$ and substitute it back: $\vert{}L_1 - L_2\vert{} < 2 \left( \frac{\vert{}L_1 - L_2\vert{}}{2} \right) = \vert{}L_1 - L_2\vert{}$ Contradiction: Because a number cannot be strictly less than itself ($\vert{}L_1 - L_2\vert{} < \vert{}L_1 - L_2\vert{}$ is impossible), the assumption that $L_1 \neq L_2$ is false. $\therefore L_1 = L_2 \quad (\text{i.e., limits are unique})$

  

Boundedness Lemma

  

- Lemma: Every convergent sequence is bounded. (There exists $M > 0$ such that $\vert{}a_n\vert{} \le M$ for all $n$).
    
      
    - Note on Converse: The converse is false. A bounded sequence is not necessarily convergent. For example, $a_n = (-1)^n$ is bounded between $-1$ and $1$, but oscillates infinitely and diverges.
        
          
        

3. The Arithmetic of Limits Just as $\mathbb{R}$ acts as an ordered field, sequences exhibit closed algebraic operations under limits, allowing complex sequences to be broken into simpler constituent limits [[01-Limits]].
    
      
    

Limit Axioms Let $(a_n)$ and $(b_n)$ be convergent sequences where $\lim_{n \to \infty} a_n = L$ and $\lim_{n \to \infty} b_n = M$.

  

|**Operation**|**Limit Result**|**Condition**|
|---|---|---|
|Addition (+)|$\lim (a_n + b_n) = L + M$|$\forall a_n, b_n$|
|Subtraction (-)|$\lim (a_n - b_n) = L - M$|$\forall a_n, b_n$|
|Multiplication ($\cdot$)|$\lim (a_n \cdot b_n) = L \cdot M$|$\forall a_n, b_n$|
|Division ($\div$)|$\lim \left(\frac{a_n}{b_n}\right) = \frac{L}{M}$|$M \neq 0, \; b_n \neq 0$|
|Scalar Identity|$\lim (c \cdot a_n) = c \cdot L$|$c \in \mathbb{R}$|

4. Core Theorems of Convergence & Inequality Constraints When algebraic calculation is insufficient, the convergence of sequences can be proven by evaluating their order relations and bounds.
    
      
    

Squeeze (Sandwich) Theorem If a sequence is bounded between two other sequences that converge to the same limit, it must also converge to that limit. For any real sequences $a_n, b_n, c_n$: If $a_n \le b_n \le c_n$ for all $n \ge N_0$, and $\lim_{n \to \infty} a_n = \lim_{n \to \infty} c_n = L$, then:$\lim_{n \to \infty} b_n = L$

  

Monotone Convergence Theorem A sequence $(a_n)$ is monotonic if it is consistently non-decreasing ($a_{n+1} \ge a_n$) or non-increasing ($a_{n+1} \le a_n$). Theorem: Every bounded monotonic sequence converges to a limit.

  

- Supremum Rule: If $(a_n)$ is monotonically increasing and bounded above, it converges exactly to its supremum (least upper bound).
    
      
    
- Infimum Rule: If $(a_n)$ is monotonically decreasing and bounded below, it converges exactly to its infimum (greatest lower bound).