# 📊 Retail Sales Statistical Analysis Project

## 📋 Project Overview
A comprehensive statistical analysis of retail sales data from a retail company operating both online and physical stores across multiple regions. The analysis aims to understand sales performance, evaluate marketing effectiveness, and provide data-driven business recommendations using statistical methods.

---

## 📁 Dataset Information

**File:** `statistics_sales_project_data.csv`  
**Records:** 1,460+ daily transactions  
**Time Period:** January 2023 - April 2026 (3+ years)

### Columns:
| Column | Description | Type |
|--------|-------------|------|
| `date` | Transaction date | DateTime |
| `store_type` | Online or Physical store | Categorical |
| `region` | Region of sale (Central, Coast, Nairobi, Rift Valley, Western) | Categorical |
| `units_sold` | Number of units sold | Integer |
| `revenue` | Total revenue in Kenyan Shillings (KES) | Float |
| `marketing_campaign` | Whether marketing campaign was active (Yes/No) | Boolean |

---

## 🎯 Project Objectives

### Business Questions:
1. How are sales performing across different store types and regions?
2. Is the new marketing strategy actually improving revenue?
3. How reliable are our sales insights?

### Statistical Learning Objectives:
1. **Descriptive Statistics** - Central tendency and distribution shape
2. **Data Visualization** - Multiple chart types for different insights
3. **Sampling and Bias** - Awareness of sampling methods
4. **Central Limit Theorem** - Understanding sample mean distributions
5. **Hypothesis Testing** - One-tailed and two-tailed tests
6. **Error Interpretation** - Type I and Type II errors
7. **Effect Size & Power** - Practical significance assessment

---

## 📈 Analysis Results Summary

### Part 1: Descriptive Statistics

#### Task 1.1 – Central Tendency (Monthly Revenue)
| Measure | Value (KES) | Recommendation |
|---------|------------|----------------|
| Mean | [Ksh 248,159.22] | Primary measure if no outliers |
| Median | [KSH 250,308.56] | Better if outliers present |
| Mode | [Less informative] | Less useful for continuous data |

**Key Finding:** [Median/Mean] is the best measure because [explanation based on outlier analysis].

#### Task 1.3 – Distribution Shape
- **Skewness:** [0.749] → [Positive/Negative/Symmetric] distribution
- **Kurtosis:** [0.614] → [Heavy/Light/Normal] tails
- **Interpretation:** Revenue distribution shows [description of shape pattern]

---

### Part 2: Data Visualization

#### Four Key Visualizations:
1. **Line Chart** - Monthly Revenue Trends
   - Shows: Seasonal patterns, growth trends, revenue fluctuations
   - Insight: [Peak months, growth rate, anomalies]

2. **Bar Chart** - Revenue by Store Type
   - Shows: Online vs Physical store performance
   - Insight: [Which performs better, by what margin]

3. **Box Plot** - Revenue by Region
   - Shows: Distribution, median, spread, outliers per region
   - Insight: [Most consistent region, highest median, outliers]

4. **Scatter Plot** - Units Sold vs Revenue
   - Shows: Correlation between units and revenue
   - Insight: [Strong/Weak linear relationship, average revenue per unit]

---

### Part 3: Sampling and Bias

#### Task 3.1 – Sampling Methods
- **Random Sampling:** Each transaction has equal chance
- **Systematic Sampling:** Every nth transaction
- **Stratified Sampling:** By store type or region

#### Task 3.2 – Bias Types
- **Selection Bias:** Online-only analysis misses physical stores
- **Measurement Bias:** Revenue recording errors
- **Temporal Bias:** Seasonal fluctuations not accounted for

---

### Part 4: Central Limit Theorem

#### Task 4.2 – CLT Demonstration
- **Samples:** 200 random samples
- **Sample Size:** n = 30 transactions each
- **Observation:** Distribution of sample means approximates normal curve
- **Business Implication:** Can use normal distribution for inference even if raw data is skewed

**Why CLT Works:**
1. Averages reduce extreme values
2. Sampling variability creates symmetry
3. Mathematical guarantee with n ≥ 30
4. Enables confidence intervals and hypothesis tests

---

### Part 5: Hypothesis Testing

#### Business Question:
"Does running a marketing campaign increase average revenue per transaction?"

#### Task 5.1 – Hypotheses Formulation
- **H₀ (Null):** μ_campaign = μ_no_campaign  
  (No difference in average revenue)
- **H₁ (Alternative):** μ_campaign > μ_no_campaign  
  (Campaign increases average revenue)
- **Test Type:** One-tailed t-test (right-tailed)
- **Confidence Level:** 95%
- **Alpha (α):** 0.05

#### Task 5.2 – Statistical Test Results
| Metric | Value |
|--------|-------|
| Test Statistic (t) | [4.3357] |
| p-value (one-tailed) | [0.0000] |
| Decision at α=0.05 | [Reject/Fail to reject H₀] |
| Conclusion | [Campaign does/does not increase revenue] |

---

### Part 6: Errors and Interpretation

#### Task 6.1 – Statistical Errors

**Type I Error (False Positive):**
- **Statistical:** Reject H₀ when it's true
- **Business:** Conclude campaign works when it doesn't
- **Consequence:** Wasted marketing budget, false confidence
- **Probability:** α = 0.05 (5% risk we accept)

**Type II Error (False Negative):**
- **Statistical:** Fail to reject H₀ when it's false
- **Business:** Conclude campaign doesn't work when it does
- **Consequence:** Missed revenue opportunity
- **Probability:** β (depends on sample size and effect)

**Type I Error Example Impact:**


---

### Part 7: Effect Size and Power

#### Task 7.1 – Effect Size (Cohen's d)
| Metric | Value | Interpretation |
|--------|-------|----------------|
| Cohen's d | [0.265] | [Small/Medium/Large] effect |
| Mean Difference | KES [Value] | [Percentage]% increase |
| Effect Category | [Very Small/Small/Medium/Large] | |

**Effect Size Guidelines:**
- **d < 0.2:** Negligible effect (not practically meaningful)
- **0.2 ≤ d < 0.5:** Small effect (noticeable but minor)
- **0.5 ≤ d < 0.8:** Medium effect (practically important)
- **d ≥ 0.8:** Large effect (substantial difference)

#### Task 7.2 – Power Discussion
- **Current Power:** [XX]% (probability of detecting true effect)
- **Recommended Power:** ≥80% for reliable testing
- **Why Low Power Matters:** Risk of Type II error (missing real effects)

**Should Company Collect More Data?**
- **Yes, if:** Current power < 80% AND effect size is meaningful
- **No, if:** Power already high OR effect is too small to matter economically

**Power Increase Example:**
- Current (n=[current]): [XX]% power
- With n=500 per group: [YY]% power
- Recommendation: [Collect more data/Current sample sufficient]

---

## 🏢 Business Recommendations

### 1. Marketing Strategy: