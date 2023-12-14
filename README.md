Institution Graduation Rate Analysis
==============================

Overview
-----------------------------

This project aims to provide insights into the admissions test requirements and graduation rates of Chicago State University in comparison to other 4-year institutions within the American education system. The analysis involves merging data from the Integrated Postsecondary Education Data System and Wikipedia to develop a tool capable of explaining 64% of the variation in graduation rates.

Data Wrangling
-----------------------------

Merged datasets from the 2015/2016 to 2018/2019 academic years, resulting in a dataset with 1187 rows and 11 columns. Geographic and demographic data were added, requiring dimensionality reduction to 11 features.  The distribution of acceptance rates, graduation rates, and total graduating students are shown below:

![Admission_rate](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/Admission_rate.png)

![Graduation Rate](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/graduationrate.png)

![Graduating Students](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/graduating_student_frequency.png)

Chicago State University has some concerning statistics within the distributions shown above.

Here are some additional statistics related to CSU:

- It appears as 39th in admissions selectivity of matriculating students for the 2015/2016 academic year.
1135th in average ACT 25th percentile score for the 2015/2016 academic year.
- The university ranks 1176th in graduation rate of bachelor degree earning students during the 2018/2019
academic year.
- 884th in terms of total bachelor degree earning students graduating during the 2018/2019
academic year.

Exploratory Data Analysis
-----------------------------

The exploration began with an examination of Chicago State University's standing among institutions in Illinois. Various visualizations, including skewness, a correlation heat map, and Seaborn Jointplots, were employed to understand the relationships between different variables.

![Distribution of Features](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/distributions.png)

Only the admission_rate distribution appears to be skew-left.

![Heatmap](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/heatmap.png)

Some notable positive strong and medium/strong correlations that appear include the
act_25th_percentile_score and graduation_rate features (0.76), and territory_or_state_area_sqmi
and territory_or_state_population features (0.62). The feature act_25th_percentile_score belongs
to both positive correlations mentioned. Some notable negative medium/strong correlations
include admission_rate and act_25th_percentile_score features (-0.45), and admission_rate and
graduation_rate features (-0.35). The feature admission_rate belongs to both negative
correlations mentioned.

![Heatmap](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/corr_act_grad.png)

The strongest positive correlation I found in the act_25th_percentile_score and graduation_rate Seaborn Jointplot seems
intuitive to me, but I wonder if it's a result from bias during the wrangling process by only
including institutions that are predominately bachelor's and graduate degree granting.

Pre-Processing and Modeling
-----------------------------

The modeling phase involved creating dummy variables, splitting the data into training and test sets (70:30 split), and evaluating five regression models. The top-performing models were identified as multiple linear regression and random forest.  The multiple linear regression model explained 64% of the variation in graduation rates with a MSE of .38, while random forest explained 62% of the variation of graduation rates with a MSE of .39. Further hyperparameter tuning on the random forest model slightly improved its prediction of changes to 62.2% MSE while worstened to .399.

Conclusion
-----------------------------

The multiple linear regression model emerged as the most effective in predicting graduation rates. Notably, the dummy variable 'WY' exhibited a significant influence on graduation rates.

![Feature Importance for Multiple Linear Regression](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/figures/FeatureImportance.png)

Further Research
-----------------------------

1. Analyze Institutions in Wyoming (WY): A deeper investigation into institutions in Wyoming is warranted to understand the peculiar impact of this variable on graduation rates.
2. Introduce a Public/Private Institution Variable: Consider incorporating a variable indicating whether an institution is public or private to assess its potential impact on data distribution. Public and private institutions may have distinct approaches to dealing with underperforming students, influencing student success outcomes.
3. Address Data Gaps on Transfer Students: The absence of data on transfer students is acknowledged. Further research should explore the impact of transfer students on graduation rates, addressing issues such as students transferring in as sophomores and the potential bias introduced by their inclusion in the data.

Project Writeup:
------------

[Final Project PDF](https://github.com/Mkreitman/Capstone-Two/blob/main/reports/Capstone_Final_Report.pdf)
