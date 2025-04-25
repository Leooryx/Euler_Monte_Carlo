```markdown
# 📐 Estimating Euler's Constant γ

Euler's constant is defined as:

γ = limₙ→∞ ( ∑ₖ₌₁ⁿ 1/k − log(n) )  
  = ∑ₖ₌₁^∞ ( 1/k − log(1 + 1/k) )

It also admits an integral form:

γ = −∫₀¹ log(−log x) dx

---

## 1. Importance Sampling

We derived an unbiased estimator of γ using importance sampling with a proposal of the form X = ⌈c / U^α⌉, where U ~ Uniform[0,1]. The parameters c and α were chosen to ensure good coverage of the summation tail.

---

## 2. Monte Carlo Estimation

We estimated γ using its integral representation with three methods:
- Standard Monte Carlo
- Stratified Monte Carlo
- Quasi-Monte Carlo (Sobol sequences)

We compared the convergence rates of the estimators through visualizations.

---

## 3. Control Variates

To reduce variance, we introduced control variates based on log(1 − U), using the approximation log(x) ≈ x − 1 near 1. We re-estimated γ with these variates and showed the improvement in convergence.

---

## 4. Truncated Sum Estimator

We used a truncated sum estimator of the form:

  ∑ₖ₌₀^R aₖ / P(R ≥ k)

We proved its unbiasedness and selected a distribution for R that ensures low variance. This method allowed us to estimate γ from its original series definition.

---
```
