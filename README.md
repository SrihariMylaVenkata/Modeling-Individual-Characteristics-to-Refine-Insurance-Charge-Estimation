# Modeling-Individual-Characteristics-to-Refine-Insurance-Charge-Estimation

Overview
This project focused on analyzing and modeling health insurance charges using demographic and behavioral features. Working with a real-world dataset containing variables such as age, sex, BMI, smoking status, region, and number of children, the goal was to understand key cost drivers and build interpretable models to predict medical charges.

The project was conducted in R, and involved data cleaning, EDA, correlation analysis, statistical testing, and both regression and classification modeling. This end-to-end pipeline demonstrates my ability to extract insights and build predictive tools in the healthcare domain.

Data Source
Dataset: insurance.csv with 1,338 records and 7 variables

Columns: age, sex, bmi, children, smoker, region, and charges (target variable)

Key Steps and Insights
1. Data Exploration and Cleaning
Verified data dimensions and structure

Confirmed zero missing values

Converted categorical features into factors and used one-hot encoding for modeling

Identified variable types and summary statistics

2. Exploratory Data Analysis (EDA)
Histograms and boxplots revealed a right-skewed distribution in charges

Scatter plots showed a positive correlation between age, BMI, and charges

Smokers had significantly higher charges than non-smokers

Boxplots for region, sex, and children offered insight into variability

3. Correlation Matrix
Computed Spearman correlation on the numerically encoded dataset

Found strong positive correlation between charges and:

age (0.53)

smokeryes (0.66)

Weak or no correlation from variables like region or sex

4. Statistical Testing
T-tests revealed significant differences in charges based on high vs. low values for age, BMI, and children

Chi-square tests showed that smoking status had a statistically significant impact on charges (p < 0.001), while sex and region did not

Shapiro-Wilk test confirmed that charges is not normally distributed

Kruskal-Wallis tests supported the above findings for non-normal variables

Modeling Approaches
Linear Regression
Simple Linear Regression using age only yielded an R² of 0.089

Multiple Linear Regression using all features improved R² to 0.78

Key predictors: age, BMI, smoker, and region

smoker alone added over $23,000 to predicted charges (p < 0.001)

Logistic Regression
Converted charges into a binary variable (above/below median)

Logistic regression identified:

age and BMI as significant predictors (p < 0.05)

region (southeast and southwest) had negative influence

smoker produced a coefficient with high standard error—likely due to perfect separation

Model Evaluation
Compared R² values of simple vs. multiple linear models in a bar plot

Residual plots showed random dispersion, supporting model assumptions

Logistic regression achieved good separation but was affected by extreme smoking-related values

Tools & Techniques Used
R packages: dplyr, Hmisc, corrplot

Techniques: One-hot encoding, Spearman correlation, Q-Q plots, boxplots, chi-square and Kruskal-Wallis tests

Models: Linear regression (simple/multiple), logistic regression

Visualizations: Residual plots, bar plots, correlation heatmap

Key Takeaways
Smoking status is the most influential variable affecting insurance charges

Age and BMI also contribute significantly to prediction accuracy

Linear regression provided solid model fit, while classification allowed for cost group stratification

Strong evidence that demographic and behavioral variables can be used to guide insurance pricing and risk assessment
