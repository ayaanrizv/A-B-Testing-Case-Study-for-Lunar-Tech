# A-B-Testing-Case-Study-for-Lunar-Tech

This Python-based project demonstrates a simulated A/B testing workflow, a widely adopted statistical approach used to compare two variations of a feature or experience to evaluate performance differences. The project highlights how A/B testing can be applied in real-world product analytics and decision-making scenarios.

![Control](https://github.com/TatevKaren/CaseStudies/assets/76843403/08318891-36ab-49da-acc5-6eca9a5780c0)

## 1. Generating Simulated Click Data for A/B Testing

### Objective
To create synthetic click interaction data for both the experimental (`exp`) and control (`con`) groups.

### Approach
- Uses the `numpy` and `pandas` libraries to generate randomized binary click outcomes (`1` representing a click and `0` representing no interaction).
- Builds two separate datasets:
  - `df_exp` for the experimental variation
  - `df_con` for the control variation
- Each dataset contains `1000` observations with different click probabilities:
  - `0.5` for the experimental group
  - `0.2` for the control group
- Combines both datasets into a consolidated DataFrame named `df_ab_test` for further statistical analysis.

![Unknown](https://github.com/TatevKaren/CaseStudies/assets/76843403/7b754602-d3a7-42ad-961c-9e9b276aa9ed)

## 2. Measuring Statistical Significance in A/B Testing

### Objective
To evaluate whether the observed difference in click-through rates between the experimental and control groups is statistically meaningful.

### Approach
- Computes:
  - total clicks (`X_con`, `X_exp`)
  - estimated click probabilities (`p_con_hat`, `p_exp_hat`)
- Calculates:
  - pooled click probability (`p_pooled_hat`)
  - pooled variance
- Determines the standard error (`SE`) to assess the reliability of the estimated click rates.
- Executes a two-sample Z-test by calculating:
  - test statistic (`Test_stat`)
  - critical value (`Z_crit`)
  - p-value
- Establishes a confidence interval (`CI`) to estimate the likely range of the true difference between click probabilities.

## Business Application: A/B Testing Case Study

### Scenario
A digital platform is comparing two webpage layouts to identify which version drives stronger user engagement, measured through click activity.

### Workflow
- Users in the `exp` group interact with the redesigned webpage experience.
- Users in the `con` group continue viewing the original webpage version.
- The script simulates click behavior for both groups and computes click-through rates.
- Statistical analysis is then performed to determine whether the updated design produces a meaningful improvement in engagement.

## 📊 A/B Test Dashboard Overview

<img width="1416" height="792" alt="image" src="https://github.com/user-attachments/assets/53326399-4352-458e-a03a-8808b1354ab2" />

*Dashboard showing CTR comparison and trend over time.*

## Conclusion

### Key Insights
The analysis provides statistical evidence indicating whether the experimental webpage design generates a significantly higher click-through rate than the control version.

![ABtesting_figure](https://github.com/TatevKaren/CaseStudies/assets/76843403/a8ada9b2-4fe2-4381-875f-199d7a9a9c22)

### Decision-Making Process
Final implementation decisions are guided by:
- the p-value
- confidence interval analysis
- statistical significance thresholds

These insights help determine whether the redesigned webpage should be rolled out more broadly across the platform.

---

*This case study demonstrates how A/B testing can support data-driven product optimization, digital experimentation, customer engagement analysis, and user experience improvement initiatives.*
