---
tags:
  - concept
  - math
  - calculus
---
## Intuitive Explanation

Informally, the **limit** of a [[Function]] describes the behavior of that function as its input gets closer and closer to a specific value, rather than what happens _at_ that exact value.

  

When we write:

  

$$\lim_{x \to c} f(x) = L$$

We mean: **"As $x$ gets infinitely close to $c$ (from either side), the value of $f(x)$ gets arbitrarily close to $L$."**

  

### Key Takeaway

- The function **does not need to be defined at $x = c$** for a limit to exist.
    
      
    
- We only care about what happens _near_ $c$, not _at_ $c$.
    
      
    

## 2. Formal Definition ($\varepsilon$-$\delta$ Definition)

While the intuitive idea works for basic functions, rigorous calculus requires the precise **$\varepsilon$-$\delta$ (epsilon-delta) definition**, formulated by Karl Weierstrass.

  

> **Definition:**
> 
> Let $f$ be a function defined on an open interval containing $c$ (except possibly at $c$). We say that
> 
>   
> 
> $$\lim_{x \to c} f(x) = L$$
> 
> if for every number $\varepsilon > 0$, there exists a corresponding number $\delta > 0$ such that for all $x$:
> 
>   
> 
> $$0 < \vert{}x - c\vert{} < \delta \implies \vert{}f(x) - L\vert{} < \varepsilon$$

### Decoding the Definition

- **$\varepsilon$ (Epsilon):** Represents the _target tolerance_ or allowable error for the output $f(x)$. We want $f(x)$ to be within $\varepsilon$ of $L$ (i.e., $L - \varepsilon < f(x) < L + \varepsilon$).
    
      
    
- **$\delta$ (Delta):** Represents the _input restriction_ required to achieve that target. It tells us how close $x$must be to $c$ (i.e., $c - \delta < x < c + \delta$).
    
      
    
- **$0 < \vert{}x - c\vert{} < \delta$:** The $0 <$ part ensures that $x \neq c$. We are looking at points _around_$c$, not necessarily at $c$ itself.
    
      
    

## 3. Basic Limit Laws

If $\lim_{x \to c} f(x) = L$ and $\lim_{x \to c} g(x) = M$, then:

  

- **Sum Rule:** $\lim_{x \to c} [f(x) + g(x)] = L + M$
    
      
    
- **Product Rule:** $\lim_{x \to c} [f(x) \cdot g(x)] = L \cdot M$
    
      
    
- **Quotient Rule:** $\lim_{x \to c} \left[\frac{f(x)}{g(x)}\right] = \frac{L}{M}$, provided $M \neq 0$

