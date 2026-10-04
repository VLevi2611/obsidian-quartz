---
tags:
  - summary
  - math
  - calculus
---
## Overview 

### Function

A [[Function]] is a rule or correspondence that assigns each [[Element Of|Element]] in one [[Set]] to exactly one element in another set.

> **Definition:**
> 
> Let $A$ and $B$ be sets. A function $f: A \to B$ is a relation that assigns to every element $x \in A$ a unique element $f(x) \in B$.

## 2. Domain, Codomain, and Range

When working with functions, it is essential to distinguish between the input sets and output sets:

  

- **Domain ($A$):** The complete set of all possible input values ($x$) for which the function is defined.
    
      
    
- **Codomain ($B$):** The set of all _potential_ output values specified by the function's definition. The actual outputs are constrained to live inside this set.
    
      
    
- **Range (or Image):** The actual set of values produced by the function. It is a subset of the codomain:
    
      
    
    $$\text{Range} = \{ f(x) \mid x \in \text{Domain} \} \subseteq B$$
    

## 3. Limit of a Function

Informally, a limit describes how a function behaves as its input approaches a specific value, rather than what happens at that exact value.

  

> **Definition:**
> 
> We write:
> 
>   
> 
> $$\lim_{x \to c} f(x) = L$$
> 
> meaning that as $x$ gets infinitely close to $c$ (from either side), the value of $f(x)$ gets arbitrarily close to $L$.
> 
>   

### Key Takeaways

- **Independence from the Point:** The function **does not need to be defined at $x = c$** for the limit to exist. We only care about the behavior _near_ $c$.
    
      
    
- **Rigorous Foundation:** Defined formally using the $\varepsilon$-$\delta$ definition (see [[Limit]]).