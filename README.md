Institution Graduation Rate Analysis
==============================

Overview
-----------------------------

This project aims to provide insights into the admissions test requirements and graduation rates of Chicago State University in comparison to other 4-year institutions within the American education system. The analysis involves merging data from the Integrated Postsecondary Education Data System and Wikipedia to develop a tool capable of explaining 64% of the variation in graduation rates.

Data Wrangling
-----------------------------

Merged datasets from the 2015/2016 to 2018/2019 academic years, resulting in a dataset with 1187 rows and 11 columns. Geographic and demographic data were added, requiring dimensionality reduction to 11 features.

Exploratory Data Analysis
-----------------------------

The exploration began with an examination of Chicago State University's standing among institutions in Illinois. Various visualizations, including skewness, a correlation heat map, and Seaborn Jointplots, were employed to understand the relationships between different variables.

![Distribution of Features](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/distributions.png)

![Heatmap](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/heatmap.png)

![Heatmap](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/corr_act_grad.png)

Pre-Processing and Modeling
-----------------------------

The modeling phase involved creating dummy variables, splitting the data into training and test sets (70:30 split), and evaluating five regression models. The top-performing models were identified as multiple linear regression and random forest, both explaining 64% of the variation in graduation rates. Further, hyperparameter tuning was conducted to enhance the performance of the random forest model.

Conclusion
-----------------------------

The multiple linear regression model emerged as the most effective in predicting graduation rates. Notably, the dummy variable 'WY' exhibited a significant influence on graduation rates.

![Heatmap](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/FeatureImportance.png)

Further Research
-----------------------------

1. Analyze Institutions in Wyoming (WY): A deeper investigation into institutions in Wyoming is warranted to understand the peculiar impact of this variable on graduation rates.
2. Introduce a Public/Private Institution Variable: Consider incorporating a variable indicating whether an institution is public or private to assess its potential impact on data distribution. Public and private institutions may have distinct approaches to dealing with underperforming students, influencing student success outcomes.
3. Address Data Gaps on Transfer Students: The absence of data on transfer students is acknowledged. Further research should explore the impact of transfer students on graduation rates, addressing issues such as students transferring in as sophomores and the potential bias introduced by their inclusion in the data.

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
