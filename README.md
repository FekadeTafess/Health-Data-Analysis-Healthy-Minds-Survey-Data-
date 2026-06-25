# Health-Data-Analysis-Healthy-Minds-Survey-Data-
I conducted an analysis of the Healthy Minds Survey data from the University of Michigan (and other U.S. universities), examining the correlation between financial stressors and mental health among college students during the 2024–2025 academic year. I used this analysis for an Externship program to gain and adapt my skills in data analysis performance.

My research question: Are higher levels of current financial stress, food insecurity and housing instability associated with increased depression and anxiety among U.S college students?

HMS Survey Data Research Report 2024-25

Variant Research Question: "To what extent do specific basic needs insecurities (food vs. housing) independently predict the likelihood of a depression or anxiety diagnosis among college students?"
 
Original Research Question: Are higher levels of current financial stress, food insecurity and housing instability associated with increased depression and anxiety among U.S college students?

The Economics of Mental Health: A Statistical AnalysisAssessing the Impact of Basic Needs Insecurity on U.S. College Students

📌 Executive SummaryThis research utilizes data from the Healthy Minds Study (HMS) 2024-2025 ($N=69,842$) to investigate how Social Determinants of Health (SDoH)—specifically food, housing, and financial insecurity—function as independent predictors of depression and anxiety.The core finding is clear: We cannot expect students to thrive in the classroom if they are struggling to survive outside of it. The data moves the conversation from students being "broke" to identifying systemic instability as a critical clinical risk factor.

🔬 Methodology & DataDataset: Healthy Minds Study (HMS) 2024-2025.Sample Size: $N = 69,842$.

Step 1: Data Acquisition & Target PopulationThe Dataset: The study utilized the Healthy Minds Study (HMS) 2024–2025 public dataset.Sample Size: The final cleaned dataset yielded an $N = 69,842$ respondent pool.Target Population: Undergraduate and graduate students across multiple higher education institutions, capturing a diverse layout of ages, financial backgrounds, and genders as visualized in demographic_economic_visual_3.png.
Analytical Approach:Data Cleaning: Standardized gender variables and addressed missingness (under 5%). Statistical Modeling: Logistic Regression was employed to calculate Odds Ratios (OR), isolating the "risk multiplier" effect of specific insecurities.

Step 2: Feature Selection & Variable Mapping
Variables were selected based on a framework treating economic constraints as Social Determinants of Health (SDoH). The core variables extracted included:

Dependent Variables (Outcomes): Clinical screening indicators for depression (dep_any, deprawsc, dep_maj) and anxiety (anx_any, anx_score).

Independent Variables (Predictors): Indicators of economic stress, specifically current financial strain (fincur), food worry (food_worry), and housing worry (housing_worry).

Control Variables (Covariates): Sociodemographic factors including age (age), financial past (finpast), Pell Grant status (pellgrant), and gender (gender_male, gender_female) to isolate confounding effects.

Step 3: Data Cleaning & Preprocessing
Handling Missingness: Missing data across the core research variables was evaluated using missingness matrices (such as the missingno tracking protocol) to ensure data completeness. Missing values were minimal (under 5%) and handled via listwise deletion to maintain model integrity.

Feature Engineering: Categorical indicators for gender were harmonized into binary flags (gender_male, gender_female), and ordinal scales for basic needs worries were standardized to accurately reflect risk gradients (low to high stress).

Step 4: Exploratory Data Analysis (EDA)
Prevalence Profiling: Descriptive statistics established the baseline clinical landscape, identifying that 36% of the population screened positive for depression and 33% for anxiety.

Trend Analysis: Cross-tabulations were performed to map the "staircase effect"—visualizing how incremental increases in food or housing worry directly mapped to higher percentages of mental health distress.

Step 5: Statistical Modeling via Logistic RegressionBecause the primary outcomes (e.g., screening positive for depression or anxiety) are binary, Logistic Regression was selected as the core mathematical framework.The model estimates the probability ($P$) of a student experiencing clinical distress using the log-odds formula:$$\ln\left(\frac{P}{1 - P}\right) = \beta_0 + \beta_1(\text{Housing Worry}) + \beta_2(\text{Food Worry}) + \beta_3(\text{Financial Stress}) + \gamma(\mathbf{X})$$Where $\mathbf{X}$ represents the vector of control covariates (age, gender, etc.), and $\beta$ represents the log-odds coefficients.

Step 6: Risk Quantification (Odds Ratios)To make the findings clinically interpretable, the log-odds coefficients ($\beta$) were converted into Odds Ratios (OR) by taking their exponential ($e^\beta$):This step successfully isolated the independent "risk multiplier" effect of each basic need.For instance, it allowed us to prove that housing instability independently increases the odds of clinical depression by 39%, and food insecurity by 36%, even when students share identical age, gender, and demographic backgrounds.

Step 7: Interaction & Cumulative Impact Evaluation
The "Double Jeopardy" Check: Finally, the analysis looked beyond individual predictors to examine cumulative burden.

By evaluating the overlap of multiple stressors, the methodology successfully demonstrated a compounding, synergistic effect—proving that students experiencing both food and housing insecurity face an exponentially higher risk profile than those dealing with just one.

📊 Key Findings 

1. The Risk Multipliers The study identified three primary predictors that significantly increase the likelihood of mental health struggles:Financial Stress: Current financial strain serves as a persistent baseline for anxiety.Food Insecurity: Lack of reliable access to nutritious food correlates strongly with depressive symptoms.Housing Instability: This was found to be one of the most volatile predictors, often acting as a "tipping point" for acute mental health crises.

2. Statistical Significance By using Odds Ratios, the research demonstrates that basic needs insecurity is not just a correlate but an independent predictor. This means that even when controlling for other demographic factors, these economic pressures significantly raise the probability of a clinical diagnosis.

🚀 Implications & ROI The research suggests a transition in how higher education and healthcare approach student success:Clinical Integration: SDoH screening should be standard in campus health clinics.Targeted Investment: Programs like "Housing-First" or food pantries are not just social services; they are mental health interventions with a measurable Return on Investment (ROI) regarding student retention and wellbeing.

⚠️ Limitations Cross-Sectional Design: The data shows correlation and association; it cannot definitively establish a temporal sequence of causation.Self-Report Bias: Findings rely on student self-reporting, which may be influenced by social desirability or recall biases.

🛠️ How to Navigate This Repo/data: Contains descriptions of the HMS variables used (note: raw data may be restricted based on HMS licensing)./notebooks: Jupyter notebooks showing the Logistic Regression models and data cleaning steps./visualizations: Exported plots of Odds Ratios and prevalence patterns.
