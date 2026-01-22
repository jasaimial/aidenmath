# Solution to Functional Equation: $f(x)f(y) = f(x+y) + xy$

## Problem Statement
Find all functions $f: \mathbb{R} \rightarrow \mathbb{R}$ such that function $f$ satisfies the equation:
\[ f(x)f(y) = f(x+y) + xy \]
for all real numbers $x, y$.

---

## Solution Phase 1: Determining Initial Values

**Thinking Guide:**
In functional equations, the properties of $0$ are often the most powerful starting point because $x+0=x$ and $x \cdot 0 = 0$. We want to find the value of $f(0)$ to simplify the equation.

### Step 1.1: Calculate $f(0)$
Let $x = y = 0$ in the original equation:
\[ f(0)f(0) = f(0+0) + 0\cdot0 \]
\[ f(0)^2 = f(0) \]
This implies $f(0) = 0$ or $f(0) = 1$.

### Step 1.2: Test $f(0) = 0$
Let $x = 0$ in the original equation. If $f(0) = 0$:
\[ f(0)f(y) = f(0+y) + 0\cdot y \]
\[ 0 \cdot f(y) = f(y) \]
\[ 0 = f(y) \]
So $f(y)$ must be the zero function ($f(y) = 0$ for all $y$).
We must verify if the zero function works in the original equation:
*   **LHS:** $f(x)f(y) = 0 \cdot 0 = 0$
*   **RHS:** $f(x+y) + xy = 0 + xy = xy$
Since $0 = xy$ is not true for all $x, y$ (e.g., $x=1, y=1$), $f(y) = 0$ is not a solution.

**Conclusion:** Therefore, **$f(0) = 1$**.

---

## Solution Phase 2: Analyzing Coefficients and Symmetry

**Thinking Guide:**
Now that we have a specifically known value ($f(0)=1$), we want to relate $f(x)$ to specific algebraic structures. Substituting values that create cancellations (like $y = -x$) is a standard technique to isolate terms.

### Step 2.1: Substitute $y = -x$
Substitute $y = -x$ into the original equation:
\[ f(x)f(-x) = f(x-x) + x(-x) \]
\[ f(x)f(-x) = f(0) - x^2 \]
Since $f(0)=1$:
\[ f(x)f(-x) = 1 - x^2 \]
\[ f(x)f(-x) = (1-x)(1+x) \]

**Crucial Insight:**
At this point, one might be tempted to guess that $f(x) = 1+x$ or $f(x) = 1-x$ simply by matching terms. While true, we haven't *proven* it yet. We only know their product behaves this way. We need to find the specific instances where the function "forces" the rest of the values.

---

## Solution Phase 3: The Fork in the Road (Roots)

**Thinking Guide:**
Look at the equation $f(x)f(-x) = 1 - x^2$. The right hand side becomes zero when $x=1$ or $x=-1$. This forces the function to be zero at specific points, which acts as a "pin" that we can use to fix the function's behavior everywhere else.

### Step 3.1: Analyze $x=1$
Substitute $x=1$ into our derived product equation:
\[ f(1)f(-1) = 1 - 1^2 = 0 \]
This implies that either **$f(1) = 0$** or **$f(-1) = 0$**. These are our two main cases.

---

## Solution Phase 4: Solving for the Function

**Thinking Guide:**
If we know $f(c) = 0$ for some constant $c$, we can substitute $y=c$ into the *original* equation. This makes the term $f(x)f(y)$ zero, allowing us to equate $f(x+c)$ directly to a polynomial in $x$.

### Case A: Assume $f(1) = 0$
Substitute $y=1$ into the original equation:
\[ f(x)f(1) = f(x+1) + x(1) \]
\[ f(x) \cdot 0 = f(x+1) + x \]
\[ 0 = f(x+1) + x \]
\[ f(x+1) = -x \]

Now, let $t = x+1$, which implies $x = t-1$:
\[ f(t) = -(t-1) \]
\[ f(t) = 1 - t \]
So, one candidate solution is **$f(x) = 1 - x$**.

### Case B: Assume $f(-1) = 0$
Substitute $y=-1$ into the original equation:
\[ f(x)f(-1) = f(x-1) + x(-1) \]
\[ f(x) \cdot 0 = f(x-1) - x \]
\[ 0 = f(x-1) - x \]
\[ f(x-1) = x \]

Now, let $t = x-1$, which implies $x = t+1$:
\[ f(t) = t+1 \]
\[ f(t) = 1 + t \]
So, the second candidate solution is **$f(x) = 1 + x$**.

---

## Solution Phase 5: Verification

**Thinking Guide:**
We found necessary conditions, but we must check if they are sufficient.

### Verify $f(x) = 1 - x$
*   **LHS:** $f(x)f(y) = (1-x)(1-y) = 1 - x - y + xy$
*   **RHS:** $f(x+y) + xy = (1 - (x+y)) + xy = 1 - x - y + xy$
*   **Result:** LHS = RHS. Valid.

### Verify $f(x) = 1 + x$
*   **LHS:** $f(x)f(y) = (1+x)(1+y) = 1 + x + y + xy$
*   **RHS:** $f(x+y) + xy = (1 + (x+y)) + xy = 1 + x + y + xy$
*   **Result:** LHS = RHS. Valid.

## Final Answer
The functions satisfying the equation are:
\[ f(x) = 1+x \]
\[ f(x) = 1-x \]
