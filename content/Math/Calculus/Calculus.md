---
tags:
  - subject
  - math
  - calculus
---
## Overview

### [[01 Limits]]

- **Limits & Approach**: A limit \(\lim_{x \to a} f(x) = L\) describes the value \(f(x)\) approaches as \(x\) gets arbitrarily close to \(a\). Evaluated rigorously using \(\epsilon\)-\(\delta\) (epsilon-delta) criteria \(|f(x) - L| < \epsilon\) for \(0 < |x - a| < \delta\).
- **Continuity**: \(f(x)\) is continuous at \(x = a\) if \(\lim_{x \to a} f(x) = f(a)\). Continuous functions on closed intervals \([a,b]\) satisfy the **Extreme Value Theorem** (reaches maximum \(M\) and minimum \(m\)) and the **Intermediate Value Theorem** (takes all intermediate values between \(m\) and \(M\)).
- **Key Limit Rules**: Standard trigonometric limits include \(\lim_{x \to 0} \frac{\sin x}{x} = 1\) and \(\lim_{x \to 0} \frac{1 - \cos x}{x} = 0\).

### [[02 Derivatives and Differentiation Rules]]

- **Definition of Derivative**: Represents the instantaneous rate of change and slope of the tangent line: \[f'(x) = \lim_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x}\]
- **Core Rules**:
    - **Power Rule**: \(\frac{d}{dx}(x^n) = n x^{n-1}\)
    - **Linearity / Sum Rule**: \(\frac{d}{dx}(a u + b v) = a \frac{du}{dx} + b \frac{dv}{dx}\)
    - **Product Rule**: \(\frac{d}{dx}(u v) = u \frac{dv}{dx} + v \frac{du}{dx}\)
    - **Quotient Rule**: \(\frac{d}{dx}\left(\frac{u}{v}\right) = \frac{v \frac{du}{dx} - u \frac{dv}{dx}}{v^2}\)
    - **Chain Rule**: \(\frac{dz}{dx} = \frac{dz}{dy} \frac{dy}{dx}\) for composite functions \(z = f(g(x))\)
- **Trigonometric & Exponential Derivatives**: \(\frac{d}{dx}(\sin x) = \cos x\), \(\frac{d}{dx}(\cos x) = -\sin x\), \(\frac{d}{dx}(\tan x) = \sec^2 x\), \(\frac{d}{dx}(e^x) = e^x\), and \(\frac{d}{dx}(\ln x) = \frac{1}{x}\).

### [[03 Applications of the Derivative]]

- **Optimization & Curve Sketching**: Critical points occur where \(f'(x) = 0\) or \(f'(x)\) is undefined. The second derivative \(f''(x)\) indicates concavity (bending up if \(f''(x) > 0\), down if \(f''(x) < 0\)); \(f''(x) = 0\) indicates potential inflection points.
- **Mean Value Theorem (MVT)**: If \(f(x)\) is continuous on \([a,b]\) and differentiable on \((a,b)\), then at some point \(c \in (a,b)\): \[\frac{f(b) - f(a)}{b - a} = f'(c) \quad \text{(instantaneous speed = average speed)}\]
- **l'Hôpital's Rule**: Resolves indeterminate limit forms \(\frac{0}{0}\) or \(\frac{\infty}{\infty}\) via \(\lim_{x \to a} \frac{f(x)}{g(x)} = \lim_{x \to a} \frac{f'(x)}{g'(x)}\).
- **Newton's Method**: Iteratively approximates roots of \(f(x) = 0\) via \(x_{n+1} = x_n - \frac{f(x_n)}{f'(x_n)}\).

### [[04 Integrals and the Fundamental Theorem]]

- **Definite Integral & Riemann Sums**: The integral \(\int_a^b v(x) dx\) represents net area, defined as the limit of rectangular sums \(\sum v(x_k^*) \Delta x\) as mesh width \(\Delta x \to 0\).
- **Fundamental Theorem of Calculus (FTC)**:
    - **Part 1 (Derivative of Integral)**: If \(f(x) = \int_a^x v(t) dt\), then \(\frac{df}{dx} = v(x)\).
    - **Part 2 (Integral of Derivative)**: If \(v(x) = \frac{df}{dx}\), then \(\int_a^b v(x) dx = f(b) - f(a)\).

### [[05 Transcendental Functions and Differential Equations]]

- **Exponentials & Logarithms**: Natural logarithm defined as area \(\ln x = \int_1^x \frac{1}{t} dt\). The exponential \(e^x\) is its inverse, satisfying \(e = \lim_{n \to \infty}\left(1 + \frac{1}{n}\right)^n \approx 2.71828\).
- **Differential Equations**:
    - **Growth & Decay**: \(\frac{dy}{dt} = cy \implies y(t) = y_0 e^{ct}\).
    - **First-Order Linear**: \(\frac{dy}{dt} - cy = s \implies y(t) = e^{ct} y_0 + \frac{s}{c}(e^{ct} - 1)\).
    - **Separable Equations**: Solved by separating variables \(\int \frac{dy}{g(y)} = \int f(x) dx\).

### [[06 Techniques and Applications of Integration]]

- **Techniques of Integration**:
    - **Substitution**: Reverses the Chain Rule using \(u = g(x)\), \(du = g'(x)dx\).
    - **Integration by Parts**: Reverses the Product Rule via \(\int u dv = u v - \int v du\).
    - **Trigonometric Substitutions**: Uses \(x = a \sin\theta\), \(x = a \tan\theta\), or \(x = a \sec\theta\) for radical integrands \(\sqrt{a^2-x^2}\), \(\sqrt{a^2+x^2}\), or \(\sqrt{x^2-a^2}\).
    - **Partial Fractions**: Decomposes rational functions \(P(x)/Q(x)\) into simple fractions.
- **Geometric Applications**: Computes areas between curves, volumes by slices/shells, arc length \(L = \int \sqrt{1 + (dy/dx)^2} dx\), surface area of revolution, probability distributions, and physical work/mass moments.

### [[07 Infinite Series and Taylor Series]]

- **Geometric Series**: \(\sum_{n=0}^{\infty} x^n = 1 + x + x^2 + \dots = \frac{1}{1-x}\) for \(|x| < 1\).
- **Convergence Tests**: Tests for positive and alternating series include the Integral Test, Comparison Test, Ratio Test, and Root Test.
- **Taylor & Maclaurin Series**: Matches all derivatives at basepoint \(x = a\): \[f(x) = \sum_{n=0}^{\infty} \frac{f^{(n)}(a)}{n!} (x - a)^n\]
    - **Key Expansions**:
        - \(e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \dots\)
        - \(\sin x = x - \frac{x^3}{3!} + \frac{x^5}{5!} - \dots\)
        - \(\cos x = 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \dots\)
- **Euler's Formula**: \(e^{i\theta} = \cos\theta + i\sin\theta\), yielding \(e^{i\pi} + 1 = 0\).

### [[08 Multivariable and Vector Calculus]]

- **Partial Derivatives & Gradients**: For \(z = f(x,y)\), partials \(\frac{\partial f}{\partial x}\) and \(\frac{\partial f}{\partial y}\) measure rates of change fixing the other variable. The gradient vector \(\nabla f = \left(\frac{\partial f}{\partial x}, \frac{\partial f}{\partial y}\right)\) points in the direction of steepest increase.
- **Multiple Integrals**: Double integrals \(\iint_R f(x,y) dA\) and triple integrals \(\iiint_V f(x,y,z) dV\) calculate volumes, masses, and average values over 2D and 3D regions (including polar, cylindrical, and spherical coordinates).
- **Vector Calculus Theorems**:
    - **Line Integrals**: Computes work \(\int_C \mathbf{F} \cdot d\mathbf{r}\) along a curve \(C\).
    - **Green's Theorem**: Connects double integral over region \(R\) to line integral along boundary \(C\): \(\oint_C M dx + N dy = \iint_R \left(\frac{\partial N}{\partial x} - \frac{\partial M}{\partial y}\right) dA\).
    - **Divergence & Stokes' Theorems**: Extend Green's theorem to 3D surface and flux integrals.
