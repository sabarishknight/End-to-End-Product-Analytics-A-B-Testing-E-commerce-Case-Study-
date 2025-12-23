# End-to-End Product Analytics & A/B Testing

## Overview
This project demonstrates a complete product analytics workflow using real
e-commerce behavior data. The goal is to evaluate whether a new product
recommendation feature improves user conversion and revenue.

The project follows an industry-style approach:
- Understand raw user behavior
- Define success metrics aligned with product goals
- Simulate an A/B experiment
- Apply statistical testing
- Make a clear ship / no-ship product decision

This project is designed to be relevant for Data Analyst, Business Analyst,
Product Manager, and Data Scientist roles.

---

## Dataset
**Source:** E-commerce Behavior Data from Multi-Category Store (Kaggle)

- Event-level user interactions (view, add-to-cart, purchase)
- Two months of data (Oct–Nov 2019)
- ~1 million sampled events
- Each row represents a single user action

---

## Business Problem
A new product recommendation experience is proposed to improve user conversion.

**Key question:**
> Does the new recommendation feature increase product view → purchase
conversion without negatively impacting revenue?

---

## Project Structure
product-ab-testing/
├── notebooks/
│ ├── 01_exploration.ipynb
│ ├── 02_metric_design.ipynb
│ ├── 03_ab_test.ipynb
│ └── 04_decision.ipynb


---

## Notebook Breakdown

### 01_exploration.ipynb — Data Exploration
- Load and clean raw event data
- Understand user behavior and funnel structure
- Validate data quality
- Identify baseline conversion behavior

Key finding:
- ~8.2% of users who view a product make a purchase
- Cart is an optional step in the user journey

---

### 02_metric_design.ipynb — Metric Design
- Define product success metrics
- Select primary, secondary, and guardrail metrics
- Establish baseline values before experimentation

Primary metric:
- Conversion Rate (View → Purchase)

Secondary metrics:
- Add-to-cart rate
- Average Order Value (AOV)

Guardrail:
- Revenue per user (RPU)

---

### 03_ab_test.ipynb — A/B Test Simulation
- Randomly assign users to control and variant groups
- Compute metrics by group
- Apply statistical tests:
  - Two-proportion z-test for conversion
  - Welch’s t-test for revenue

Result:
- No statistically significant improvement in conversion or revenue

---

### 04_decision.ipynb — Product Decision
- Interpret experimental results
- Make a final product recommendation
- Discuss risks, limitations, and next steps

Final decision:
❌ Do Not Ship

Rationale:
- Observed uplift is small and not statistically significant
- No measurable revenue impact
- Shipping would add complexity without proven user value

---

## Key Takeaways
- Demonstrates end-to-end product analytics thinking
- Shows correct metric selection and funnel interpretation
- Applies statistical rigor to decision-making
- Emphasizes preventing unproven features from shipping

---

## Tech Stack
- Python
- Pandas, NumPy
- SciPy
- Jupyter Notebook

---
