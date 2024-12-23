# Statistics exercises
This repository contains exercises in statistics completed during my second year of studies. The tasks cover fundamental and advanced topics in probability theory, random variables, and statistical analysis. Each folder represents a set of problems focused on specific theoretical concepts and their practical applications.
### cwl1: Discrete Random Variable Distributions

1. **Probability Mass Function (PMF):**
   - Constructed a discrete probability distribution table for random variable \(X\) (`r1p`), showing values and their probabilities.

2. **Cumulative Distribution Function (CDF):**
   - Created a cumulative distribution table for random variable \(X\) (`r1f`), representing intervals and cumulative probabilities.

3. **Visualization of PMF and CDF:**
   - Plotted the PMF and CDF of \(X\) using the `vizualize_discrete_distribution()` function.

4. **Statistical Parameters:**
   - Calculated key parameters of the \(X\) distribution:
     - Mean (\(r1\_mean\)),
     - Variance (\(r1\_var\)),
     - Standard Deviation (\(r1\_std\)).

5. **Binomial Distribution:**
   - Constructed the PMF (`r2p`) and CDF (`r2f`) for a binomial random variable \(Y\) and visualized both using plots.
   - Calculated mean (\(r2\_mean\)), variance (\(r2\_var\)), and standard deviation (\(r2\_std\)) for \(Y\).

6. **Poisson Distribution:**
   - Constructed the PMF (`r3p`) and CDF (`r3f`) for a Poisson random variable \(Z\) and visualized both using plots.
   - Calculated mean (\(r3\_mean\)), variance (\(r3\_var\)), and standard deviation (\(r3\_std\)) for \(Z\).

7. **Probability Calculations:**
   - Computed and visualized probabilities for specific events:
     - \( P(X > 5) \),
     - \( P(1 < Y <= 6) \),
     - \( P(Z <= 12 \,|\, Z > 21) \).

### cwl2: Continuous Random Variable Distributions

1. **Uniform Distribution (X):**
   - Constructed the **Probability Density Function (PDF)** and **Cumulative Distribution Function (CDF)** for \(X\) with values ranging from -2 to 2.
   - Visualized the PDF and CDF of \(X\) using plots.
   - Calculated statistical parameters for \(X\):
     - Mean (\(r1\_mean\)),
     - Variance (\(r1\_var\)),
     - Standard Deviation (\(r1\_std\)).

2. **Normal Distribution (Y):**
   - Generated the PDF and CDF for a normal random variable \(Y\) with given mean and standard deviation.
   - Visualized the normal distribution's PDF and CDF using plots.
   - Computed statistical parameters for \(Y\):
     - Mean (\(r2\_mean\)),
     - Variance (\(r2\_var\)),
     - Standard Deviation (\(r2\_std\)).

3. **Gamma Distribution (Z):**
   - Created the PDF and CDF for a gamma random variable \(Z\) based on specified shape and scale parameters.
   - Visualized the gamma distribution's PDF and CDF using plots.
   - Calculated statistical parameters for \(Z\):
     - Mean (\(r3\_mean\)),
     - Variance (\(r3\_var\)),
     - Standard Deviation (\(r3\_std\)).

4. **Probability Calculations and Visualizations:**
   - Calculated and visualized specific probabilities for events:
     - \( P(X > -0.5) \),
     - \( P(1 < Y < 8) \),
     - \( P(Z < 2 \,|\, Z > 12) \).

This set focuses on the analysis, visualization, and calculation of statistical properties for continuous random variables.

### cwl3: Multivariate Random Variable Distributions

1. **Marginal Distributions:**
   - Computed marginal probability distributions:
     - \(P(X=x)\) stored in `r1bx`.
     - \(P(Y=y)\) stored in `r1by`.

2. **Conditional Distributions:**
   - Calculated conditional distributions:
     - \(P(X=x \,|\, Y=5)\) stored in `r1wx`.
     - \(P(Y=y \,|\, X=2)\) stored in `r1wy`.

3. **Statistical Parameters of the Joint Distribution:**
   - Computed the following parameters:
     - Mean (\(r1\_mean\)),
     - Variance (\(r1\_var\)),
     - Standard Deviation (\(r1\_std\)),
     - Covariance (\(r1\_cov\)),
     - Correlation Coefficient (\(r1\_r\)).

4. **Probability Calculations:**
   - Calculated and visualized specific joint probabilities:
     - \(P(X > 2, 0 < Y \leq 10)\) stored in `p1`.
     - \(P(X \leq 2 \,|\, X > 3, Y \geq 5)\) stored in `p2`.

5. **Independence Test:**
   - Verified the independence of \(X\) and \(Y\) using the formula:
     - \(P(X=x, Y=y) = P(X=x) \cdot P(Y=y)\).
   - Concluded that \(X\) and \(Y\) are **not independent** (`test = False`).

