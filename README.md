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

### cwl4: Exploratory Data Analysis Elements

1. **Selected Plot Types for a Single Parameter:**
   - Created a figure with 2x2 subplots, showcasing different plot types for the `Alcohol` parameter grouped by grape cultivars:
     - Boxplot with a custom color and mean marker,
     - Violinplot with a custom color,
     - Stripplot with adjusted point size, color, and transparency,
     - Swarmplot with adjusted point size and color.

2. **Plots for All Parameters by Cultivar:**
   - **Boxplots for All Parameters:**
     - Created a 2x3 subplot figure for parameters: `Alcohol`, `Malic acid`, `Ash`, `Flavanoids`, `Color intensity`, and `OD280/OD315`, grouped by grape cultivar with:
       - A consistent, custom color palette,
       - Mean markers,
       - No legends displayed.
   - **Swarmplots for All Parameters:**
     - Created a similar 2x3 subplot figure using swarmplots with:
       - A consistent, custom color palette,
       - Adjusted point sizes,
       - No legends displayed.

3. **Descriptive Statistics:**
   - Computed basic descriptive statistics for all parameters using `pandas.DataFrame.describe()`.
   - Added skewness and kurtosis for each parameter using `scipy.stats.skew()` and `scipy.stats.kurtosis()`.

4. **Linear Correlation Analysis:**
   - **Manual Calculation:**
     - Computed the linear correlation coefficient \( r \) between `OD280/OD315` (X) and `Flavanoids` (Y) using the formula for Pearson’s correlation coefficient.
   - **Using Functions:**
     - Computed a correlation matrix for all parameter pairs using `pandas.DataFrame.corr()`.
   - **Visualization:**
     - Created a heatmap of the correlation matrix using `seaborn.heatmap()` with:
       - A custom color scale,
       - Annotated values.
   - **Pairplots:**
     - Prepared pairwise scatterplots with:
       - Custom color palettes for grape cultivars,
       - Adjusted marker properties (shape, size, transparency).

5. **Linear Regression:**
   - **Manual Regression Coefficients:**
     - Calculated regression coefficients \( a_1 \) and \( b_1 \) for the linear relationship between `Flavanoids` (Y) and `OD280/OD315` (X) using the least squares method.
   - **Using Functions:**
     - Obtained regression coefficients \( a_2 \) and \( b_2 \) using `scipy.stats.linregress()`.
   - **Regression Visualization:**
     - Created a scatterplot with a regression line:
       - The line was overlaid using manually calculated coefficients.
   - **Comprehensive Regression Analysis:**
     - Generated pairplots for all parameters:
       - With a regression line for all data,
       - With separate regression lines for each cultivar,
       - Adjusted marker properties and color palettes for clarity.

### cwl5: Sampling and Representativeness in Random Samples

1. **Random Sample Scenarios:**
   - **Scenario 1:**
     - Selected the first 200 individuals passing through the main gate, sorted by `Czas przejścia przez bramę`.
     - Ensured that no individual was sampled more than once.
     - Saved result in `sample_1`.
   - **Scenario 2:**
     - Randomly sampled 200 individuals with replacement, simulating a crowd-based survey.
     - Allowed repeated sampling of individuals.
     - Saved result in `sample_2`.
   - **Scenario 3:**
     - Randomly sampled 200 individuals without replacement from the population, simulating a crowd-based survey where respondents cannot answer more than once.
     - Saved result in `sample_3`.
   - **Scenario 4:**
     - Stratified sampling approach: Selected 40 individuals from each of the 5 sectors (200 in total), ensuring equal representation from each sector.
     - Ensured no duplicates and saved result in `sample_4`.
   - **Scenario 5:**
     - Stratified sampling proportional to the population size of each sector.
     - Sampled 25% of the population from each sector without replacement.
     - Saved result in `sample_5`.
   - **Scenario 6:**
     - Cluster sampling: Randomly selected 4 buses and included all passengers in those buses in the sample.
     - Saved result in `sample_6`.

 **Strengths and Weaknesses of Sampling Methods:**
   - **Scenario 1:**
     - Strengths: Efficient and straightforward implementation.
     - Weaknesses: May not represent the diversity of the entire population.
   - **Scenario 2:**
     - Strengths: Simple and quick.
     - Weaknesses: Repeated individuals reduce sample diversity.
   - **Scenario 3:**
     - Strengths: Ensures diverse sampling by avoiding duplicates.
     - Weaknesses: Randomization may still miss certain population segments.
   - **Scenario 4:**
     - Strengths: Equal representation from all sectors ensures balance.
     - Weaknesses: Potentially labor-intensive in execution.
   - **Scenario 5:**
     - Strengths: Proportional representation ensures sample mirrors population structure.
     - Weaknesses: Implementation complexity increases with population stratification.
   - **Scenario 6:**
     - Strengths: Captures all individuals within randomly selected clusters.
     - Weaknesses: May exclude other clusters, reducing overall diversity.

 2. **Part 1: Representativeness Analysis**
   - Evaluated the representativeness of four provided random samples drawn from a population with \( N(172, 7) \).
   - Observations:
     - Sample 1 had a positively skewed distribution and lower variance than the population.
     - Sample 2 was less dispersed, with multiple peaks, showing reduced concentration around the mean.
     - Sample 3 closely mirrored the population's parameters, being the most representative.
     - Sample 4 exhibited the highest variance, with extreme outliers causing positive skewness.

3. **Part 2: Representativeness Analysis**
   - Evaluated 5000 samples (size 100 each) drawn from a population with \( N(172, 7) \), analyzing:
     - **Mean Distribution:**
       - Symmetrical around the population mean, suggesting high representativeness.
     - **Variance Distribution:**
       - Slightly asymmetric with values skewed, indicating occasional samples with outliers.
     - **Standard Deviation Distribution:**
       - Symmetrical and concentrated around the population's standard deviation (\( 7 \)).
   - **Conclusions:**
     - Representativeness depends on how well samples capture the population's diversity.
     - Larger sample sizes reduce variability, enhancing representativeness and analysis accuracy.

