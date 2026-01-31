# Marketing A/B Testing Analysis

## Project Overview

This project analyzes a real-world marketing A/B testing dataset to evaluate whether showing advertisements leads to higher conversion rates compared to showing a Public Service Announcement (PSA).

The goal is to make a data-driven business decision using statistical hypothesis testing rather than intuition.

---

## Business Problem

Marketing teams want to know:

1. Was the advertising campaign successful?
2. Did users who saw ads convert more than users who saw a PSA?
3. Is the observed difference statistically significant or due to random chance?

---

## Experiment Design

- **Control Group (PSA):** Users shown a public service announcement
- **Treatment Group (Ad):** Users shown real advertisements

Users were randomly assigned to one of the two groups.

---

## Dataset Description

**Source:** Public marketing A/B testing dataset  
**Unit of Analysis:** Individual user

### Key Columns

| Column         | Description                          |
|----------------|--------------------------------------|
| `user_id`      | Unique identifier for each user      |
| `test group`   | `ad` (treatment) or `psa` (control)  |
| `converted`    | 1 if user purchased, 0 otherwise     |
| `total ads`    | Total ads shown to the user          |
| `most ads day` | Day with highest ad exposure         |
| `most ads hour`| Hour with highest ad exposure        |

---

## Key Metric

**Conversion Rate**

```
conversion rate = total conversions / total users
```

This metric directly measures campaign effectiveness.

---

## Methodology

1. **Data Cleaning**
   - Removed unnecessary index column
   - Converted target variable to numeric format
   - Checked for missing values

2. **Exploratory Data Analysis (EDA)**
   - User distribution by group
   - Conversion counts
   - Conversion rate comparison

3. **Statistical Testing**
   - Hypothesis testing using Z-test for proportions
   - 95% confidence level
   - p-value threshold: 0.05

---

## Hypothesis

- **Null Hypothesis (H0):**  
  There is no difference in conversion rates between ad and PSA groups.

- **Alternative Hypothesis (H1):**  
  The ad group has a higher conversion rate than the PSA group.

---

## Statistical Test Used

**Z-test for proportions**

Why this test was chosen:
- Binary outcome (converted / not converted)
- Large sample size
- Comparison of two independent groups

---

## Results Summary

- The ad group showed a higher conversion rate than the PSA group.
- The p-value was below the significance level (0.05).
- The difference is statistically significant.

---

## Business Recommendation

Based on the statistical evidence, the advertising campaign had a positive impact on conversions.

**Recommendation:** Scale the ad campaign to reach more users.

---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- SciPy
- Statsmodels
- Jupyter Notebook

---

## Project Structure

```
├── analysis_code.ipynb
├── marketing_AB.csv
├── requirements.txt
├── README.md
```

---

## Skills Demonstrated

- A/B Testing
- Hypothesis Testing
- Statistical Analysis
- Data Cleaning
- Business Decision Making
- Data Visualization

---



This A/B testing analysis successfully demonstrated that the advertising campaign outperformed the public service announcement in driving user conversions. By applying rigorous statistical methods, we rejected the null hypothesis and confirmed that the difference in conversion rates between the two groups is statistically significant and not due to random chance.

The findings provide strong evidence to support continued investment in the advertising strategy. This project highlights the importance of using data-driven approaches to validate marketing decisions, ensuring that business resources are allocated effectively based on measurable outcomes rather than assumptions.
