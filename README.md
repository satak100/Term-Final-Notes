# Lecture - 1
## **1. What “expectation” means**

In probability and statistics, the **expectation** (also called the *expected value* or *mean*) is basically the **long-run average** you’d get if you could repeat an experiment infinitely many times.

---

### **Example: Rolling a fair die**

* Possible outcomes: $1, 2, 3, 4, 5, 6$
* Each outcome has probability $1/6$
* Expectation =

$$
E[X] = \frac{1+2+3+4+5+6}{6} = 3.5
$$

You’ll **never** roll a 3.5, but if you rolled the die enough times and took the average, it would hover around 3.5.

---

## **2. The mathematical definition**

If $X$ is a **discrete** random variable with possible values $x_i$ and probabilities $p_i$:

$$
E[X] = \sum_i x_i \cdot p_i
$$

If $X$ is **continuous** with probability density function $f(x)$:

$$
E[X] = \int_{-\infty}^{\infty} x \cdot f(x) \, dx
$$

---

## **5. A note on “expectation != prediction”**

The expectation tells you the *average* — not necessarily the most likely outcome.
Example:

* If you have a 90% chance of \$10 and 10% chance of \$1000,
  Expectation = $0.9 \times 10 + 0.1 \times 1000 = 109$.
  You’ll rarely get exactly \$109, but that’s the long-run average.

---
