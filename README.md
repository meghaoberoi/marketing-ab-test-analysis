# Marketing A/B Test Analysis

Statistical analysis of a marketing campaign A/B test to determine the effectiveness of ads vs. a PSA control group, with segmentation by exposure level and time-of-day analysis.

## Overview
- **Dataset:** 588,101 users
- **Test Groups:** Ad campaign vs. Public Service Announcement (PSA)
- **Objective:** Determine if ads significantly improve conversion rates

## Key Findings
1. **Simpson's Paradox:** The aggregate relative lift of 43% (p < 0.001) is misleading. When segmented by ad exposure level, only high-exposure users show a significant positive lift (55.4%, p < 0.001). Low and medium exposure users show negative or negligible lift, which is not statistically significant (p = 0.47 and p = 0.96 respectively).

2. **Early Morning Compliers:** Users whose ad exposure was concentrated in early morning hours (12am–6am) show near-zero organic conversion rates in the PSA group, while the ad group shows non-zero conversion. This suggests strong causal effectiveness of ads in these hours — these users are perfect compliers who would not have converted without the ad.

3. **Time-of-Day Pattern:** Conversion rates follow an inverted U shape across the day, peaking at mid-afternoon (~3–4pm) for both groups. This pattern holds across all exposure levels, though the magnitude of lift is strongest for high-exposure users.

## Methodology
- Exploratory data analysis on 588K+ users
- Chi-square hypothesis testing for statistical significance (overall and by exposure level)
- Exposure level segmentation using tertile binning (Low / Medium / High) to uncover Simpson's Paradox
- Time-based analysis by day of week and hour of day, segmented by exposure level
- Effect size calculation (absolute and relative lift) for all segments
- Complier analysis using PSA group as counterfactual for causal inference

## Recommendations
1. **Minimum frequency threshold:** Set a minimum ad exposure level before counting a user as treated — low and medium exposure users show no significant lift
2. **Target early morning hours:** Ads are most causally effective between 12am–6am when organic intent is lowest
3. **Maximize frequency for high-exposure users:** The lift is only significant and positive for high-exposure users — concentrate budget here
4. **Always segment results:** Reporting only aggregate lift overstates campaign effectiveness

## Tools & Technologies
- **Python:** pandas, NumPy, scipy, matplotlib, seaborn
- **Statistical Methods:** Chi-square hypothesis testing, effect size analysis, causal inference (complier analysis)
- **Visualization:** matplotlib, seaborn — bar charts, line plots, segmented subplots

## Project Structure
```
├── marketing_AB.csv              # Dataset
├── Marketing_AB_Testing.ipynb    # Full analysis
├── .gitignore
└── README.md                     # Project documentation
```

## How to Run
1. Clone this repository
2. Install dependencies: `pip install pandas numpy scipy matplotlib seaborn`
3. Open `Marketing_AB_Testing.ipynb` in Jupyter Notebook
4. Run all cells

## Dataset
Marketing A/B testing dataset from Kaggle analyzing conversion rates between an ad campaign and PSA control group.

## Author
Megha Oberoi
