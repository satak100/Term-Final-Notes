
## 📊 1. Poisson Distribution

### 🔹 Use Case:

Models the **number of events** in a fixed period of **time** or **space**, **when events occur randomly and independently at a constant rate**.

### 💡 Examples:

* Number of calls received at a call center per hour.
* Number of earthquakes in a year.
* Number of typos per page in a book.

### 🔣 Definition:

If events happen at an average rate ( \lambda ) per unit time, the **Poisson distribution** gives the probability of observing exactly ( k ) events in time ( t ):

[
P(N(t) = k) = \frac{(\lambda t)^k e^{-\lambda t}}{k!}, \quad k = 0, 1, 2, ...
]

* ( \lambda ): average rate (events per unit time)
* ( t ): time interval
* ( N(t) ): number of events in time ( t )

### 🧮 Mean and Variance:

[
\mathbb{E}[N(t)] = \lambda t, \quad \text{Var}(N(t)) = \lambda t
]

---

## ⏱ 2. Exponential Distribution

### 🔹 Use Case:

Models the **time between events** in a Poisson process.

### 💡 Examples:

* Time until the next phone call.
* Time between arrivals at a bus stop.
* Lifetime of a light bulb (in some cases).

### 🔣 Definition:

If events occur with rate ( \lambda ), then the **time until the next event** (denoted ( T )) follows the **exponential distribution**:

[
f_T(t) = \lambda e^{-\lambda t}, \quad t \geq 0
]

This is the **probability density function** (PDF).

### 📈 Cumulative Distribution Function (CDF):

[
F_T(t) = P(T \leq t) = 1 - e^{-\lambda t}
]

### 🧮 Mean and Variance:

[
\mathbb{E}[T] = \frac{1}{\lambda}, \quad \text{Var}(T) = \frac{1}{\lambda^2}
]

---

## 🔗 Connection Between Poisson and Exponential

Here's the key:

> The **Poisson distribution** tells you the **number of events** in time ( t ),
> while the **Exponential distribution** tells you the **waiting time between those events**.

### Specifically:

* If the number of arrivals follows a **Poisson distribution with rate ( \lambda )**,
* Then the **time between arrivals** is **exponentially distributed** with the **same rate ( \lambda )**.

This relationship is the basis of the **Poisson process**:

### ⛓️ Poisson Process:

A process where:

1. Events occur randomly and independently.
2. The number of events in time ( t ) follows a Poisson distribution.
3. The inter-arrival times (time between events) are exponentially distributed.

---

## 🔁 Memoryless Property (Exponential)

A powerful feature of the exponential distribution:

[
P(T > t + s \mid T > s) = P(T > t)
]

**Meaning**: If you’ve already waited ( s ) time units, the probability you have to wait another ( t ) is the same as if you had just started. **Past doesn’t matter** — the process “forgets” its history.

---

## ✅ Summary Table

| Feature        | Poisson                                     | Exponential                |
| -------------- | ------------------------------------------- | -------------------------- |
| Models         | Number of events in time ( t )              | Time between two events    |
| Variable       | ( N(t) ): counts                            | ( T ): waiting time        |
| PMF / PDF      | ( \frac{(\lambda t)^k e^{-\lambda t}}{k!} ) | ( \lambda e^{-\lambda t} ) |
| Mean           | ( \lambda t )                               | ( \frac{1}{\lambda} )      |
| Variance       | ( \lambda t )                               | ( \frac{1}{\lambda^2} )    |
| Key Connection | Number of arrivals                          | Time between arrivals      |

---

