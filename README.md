# Health-Data-Analysis-Healthy-Minds-Survey-Data-
I conducted an analysis of the Healthy Minds Survey data from the University of Michigan (and other U.S. universities), examining the correlation between financial stressors and mental health among college students during the 2024–2025 academic year. I used this analysis for an Externship program to gain and adapt my skills in data analysis performance.

My research question: Are higher levels of current financial stress, food insecurity and housing instability associated with increased depression and anxiety among U.S college students?

HMS Survey Data Research Report 2024-25

Variant Research Question: "To what extent do specific basic needs insecurities (food vs. housing) independently predict the likelihood of a depression or anxiety diagnosis among college students?"
 
Original Research Question: Are higher levels of current financial stress, food insecurity and housing instability associated with increased depression and anxiety among U.S college students?

Research Report: The Hidden Weight on Student Mental Health
An Analysis of Financial Stress and Mental Health Outcomes among U.S. College Students
1. Title & Abstract
Title: Financial Insecurity and Mental Health: A Statistical Analysis of 69,842 U.S. College Students.
Abstract: A brief summary (approx. 200 words) of the study. "This study analyzes the Healthy Minds Study (HMS) dataset, which consists of 69,842 responses from the 2024-2025 national student survey. The dataset includes 9 variables relevant to this analysis, such as financial stress, food and housing insecurity, age, and mental health indicators (Depression and Anxiety). Data cleaning involved handling missing values to ensure a robust sample and standardizing categorical variables, particularly gender identity. Our analysis utilized descriptive statistics (EDA), correlation analysis, and logistic regression to identify significant financial predictors of depression and anxiety among U.S. college students.", the focus on food and housing insecurity, and the discovery that these factors increase the odds of depression and anxiety by nearly 40%.
2. Introduction
Background: Overview of the rising cost of higher education and the modern "basic needs" crisis (food and housing).
Framework: Brief explanation of the public health model used: Demographics → Health Behaviors → Risk Factors.
3. Data & Methodology
Data Cleaning: How the dataset was prepared.
Handling missing values (dropping NaNs to ensure model integrity).
Defining binary outcomes for mental health (dep_any, anx_any).
Standardizing demographic variables (gender_clean).
Statistical Methods:
Exploratory Data Analysis (EDA): Used to identify prevalence and initial trends.
Correlation Matrix: Used to assess comorbidity (overlap) between anxiety and depression.
Logistic Regression: The primary tool used to calculate Odds Ratios, allowing us to see the independent impact of food vs. housing insecurity.
4. Key Findings & Visualizations
The Baseline Problem (Prevalence): * Finding: 36% of the sample (n=25,133) reported depression; 33% (n=22,999) reported anxiety.
Visualization: [Figure 1: Overall Prevalence with Counts]

The Risk Gradient:
Finding: Mental health risk follows a "staircase" pattern—as financial worry increases, so does the rate of illness.
Visualization: [Figure 2: Risk Gradients for Food and Housing]

The Statistical Evidence (Logistic Regression):
Finding: Housing insecurity (OR 1.39) and Food insecurity (OR 1.36) are both statistically significant predictors.
The Red Dashed Line (OR = 1.0): This is the baseline.
If a bar is at 1.0, that variable has no effect on the outcome.
If a bar is greater than 1.0, it increases the risk.
If a bar is less than 1.0, it decreases the risk.
The gender_clean bar: * In this analysis, gender_clean was likely coded as a binary (typically 0=Male, 1=Female).
If the gender_clean bar is at 1.5, for example, it means that female students in this sample are 1.5 times (or 50%) more likely to report a depression/anxiety diagnosis than male students, even when their age and financial situation are exactly the same.
In mental health research, gender is often a significant predictor because female students traditionally report higher rates of diagnosed depression and anxiety than male students.
Housing vs. Food: Since both are above 1.0, both are "risk factors." The longer the bar, the stronger the predictor.
Visualization: [Figure 3: Odds Ratio Forest Plot]

The Cumulative Burden:
Finding: Students facing both food and housing insecurity are at the highest risk, demonstrating a "Double Jeopardy" effect.
Visualization: [Figure 4: Cumulative Impact Bar Chart]

5. Conclusion & Recommendations
Summary: Final answer to the research question—confirming a strong, independent association between basic needs insecurity and mental health crisis.
Actionable Recommendations:
Prioritize Housing: Since housing instability showed a slightly higher risk factor (39% increased odds), universities should prioritize emergency housing vouchers.
Screening for Basic Needs: Mental health clinics should screen students for food/housing insecurity as part of their intake process.
Potential Applications: How TruBridge or university administrators can use this data to allocate resources more effectively to the most "at-risk" students.
