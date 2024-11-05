This repository contains the code to reproduce the results of the article: "A Novel Approach to Performance Evaluation of Current Controllers in Power Converters and Electric Drives Using Non-Parametric Analysis".

Description

In this study, in the real data section the performance of two types of controllers (MPC and M2PC) is evaluated in terms of their error and harmonic distortion. Specifically, the following metrics were used:
- **Mean Squared Error (MSE):** Calculated for each controller type over 200 tests.
- **Total Harmonic Distortion (THD):** Measured over the same tests for both MPC and M2PC controllers.

The code in this repository allows you to:
1. Calculate descriptive statistics (minimum, maximum, mean, standard deviation) for MSE and THD values.
2. Extract samples from the MSE and THD data for normality testing using the Lilliefors test.
3. Rank the THD values of both controllers and display a combined ranking.
4. Conduct a Mann-Whitney U test to compare the THD distributions of the two controllers.

## Requirements

- R version 4.0 or later
- Required R packages:
  - `nortest` (for Lilliefors normality test)

## Usage

1. **Run the Descriptive Analysis**
   - The code calculates the minimum, maximum, mean, and standard deviation for both MSE and THD values of each controller.
   - The results are stored in a data frame and printed for easy reference.

2. **Sample Extraction and Normality Testing**
   - Sample subsets of 30 values are taken from the full MSE and THD data for each controller.
   - Normality is tested using the Lilliefors test, and p-values are displayed.

3. **Ranking THD Values**
   - The THD values for MPC and M2PC are combined, ranked, and displayed in ascending order.
   - This table provides a comparative ranking of THD for both controllers.

4. **Non-Parametric Comparison (Mann-Whitney U Test)**
   - A Mann-Whitney U test is performed to evaluate the difference between the THD distributions of MPC and M2PC.

## Running the Code

To run the code, open the R script in this repository and execute it. Make sure to install any missing packages before running the script.

## Example Output

- **Table III**: Descriptive statistics (Min, Max, Mean, SD) for MSE and THD for each controller.
- **Table IV**: p-values from the Lilliefors test to assess normality of MSE and THD samples.
- **Table V**: Ranked THD values for both MPC and M2PC.
- **Mann-Whitney U Test**: p-value indicating whether there is a significant difference in THD distributions.

## Contact
For questions or further information, please contact the author of the repository (grivas@facenuna.edu.py) or refer to the article for additional context.
