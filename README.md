# Marketing A/B Test Analysis

Statistical analysis of a marketing campaign A/B test to determine effectiveness of ads vs. PSA (control group).

## Overview
- **Dataset:** 588,101 users
- **Test Groups:** Ad campaign vs. Public Service Announcement (PSA)
- **Objective:** Determine if ads significantly improve conversion rates

## Key Findings
- **Overall lift:** 43% relative improvement in conversion rate (p < 0.001)
- **Simpson's Paradox:** Aggregate lift is misleading — when segmented by ad exposure level, only high-exposure users show a significant positive lift (55.4%, p < 0.001). Low and medium exposure users show negative or negligible lift (not statistically significant)
- **Early morning compliers:** Users whose ad exposure was concentrated in early morning hours (12am–6am) show near-zero organic conversion rates in the PSA group, making them perfect compliers — the ad is doing real causal work in these hours
- **Time-of-day pattern:** Conversion rates follow an inverted U shape, peaking at mid-afternoon (~3–4pm) for both groups
- **Recommendation:** Maximize ad frequency and concentrate delivery in early morning hours for strongest causal impact

## Methodology
- Chi-square test for statistical significance
- Conversion rate analysis by test group
- Data visualization and exploratory analysis

## Tools & Technologies
- **Python:** pandas, NumPy, scipy, matplotlib, seaborn
- **Statistical Methods:** Hypothesis testing, chi-square test
- **Visualization:** matplotlib for charts and graphs

## Project Structure
```

├── marketing_AB.csv              # Dataset
├─Marketing_AB_Testing.ipynb    # Full analysis
└── README.md                      # Project documentation
```

## How to Run
1. Clone this repository
2. Install dependencies: `pip install pandas numpy scipy matplotlib seaborn`
3. Open `notebooks/Marketing_AB_Testing.ipynb` in Jupyter Notebook
4. Run all cells

## Analysis Highlights
- Explored dataset of 588K+ users
- Calculated conversion rates by test group
- Performed chi-square test (χ² = 54.01, p < 0.001)
- Built visualizations comparing group performance
- Provided data-driven business recommendation

## Dataset
Marketing A/B testing dataset from Kaggle analyzing conversion rates between ad campaign and PSA (control) groups.

## Author
Megha Oberoi
