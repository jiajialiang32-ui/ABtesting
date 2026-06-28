# Premium Subscription Pricing Optimization: A/B Testing and Z-Test Analysis

## Project Overview
This project evaluates the behavioral and financial impact of an optimized pricing page interface for a FinTech platform. Using a reproducible data pipeline, the analysis simulates user behavior, validates assumptions, performs statistical testing, and translates results into a revenue projection.

---

## Key Business Outcomes
* **Statistical certainty:** Achieved a **P-value of 0.0055**, demonstrating a statistically significant result against a standard $\alpha = 0.05$ threshold.
* **Conversion performance:** Increased the subscription conversion rate from **10.15%** to **11.89%**, delivering a **17.15% relative lift**.
* **Financial projection:** Estimated an annualized revenue increase of **$870,233.15** based on 1,000,000 visitors and a $50 average order value.

---

## Data Pipeline and Methodology

### 1. Experimental Design and Simulation
The project simulates 10,000 unique users and assigns them to control and treatment cohorts. The conversion outcome is generated using Bernoulli trials via `np.random.binomial`, and a fixed random seed ensures reproducibility.

* **Control Group ($n = 5,027$):** Legacy pricing page with a base conversion probability of **0.10**.
* **Treatment Group ($n = 4,973$):** New pricing page with a planned conversion probability of **0.12**.

### 2. Hypothesis Testing
The analysis uses a two-sample **Z-test for proportions** from `statsmodels` to compare conversion rates and estimate statistical significance.

$$H_0: p_{treatment} = p_{control}$$
$$H_1: p_{treatment} \neq p_{control}$$

---

## Tools and Libraries Used
* Python 3
* NumPy
* Pandas
* Seaborn
* Matplotlib
* Statsmodels
* Jupyter Notebook

Additional optional tools for visualization and reporting:
* Power BI
* Microsoft Excel

---

## Visual Evidence

<table>
  <tr>
    <td align="center"><b>Conversion Rate by Group</b></td>
    <td align="center"><b>Absolute Lift with 95% CI</b></td>
  </tr>
  <tr>
    <td><img src="notebooks/data/A:B Test Results Plot.png" width="450" alt="Conversion Rate Comparison"></td>
    <td><img src="notebooks/data/A:B Test Results Plot2.png" width="450" alt="Absolute Lift Confidence Interval"></td>
  </tr>
</table>

---

## Strategic Recommendations
1. Fully deploy the treatment pricing page, given the statistically significant conversion lift.
2. Monitor post-launch retention and average order value to confirm the long-term impact.
3. Conduct follow-up analysis by device and traffic segment to identify the strongest opportunities.

---

## How to Run the Project
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd ABtesting
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
3. Open the notebook:
   ```bash
   jupyter lab notebooks/premium_subscription_optimization.ipynb
   ```

## Data
The `data/` directory contains an optional simulated dataset export: `data/simulated_user_data.csv`.
