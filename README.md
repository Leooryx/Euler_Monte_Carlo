# 📐 Estimating Euler's Constant γ

Euler's constant is defined as:

\[
\gamma = \lim_{n \to \infty} \left( \sum_{k=1}^n \frac{1}{k} - \log(n) \right) = \sum_{k=1}^\infty \left( \frac{1}{k} - \log\left(1 + \frac{1}{k}\right) \right)
\]

It can also be written as:

\[
\gamma = -\int_0^1 \log(-\log x)\,dx
\]

---

## 1. Importance Sampling

We derived an unbiased estimator of γ using importance sampling with a proposal distribution of the form \( X = \lceil c / U^\alpha \rceil \), where \( U \sim \mathcal{U}[0,1] \). The choice of \( c \) and \( \alpha \) ensures proper tail behavior to capture contributions from large \( k \).

---

## 2. Monte Carlo Estimation

Using the integral form, we estimated γ via:
- Standard Monte Carlo
- Stratified Monte Carlo
- Quasi-Monte Carlo (Sobol sequences)

We compared their convergence rates visually.

---

## 3. Control Variates

To reduce variance, we used control variates based on \( \log(1 - U) \), leveraging the approximation \( \log x \approx x - 1 \) near 1. We repeated the Monte Carlo estimations and showed the improvement.

---

## 4. Truncated Sum Estimator

We used a truncated estimator of the form:

\[
\sum_{k=0}^R \frac{a_k}{\mathbb{P}(R \geq k)}
\]

We showed it is unbiased, and chose two distributions for \( R \) to keep variance finite. This allowed estimation of γ from its series definition.

---


