
# Youth Mortality Analysis and Prediction

## Live Project Website

View the deployed interactive project website here:

https://ecelule.github.io/dsa210project/

**What is this project about?**

In this project, I tried to understand a simple but important question:

Why do some regions have higher youth mortality (ages 5–24) than others?

And can we predict it using data?

To answer this, I combined:

* data analysis
* statistical modeling
* machine learning

**Data Used**

I merged multiple datasets:

* Youth mortality rates (UNICEF)
* Human Development Index (HDI)
* Health & education spending
* Regional classifications

Then I cleaned and combined them into one dataset at region-year level.

⸻

**Step 1 — Exploring the Data (EDA)**

First, I looked at basic relationships.

🤝🏻Key findings:

* HDI, health spending, and education spending are strongly positively correlated
* All of them are negatively correlated with mortality

In simple terms:
More development → lower youth mortality

But there is a catch (important!!!):
These variables are also highly correlated with each other

⸻

**Step 2 — Understanding + Hypothesis Testing**

Before jumping into ML, I used "Hypothesis Testing" to understand the relationships more clearly.

🤝🏻Key results:

* Model explains ~78% of variation (R² ≈ 0.78) ✅
* Health spending → strong negative & significant effect
* Education spending → positive but tricky (multicollinearity)
* HDI → not significant when other variables are included
* Regions still matter a lot

🪻 Important insight:

Even though development variables matter,
they are so correlated that it’s hard to isolate their individual effects.

⸻

**Step 3 — Machine Learning (Prediction)**

Then I switched to prediction:

🤝🏻Models used:

* Linear Regression
* KNN Regression
* Baseline (mean)

🤝🏻Results:

* KNN performed best
* Lowest RMSE
* Highest R²

Why?

Because KNN can capture non-linear patterns, unlike linear regression.

⸻

**Step 4 — Time-Based Analysis**

I also tested whether models can predict future mortality trends.

Approach:

* Train on past years
* Test on recent years

Findings:

* Model captures general trend
* But struggles with year-to-year fluctuations

🤝🏻Predicting levels is easier than predicting changes.



🥳*Key Takeaways*

* Development strongly relates to mortality
* Health spending is the most reliable predictor
* Multicollinearity is a real issue
* KNN outperforms linear models in prediction
* Predicting change over time is much harder than predicting levels

⸻

😔*Limitations*

* High correlation between variables (multicollinearity)
* Regional averages hide country-level differences
* Limited time depth for forecasting

⸻


🛠️ Tools Used

* Python
* Pandas, NumPy
* Scikit-learn
* Statsmodels
* Matplotlib & Seaborn

⸻

🥳*Final Thought*

This project shows that:

🤝🏻 Data can explain why things happen

🤝🏻 Machine learning can help predict what will happen

And combining both gives a much stronger analysis.


## How to Run

1. Clone the repository
2. Install dependencies:

pip install -r requirements.txt

3. Run the notebook:
youth_mortality_analysis_ML.ipynb
