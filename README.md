# Traffic Accidents, Speed Limits, and Winter Conditions  
**An Exploratory Analysis Using Correlation and Count Models**

## Author
Landan George

## Project Overview
This project analyzes traffic accident data to determine whether **posted speed limits**, **snow on the ground**, and their **combined interaction** impacts the number of reported motor vehicle accidents. The analysis was conducted using publicly available traffic and weather data and applies both exploratory statistical techniques and predictive count models.

The primary goal of this project is not only to identify statistically significant relationships, but also to assess **practical significance** and generate **actionable insights** that can support traffic safety planning and winter road management.

---

## Research Question
Do posted speed limits and winter conditions (specifically snow on the ground), individually or jointly, influence the number of traffic accidents?

---

## Hypothesis
- **H₁:** Posted speed limits and the presence of snow on the ground influence traffic accident counts.

---

## Data Description
The dataset includes:
- Traffic accident counts by date and roadway
- Posted speed limits
- Weather variables, including:
  - Mean, minimum, and maximum temperature
  - Total precipitation
  - Snow on the ground

The target variable (`count`) represents the number of reported traffic accidents.

---

## Methods Used

### 1. Pearson’s Pairwise Correlation
Pearson correlation was used as an exploratory method to assess linear relationships between individual variables and accident counts.

- Metrics: correlation coefficient (r), t-statistic, p-value
- Alpha level: 0.05

This method was used to identify general patterns but not to infer causality or interaction effects.

---

### 2. Negative Binomial Regression
A negative binomial regression model was developed to predict accident counts while accounting for overdispersion in the data.

Key features of the model:
- Log link function
- Interaction term between speed limit and snow on the ground
- Maximum likelihood estimation

This model was selected because traffic accident data are count-based and exhibit variance greater than the mean.

---

## Key Findings

### Pearson Correlation Results
- Statistically significant correlations were observed between accident counts and both speed limits and snow on the ground.
- However, correlation coefficients were small in magnitude (|r| < 0.3), indicating weak linear relationships.
- Due to the large sample size, p-values were effectively zero, but practical significance was limited.

**Conclusion:**  
Pearson correlation alone is insufficient to explain accident patterns in a meaningful or actionable way.

---

### Negative Binomial Regression Results
- The overall model was statistically significant (LLR p-value < 0.001).
- Speed limits were a significant predictor of accident counts.
- Snow on the ground alone was not consistently significant.
- **The interaction between speed limits and snow on the ground was statistically significant**, indicating that winter conditions alter accident patterns on higher-speed roads.

**Conclusion:**  
Snow and speed limits jointly influence traffic accident counts, and this interaction cannot be detected using pairwise correlation.

---

## Practical Significance
While individual variables showed weak effects in isolation, the interaction between speed limits and snow on the ground has meaningful real-world implications. The findings suggest that higher-speed roads behave differently under snowy conditions, supporting targeted winter safety strategies rather than uniform policies across all road types.

---

## Recommendations
1. **Prioritize high-speed roadways for enhanced winter maintenance and safety measures** during periods of snow, including proactive snow clearing and temporary winter speed advisories.
2. **Integrate interaction-based statistical modeling** into ongoing traffic safety analysis to better anticipate risk under combined roadway and weather conditions.

---

## Limitations
- The analysis focuses on reported accident counts and does not account for traffic volume or exposure.
- Correlation does not imply causation.
- Weather conditions are aggregated at a daily level and may not reflect localized conditions at the time of each accident.

---

## Conclusion
This project successfully demonstrates the importance of using appropriate statistical models for traffic safety analysis. While simple correlations identified weak associations, negative binomial regression provided deeper insight by accounting for overdispersion and interaction effects. The results support data-driven, targeted approaches to winter road safety and traffic planning.

---