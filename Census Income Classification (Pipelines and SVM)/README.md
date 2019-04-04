# Census Data Classification (Support Vector Machine, Random Forest and Logistic Regression with Pipelines)

## Data
The dataset consists of census income data and is used to classify whether the adult earns up to or more than fifty thousand dollars per year. It is a binary classification problem with a mix of 14 (total) integer and categorical attributes.
<br>
<br>
The dataset is from http://mlr.cs.umass.edu/ml/datasets/Census+Income
<br>
<br>
## Exploratory Data Analysis
Several variables captured similar information and hence were dropped from the final feature set. There was also quite a number of fields that were unfilled. The number of adults surveyed who earning more than fifty thousand dollars per year (higher salaries) was about a quarter of all participants while the remainder earned up to fifty thousand dollars per year (lower salaries).
<br>
<br>
Observations from the initial analysis:
<ul>For higher salaries, the age of participants is normally distributed but for lower salaries, the age of participants is positively skewed.  </ul>
<ul>Increases in years of education is associated with increases in the ratio of participants from higher to lower paying salaries</ul>
<ul>Executive, managerial jobs and specialty professions are associated with a greater participants from higher to lower paying salaries.</ul>
<ul>Increases in hours per week is associated with a rise in ratio of participants from higher to lower paying salaries up to 50K. </ul>

## Models
Logistic Regression, Support Vector Machine and Random Forest models were used together with pipelines to prevent data leakage during cross validation.

## Conclusion
The Random Forest classifier performed the best, with an F1 macro score of about 0.798. Since about split of participants was about 3:1, the baseline score for accuracy was already rather high and an F1-score might be a better representation of the performance of the models since it would take recall into account was well. With that said, the model did improve the baseline accuracy of 0.763 to 0.866. From the Random Forest model, the features that contributed most to distinguishing between the two salary bands were capital gain, marrying a civilian spouse, years of education and age.
