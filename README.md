Institution Graduation Rate Analysis
==============================

Overview
-----------------------------

This project focuses on College Scorecard data provided by the U.S. Department of Education. The purpose it to explore student data to find useful insights on increasing graduation rates. In particular, I'd like to see if there is statistical significance between ACT/SAT scores at admittance and graduation rate after 4 years of enrollment.

Data Wrangling
-----------------------------

Merged datasets from the 2015/2016 to 2018/2019 academic years, resulting in a dataset with 1187 rows and 11 columns. Geographic and demographic data were added, requiring dimensionality reduction to 11 features.

Exploratory Data Analysis
-----------------------------

Explored Chicago State University's position among institutions in Illinois and identified correlations, visualized through skewness, correlation heat map, and Seaborn Jointplots.

![Heatmap](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/heatmap.png)

Pre-Processing and Modeling
-----------------------------

Generated dummy variables, split data 70:30, and tested five regression models. Multiple linear regression and random forest performed best, with a 64% variation explanation. Hyperparameter tuning improved the random forest model slightly.

Conclusion
-----------------------------

Multiple linear regression remains the top-performing model. Dummy variable 'WY' significantly impacts graduation rate. 

Further Research
-----------------------------

1. Analyze institutions in Wyoming (WY) to understand its impact.
2. Introduce a public/private institution variable to explore its effect on data distribution.
3. Address the absence of data on transfer students, as their presence may impact graduation rates.

Project Organization
------------

    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── interim        <- Intermediate data that has been transformed.
    │   └── processed      <- The final, canonical data sets for modeling.
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    └── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
                              generated with `pip freeze > requirements.txt`
