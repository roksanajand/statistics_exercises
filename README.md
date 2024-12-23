# Statistics exercises
This repository contains a series od 12 notebooks completed during my second year of studies. It is designed to explore various statistical concepts, hypothesis testing methods, and data analysis techniques. Each notebook focuses on a specific topic, providing theoretical background, practical implementation, and visualizations to enhance understanding.
The tasks include:

1. Exploring probability distributions and descriptive statistics.
2. Conducting statistical hypothesis testing using parametric, non-parametric, bootstrap, and permutation methods.
3. Performing variance analysis and post-hoc tests such as Tukey's HSD.
4. Implementing and analyzing real-world data with custom and library-based statistical functions.
5. Visualizing results with detailed graphs and heatmaps for deeper insights.

These notebooks serve as a comprehensive guide for understanding and applying statistical methods to real-world problems, emphasizing both manual implementations and the use of Python libraries like `scipy`, `numpy`, `pandas`, and `matplotlib`. Each notebook builds upon the previous concepts, offering a structured approach to learning statistics and data analysis.


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

### cwl6: Parametric Estimation

1. **Point Estimation of the Mean:**
   - **Function:** `mean_estimation(data, alpha, population_std="unknown")`
   - **Purpose:** Computes the confidence interval for the population mean based on sample data.
   - **Key Steps:**
     - If the population standard deviation is known, use the normal distribution.
     - If the population standard deviation is unknown, use the t-distribution.
     - Compute the margin of error and calculate the confidence interval bounds.
   - **Output Format:**
     - Prints: 
       ```
       μ należy do przedziału [X, Y] przy założeniu poziomu ufności 1-α = Z
       ```
     - Returns the lower (`X`) and upper (`Y`) bounds.
   - **Examples:**
     - With population std = 0.2:
       - \(𝜇 in [4.9056, 5.0527] \) for \( 1-α = 0.9 \)
     - Without population std:
       - \( 𝜇 in [4.9134, 5.0450] \) for \( 1-α = 0.9 \)

2. **Interval Estimation of Variance:**
   - **Function:** `variance_estimation(data, alpha, population_mean="unknown")`
   - **Purpose:** Computes the confidence interval for the population variance.
   - **Key Steps:**
     - If the population mean is unknown, calculate it from the sample.
     - Use the chi-square distribution to determine the confidence interval bounds.
   - **Output Format:**
     - Prints:
       ```
       𝜎^2  należy do przedziału [X, Y] przy założeniu poziomu ufności 1-α = Z
       ```
     - Returns the lower (`X`) and upper (`Y`) bounds.
   - **Examples:**
     - With population mean = 5:
       - \( 𝜎^2 in [0.0186, 0.0553] \) for \( 1-α = 0.9 \)
     - Without population mean:
       - \( 𝜎^2 in [0.0183, 0.0544] \) for \( 1-α = 0.9 \)

3. **Confidence Interval for Pearson's Correlation Coefficient:**
   - **Function:** `correlation_estimation(data, alpha)`
   - **Purpose:** Computes the confidence interval for the Pearson correlation coefficient.
   - **Key Steps:**
     - Calculate the sample Pearson correlation coefficient.
     - Use the Fisher z-transformation to compute confidence interval bounds.
   - **Output Format:**
     - Prints:
       ```
       r należy do przedziału [X, Y] przy założeniu poziomu ufności 1-α = Z
       ```
     - Returns the lower (`X`) and upper (`Y`) bounds.
   - **Examples:**
     - \( r in [0.9495, 0.9692] \) for \( 1-α = 0.95 \)
     - \( r in [0.9476, 0.9711] \) for \( 1-α = 0.98 \)

4. **Confidence Interval for Linear Regression Coefficients:**
   - **Function:** `linear_regression_coefficients_estimation(data, alpha)`
   - **Purpose:** Computes the confidence intervals for the slope (\( a \)) and intercept (\( b \)) of a linear regression equation.
   - **Key Steps:**
     - Calculate \( a \) (slope) and \( b \) (intercept) using the method of least squares.
     - Use the t-distribution to determine confidence intervals for \( a \) and \( b \).
   - **Output Format:**
     - Prints:
       ```
       a należy do przedziału [X1, X2] przy założeniu poziomu ufności 1-α = Z1
       b należy do przedziału [X2, Y2] przy założeniu poziomu ufności 1-α = Z2
       ```
     
   - **Examples:**
     - \( a in [1.9033, 2.0245] \), \( b in [-5.331, -4.7958] \) for \( 1-α = 0.9 \)
     - \( a in [1.8916, 2.0361] \), \( b in [-5.3827, -4.7442] \) for \( 1-α = 0.95 \)

### Conclusions:
This set of tasks demonstrates parametric estimation techniques for population mean, variance, Pearson correlation, and regression coefficients. Confidence intervals provide a measure of uncertainty, allowing us to quantify the reliability of our estimates under specified confidence levels.

### cwl7: Nonparametric Estimation

1. **Histogram Visualization:**
   - Created histograms of the sample dataset using various binning strategies:
     - Default binning based on the dataset.
     - Fixed number of bins (e.g., 20 bins).
     - Fixed bin width (e.g., 0.3).
     - Custom bin edges with defined steps (e.g., 0.05, 0.15, 0.4).
   - Added a visual representation of the dataset using markers below the histogram.
   - Demonstrated the effect of different binning strategies on histogram shape.

2. **Kernel Density Estimation (KDE):**
   - **Custom Implementation:**
     - Built a KDE function from scratch using Gaussian kernels.
     - Generated smooth probability density functions by aggregating kernel contributions.
   - **scikit-learn Implementation:**
     - Utilized the `KernelDensity` class with multiple kernel types (e.g., Gaussian, Epanechnikov, Tophat).
     - Explored the effect of kernel bandwidth on density estimation:
       - Small bandwidths result in overfitting (too many peaks).
       - Large bandwidths overly smooth the data, losing finer details.

4 . **CDF Estimation:**
   - Implemented cumulative distribution function (CDF) estimation:
     - Calculated empirical CDF from the sorted dataset.
     - Computed confidence intervals based on the Kolmogorov-Smirnov distribution.
   - Visualized the CDF along with confidence intervals for specified significance levels (e.g., 0.05, 0.02).

### cwl8: Bootstrap Estimation

1. **Bootstrap Estimation of Sample Parameters:**
   - Developed the `bootstrap_parameter_estimation()` function to estimate confidence intervals for sample parameters using the bootstrap method:
     - Mean (`mean`),
     - Variance (`var`),
     - Standard deviation (`std`).
   - Results include:
     - Confidence intervals calculated based on the specified number of bootstrap samples and significance levels.
     - Printed output format: `P belongs to [X, Y] at confidence level 1-α = Z`.

2. **Bootstrap Estimation of Pearson Correlation Coefficient:**
   - Created the `bootstrap_correlation_estimation()` function to estimate confidence intervals for the Pearson correlation coefficient (`r`) using bootstrap resampling.
   - Results include:
     - Confidence intervals for the correlation coefficient based on specified parameters.
     - Printed output format: `r belongs to [X, Y] at confidence level 1-α = Z`.

3. **Bootstrap Estimation of Linear Regression Coefficients:**
   - Developed the `bootstrap_linear_regression_coefficients_estimation()` function to estimate confidence intervals for:
     - Slope (`a`),
     - Intercept (`b`).
   - Results include:
     - Confidence intervals for regression coefficients calculated using bootstrap resampling.
     - Printed output format: `a belongs to [X1, Y1] at confidence level 1-α = Z1` and `b belongs to [X2, Y2] at confidence level 1-α = Z2`.

4. **Bootstrap Estimation Using `scipy.stats.bootstrap()`:**
   - Used `scipy.stats.bootstrap()` to estimate confidence intervals for various sample parameters:
     - Mean, variance, and standard deviation of `sample_1`.
     - Pearson correlation coefficient, slope, and intercept for `sample_2`.
   - Results include:
     - Automatically calculated confidence intervals for each parameter at a significance level of 1-α = 0.98.
     - Values stored in variables `mean_ci`, `var_ci`, `std_ci`, `r_ci`, `a_ci`, and `b_ci`.

### cwl9: Hypothesis Testing - Parametric Tests

1. **Testing Hypothesis About the Mean:**
   - Created the `mean_NHST()` function to test hypotheses about the mean of a sample:
     - Supports three types of alternative hypotheses: two-sided, less, and greater.
     - Outputs include:
       - Test statistic (\(t\)),
       - Critical value (\(t_alpha\)),
       - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.

2. **Testing Hypothesis About Variance:**
   - Developed the `variance_NHST()` function to test hypotheses about sample variance:
     - Supports three types of alternative hypotheses: two-sided, less, and greater.
     - Outputs include:
       - Test statistic (\(\chi^2\)),
       - Critical values (\(\chi^2_alpha\)),
       - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.

3. **Testing Hypothesis About Proportions:**
   - Prepared the `proportion_NHST()` function to test hypotheses about proportions in binary samples:
     - Supports three types of alternative hypotheses: two-sided, less, and greater.
     - Outputs include:
       - Test statistic (\(u\)),
       - Critical value (\(u_alpha\)),
       - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.

4. **Hypothesis Testing Using Dedicated Functions:**
   - a) **Coin Toss Test:**
     - Used `scipy.stats.binomtest()` to test if a coin is fair.
     - Results:
       - \(p\)-value stored in `pvalue_1`.
       - Test result (\(H_1\)): 1 if \(H_0\) (coin is fair) is rejected, 0 otherwise.
   - b) **Single Sample Mean Test:**
     - Tested if the mean weight of products from the first production line equals 0.5kg using `scipy.stats.ttest_1samp()` with a one-sided alternative hypothesis.
     - Results:
       - \(p\)-value stored in `pvalue_2`.
       - Test result (\(H_2\)): 1 if \(H_0\) (mean equals 0.5kg) is rejected, 0 otherwise.
   - c) **Paired Samples Test:**
     - Used `scipy.stats.ttest_rel()` to test if the mean weight from the second production line is higher than the first.
     - Results:
       - \(p\)-value stored in `pvalue_3`.
       - Test result (\(H_3\)): 1 if \(H_0\) (means are equal) is rejected, 0 otherwise.

 **Visualization:**
   - All functions provide visualizations using the `vizualize_test_result()` helper function:
     - Displays the probability density function (PDF) of the test statistic's theoretical distribution.
     - Highlights critical regions and indicates the test statistic value.

### cwl10: Hypothesis Testing - Non-Parametric Tests

1. **Chi-Square Test for Homogeneity:**
   - Prepared data for a Chi-Square test using `chi2_NHST()`:
     - Theoretical probabilities for the number of heads in 20 coin tosses were computed using `scipy.stats.binom.pmf()`.
     - Observed counts were calculated using `np.bincount()`.
   - Outputs include:
     - Test statistic (\(\chi^2\)),
     - Critical value (\(\chi^2_\alpha\)),
     - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.

2. **Normality Tests:**
   - a) **Shapiro-Wilk Test for Normality:**
     - Used `scipy.stats.shapiro()` to test if the bill depth of Gentoo penguins follows a normal distribution.
     - Results:
       - \(p\)-value stored in `pvalue_1`.
       - Test result (\(H_1\)): 1 if \(H_0\) is rejected, 0 otherwise.
   - b) **Kolmogorov-Smirnov Test for Normality:**
     - Tested if the flipper length of Adelie penguins follows a normal distribution with a mean of 190 and a standard deviation of 6 using `scipy.stats.kstest()`.
     - Results:
       - \(p\)-value stored in `pvalue_2`.
       - Test result (\(H_2\)): 1 if \(H_0\) is rejected, 0 otherwise.
   - c) **Chi-Square Goodness-of-Fit Test:**
     - Used `scipy.stats.chisquare()` to test if the flipper lengths of Adelie penguins follow a normal distribution with a mean of 190 and a standard deviation of 6:
       - Binned observed values using `np.histogram()`.
       - Calculated expected frequencies using `scipy.stats.norm.cdf()`.
     - Results:
       - \(p\)-value stored in `pvalue_3`.
       - Test result (\(H_3\)): 1 if \(H_0\) is rejected, 0 otherwise.
   - d) **Two-Sample Kolmogorov-Smirnov Test:**
     - Used `scipy.stats.ks_2samp()` to test if the flipper length distributions of Adelie and Chinstrap penguins are identical:
       - Compared the empirical distribution functions of the two samples.
     - Results:
       - \(p\)-value stored in `pvalue_4`.
       - Test result (\(H_4\)): 1 if \(H_0\) is rejected, 0 otherwise.

### cwl11: Hypothesis Testing - Bootstrap and Permutation Tests

1. **Bootstrap Test for Mean:**
   - Implemented `bootstrap_mean_NHST()` to test the hypothesis about the mean of a population using the bootstrap method:
     - Generated bootstrap samples by resampling with replacement.
     - Computed \(p\)-value based on the bootstrap distribution.
     - Results include:
       - \(p\)-value,
       - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.

2. **Bootstrap Test for Two Means:**
   - Implemented `bootstrap_means_NHST()` to test the hypothesis about the means of two populations using the bootstrap method:
     - Created a combined bootstrap population.
     - Generated bootstrap samples for both groups and computed differences in means.
     - Results include:
       - \(p\)-value,
       - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.

3. **Permutation Test for Two Means:**
   - Implemented `permutation_means_NHST()` to test the hypothesis about the means of two populations using a permutation test:
     - Mixed both samples and permuted the data.
     - Calculated differences in means for each permutation.
     - Results include:
       - \(p\)-value,
       - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.

4. **Permutation Test Using Dedicated Function:**
   - a) **Test for Mean Differences:**
     - Used `scipy.stats.permutation_test()` to test if the means of two populations are different.
     - Results:
       - \(p\)-value stored in `pvalue_1`,
       - Test result (\(H_1\)): 1 if \(H_0\) is rejected, 0 otherwise.
   - b) **Test for Variance Differences:**
     - Used `scipy.stats.permutation_test()` to test if the variance of one population is greater than the other.
     - Results:
       - \(p\)-value stored in `pvalue_2`,
       - Test result (\(H_2\)): 1 if \(H_0\) is rejected, 0 otherwise.

### cwl12: Analysis of Variance (ANOVA)

1. **One-Way ANOVA:**
   - Implemented `one_way_anova()` to test the hypothesis about the equality of means across multiple groups:
     - Computed the F-statistic and compared it with the critical F-value.
     - Results include:
       - \(F\)-statistic,
       - \(F_alpha\) critical value,
       - Test result (\(H\)): 1 if \(H_0\) is rejected, 0 otherwise.
     - Visualization included the probability density function of the F-distribution with rejection regions highlighted.

2. **Tukey's HSD Test:**
   - Implemented `tukey_HSD_test()` to compare all pairs of groups for mean differences:
     - Computed the Tukey's HSD statistic for each pair.
     - Results include:
       - HSD statistic matrix,
       - \(HSD_alpha\) critical value,
       - Decision matrix (H): 1 if \(H_0\) is rejected for a pair, 0 otherwise.
     - Visualization displayed a heatmap of results with a color scale centered on \(HSD_\alpha\).

3. **Using Dedicated Functions:**
   - a) One-Way ANOVA Using `scipy.stats.f_oneway()`:
     - Tested the equality of means across groups in `test_data_2`.
     - Results:
       - \(p\)-value stored in `pvalue_1`,
       - Test result (H_1): 1 if \(H_0\) is rejected, 0 otherwise.
   - b) Tukey's HSD Using `scipy.stats.tukey_hsd()`:
     - Tested pairwise differences in means across groups in `test_data_2`.
     - Results:
       - Matrix of p-values stored in `pvalue_2`,
       - Decision matrix (H_2): 1 if \(H_0\) is rejected for a pair, 0 otherwise.

