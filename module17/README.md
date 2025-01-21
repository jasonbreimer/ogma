https://github.com/jasonbreimer/ogma/tree/main/module17

Goal:
The objective of this project is to compare the performance of various classifiers, namely K-Nearest Neighbors, Logistic Regression, Decision Trees, and Support Vector Machines, using a dataset related to marketing bank products over the telephone. The dataset encompasses 17 campaigns conducted between May 2008 and November 2010, totaling 79,354 contacts.

Data Preparation and Cleaning

Round 1: Data Cleaning

Filtering poutcome Values: Only included 'failure' and 'success'.
Removing sex Column: As it had minimal importance. **This had already been done but noted from White Paper.

Additional Cleaning Steps:
Filtered out rows with zero age.
Removed rows with 'unknown' values. **Post-Work excecise attempts simple impute
Removed periods from education values to avoid potential issues.

Round 2: Data Preparation

Handling Unseen Values in education:
Introduced stratification on education during the train-test split to ensure balanced representation:

Performance Improvements Noted:
Accuracy: Improved from 83.29% to 85.42%.
Mean Squared Error (MSE): Decreased from 0.1671 to 0.1458.
R-squared (R²): Improved from 0.1924 to 0.2432.
Class 0: Slight improvements in precision, recall, and F1-score.
Class 1: Slight decrease in recall, but overall performance remained similar.

Handling 'illiterate' Value:
As the 'illiterate' value had only one sample, it was dropped to avoid issues with stratification.

Overall Conclusion
Every model evaluated, including their hyper-tuned versions, outperforms the baseline dummy classifier significantly in terms of accuracy and error metrics. The hyper-tuned versions of K-Nearest Neighbors and Decision Tree models, in particular, show improved performance and stability. Logistic Regression and SVM also provide strong results, making them reliable choices depending on the specific application requirements. This demonstrates the effectiveness of these models over a simple dummy classifier in predicting outcomes with greater accuracy and reliability.

Logistic Regression and SVM show strong performance with relatively high test accuracy and low MSE. However, hyper-tuning KNN and Decision Tree models also yield improved residual plots and better generalization, highlighting the importance of model optimization. Each model has its trade-offs between training time, accuracy, and complexity, allowing for flexibility depending on the specific application requirements.

An interesting follow up exercise would be to try and impute unknown values. See the Post-Work section in the Jupyter Notebook.

Post-Work Summary:
The model demonstrated strong performance metrics across both training and testing sets. It achieved a training accuracy of 91.88% and a testing accuracy of 91.25%. Additionally, the training process, although computationally intensive, took approximately 7 hours.

In terms of prediction accuracy and error metrics, the mean squared error (MSE) was 0.0875, while the R-squared value stood at 0.1041. These values indicate a reasonable level of prediction accuracy, though with some room for improvement in explaining the variance in the data.

The classification report highlighted a high overall accuracy of 91.25%, with class 0 (the majority class) showing excellent precision, recall, and F1-score of 0.93, 0.97, and 0.95, respectively. Class 1, although underrepresented, managed to achieve a precision of 0.66, recall of 0.41, and F1-score of 0.51. The macro average scores, which consider the balance between the classes, were 0.80 for precision, 0.69 for recall, and 0.73 for F1-score. Weighted averages, which account for the support of each class, were similarly strong, reinforcing the model's balanced performance. 

Post-work exercise attempting SimpleImputer on unknown values shows slight scoring improvements but significant training time of 7 hours. Other classifiers without Impute showed similer scoring. Using SimpleImputer might not be worth the tradeoff of significant training time for slight scoring improvements.


| Model                     | Train Time  | Train Accuracy | Test Accuracy | MSE    | R2     |
|---------------------------|-------------|----------------|---------------|--------|--------|
| Logistic Regression       | 0.045959    | 0.841935       | 0.845328      | 0.1547 | 0.2315 |
| K-Nearest Neighbors       | 0.026209    | 0.871237       | 0.813104      | 0.1869 | 0.0715 |
| Decision Tree             | 0.083535    | 1.000000       | 0.794844      | 0.2052 | -0.0193|
| Support Vector Machine    | 2.394350    | 0.877151       | 0.837809      | 0.1622 | 0.1942 |
| K-Nearest Neighbors (17)  | 1.159600    | 0.834700       | 0.822800      | 0.1772 | 0.1195 |
| Decision Tree (10)        | 5.787100    | 0.941900       | 0.809900      | 0.1901 | 0.0554 |
| Baseline Dummy            | 0.001000    | 0.723900       | 0.720700      | 0.2793 | -0.3875|
| Simple Imputer            | 25397.3509  | 0.918800       | 0.912500      | 0.0875 | 0.1041 |
