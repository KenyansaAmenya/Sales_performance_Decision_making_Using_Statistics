# Retail Sales Statistical Analysis Project
📊 Project Overview
A comprehensive statistical analysis of retail sales data to evaluate performance, test marketing effectiveness, and provide data-driven business recommendations.

📁 Dataset
File: statistics_sales_project_data.csv

Columns:

date: Transaction date

store_type: Online / Physical

region: Region of sale (Central, Coast, Nairobi, Rift Valley, Western)

units_sold: Number of units sold

revenue: Total revenue in KES

marketing_campaign: Yes / No

Time Period: January 2023 - April 2026 (3+ years of transaction data)

🎯 Project Objectives
Apply descriptive statistics to understand sales performance

Visualize sales patterns and distributions

Apply sampling theory and Central Limit Theorem

Conduct hypothesis testing on marketing effectiveness

Understand statistical errors and their business implications

Calculate effect sizes and statistical power

📈 Analysis Performed
Part 1: Descriptive Statistics
Task 1.1: Central tendency measures (Mean, Median, Mode) for monthly revenue

Task 1.3: Distribution shape analysis (skewness, kurtosis)

Part 2: Data Visualization
Line chart: Revenue trends over time

Bar chart: Revenue by store type (Online vs Physical)

Box plot: Revenue distribution by region

Scatter plot: Units sold vs Revenue

Part 3: Sampling and Bias
Task 3.1: Sampling methods comparison

Task 3.2: Systematic vs Random sampling

Part 4: Central Limit Theorem
Task 4.2: Demonstrate CLT with 200 samples (n=30)

Show convergence to normal distribution

Part 5: Hypothesis Testing
Business Question: Does marketing campaign increase average revenue?

Task 5.1: Hypotheses formulation (H₀, H₁)

Task 5.2: t-test execution and decision making

Part 6: Errors and Interpretation
Task 6.1: Type I vs Type II errors in business context

Real-world implications of statistical errors

Part 7: Effect Size and Power
Task 7.1: Cohen's d calculation and interpretation

Task 7.2: Statistical power analysis and recommendations

🔧 Technical Implementation
Prerequisites
bash
pip install pandas numpy matplotlib seaborn scipy statsmodels
Required Libraries
python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
from scipy import stats
from statsmodels.stats.power import TTestIndPower
Key Code Snippets
1. Data Loading and Preparation
python
df = pd.read_csv('statistics_sales_project_data.csv')
df['date'] = pd.to_datetime(df['date'])
2. Monthly Revenue Calculation
python
df['month'] = df['date'].dt.strftime('%Y-%m')
monthly_revenue = df.groupby('month')['revenue'].sum()
3. Marketing Campaign Hypothesis Test
python
from scipy.stats import ttest_ind
revenue_with = df[df['marketing_campaign'] == 'Yes']['revenue']
revenue_without = df[df['marketing_campaign'] == 'No']['revenue']
t_stat, p_value = ttest_ind(revenue_with, revenue_without, equal_var=False)
4. Effect Size Calculation
python
# Cohen's d
mean_diff = revenue_with.mean() - revenue_without.mean()
pooled_std = np.sqrt(((n1-1)*std1**2 + (n2-1)*std2**2) / (n1 + n2 - 2))
cohens_d = mean_diff / pooled_std
📋 Key Findings
1. Central Tendency
Mean Monthly Revenue: [Value]

Median Monthly Revenue: [Value]

Recommendation: Use [Mean/Median] due to [presence/absence] of outliers

2. Distribution Characteristics
Revenue distribution is [positively/negatively] skewed

Kurtosis indicates [heavy/light] tails

3. Marketing Campaign Effectiveness
Statistical Result: [Significant/Not significant] (p = [value])

Effect Size: [Small/Medium/Large] (Cohen's d = [value])

Business Recommendation: [Continue/Discontinue/Further test] marketing campaigns

4. Statistical Power
Current power: [XX]%

Recommended action: [Collect more data/Current sample sufficient]

🎓 Statistical Concepts Demonstrated
Descriptive Statistics: Measures of center and spread

Data Visualization: Multiple chart types for different insights

Sampling Theory: Random vs systematic sampling

Central Limit Theorem: Convergence of sample means to normal distribution

Hypothesis Testing: One-tailed t-test for marketing effectiveness

Error Types: Type I (false positive) vs Type II (false negative)

Effect Size: Practical significance beyond p-values

Statistical Power: Ability to detect true effects

📊 Business Insights
Marketing Recommendations
Based on statistical test: [Actionable recommendation]

Effect size consideration: [Economic vs statistical significance]

Risk assessment: [Type I/II error implications]

Operational Insights
Best performing store type: [Online/Physical]

Regional performance: [Top performing region]

Seasonal patterns: [Trends over time]

🚀 How to Run the Analysis
Clone/Download the project files

Install dependencies: pip install -r requirements.txt

Run Jupyter Notebook or Python script

Follow the analysis flow from Part 1 to Part 7

Modify parameters for different scenarios

📚 Educational Value
This project demonstrates:

Real-world application of statistical concepts

Business problem formulation as statistical questions

Interpretation of results in business context

Decision making under uncertainty

Communication of statistical findings to non-technical stakeholders

📄 License
Educational Use - For learning and demonstration purposes

👥 Author
Statistical Analysis Project - Retail Sales Data