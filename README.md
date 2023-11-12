# Split-Data

Travel Insurance Dataset Analysis and Predictive Modeling Report

1. Introduction

Travel insurance plays a crucial role in mitigating risks associated with unforeseen circumstances during trips. This report aims to analyze a comprehensive travel insurance dataset, perform exploratory data analysis (EDA), feature engineering, and develop a predictive model for claim prediction.

2. Data Overview:

The dataset comprises 63,326 entries with 11 columns, including agency details, product information, duration, destination, net sales, commission, gender, and age. The data types include float64, int64, and object. A critical observation is the presence of missing values in the "Gender" column.

3. Data Cleaning

Handling missing values is essential for a robust analysis. In this case, the "Gender" column was addressed by dropping the column.

4. Exploratory Data Analysis (EDA):

4.1 Categorical Data Exploration:

Understanding categorical variables is crucial. The unique elements of categorical columns, including "Agency," "Agency Type," "Distribution Channel," "Product Name," "Destination," and "Claim," were explored. This exploration lays the foundation for subsequent analyses.

4.2 Visualization:

Visualization aids in understanding patterns and trends. Visualized aspects such as popular destinations, age distribution, agency performance, and preferred insurance plans using interactive pie charts, histograms, and bar plots.

Results: The pie chart showcasing popular destinations revealed that certain destinations attract a significantly higher number of insured individuals. The age distribution histogram indicated a wide range of ages, with a concentration in the mid-30s. Bar plots depicted the distribution of insured individuals among different agencies and product plans.

Popular Destinations Pie Chart

![image](https://github.com/sesan-81/Split-Data/assets/104377031/485a1f7b-9854-46a0-9021-1159c4a7dbab)

 
Age Distribution Histogram

 ![image](https://github.com/sesan-81/Split-Data/assets/104377031/6e12eeed-0b8f-498c-a21b-ed7b7ac77fa3)


Agency Distribution Bar Plot
 

![image](https://github.com/sesan-81/Split-Data/assets/104377031/62a32fb7-3270-47ec-a489-dfab04f381ff)


5. Feature Engineering:

5.1 Grouping and Aggregation:

Insights into popular destinations, agency performance, and preferred insurance plans were obtained through grouping and aggregation. This step is crucial for deriving meaningful features for model training.

5.2 Label Encoding:

Categorical data was encoded using label encoding to convert string labels into numeric format, facilitating model training.

Results: Grouping by destination unveiled top destinations, and label encoding converted categorical variables into a format suitable for model training.

6. Correlation Analysis:

Correlation analysis was conducted to identify relationships between different features. A heatmap was used for visual representation.

Results: The heatmap revealed correlations between certain features, guiding further exploration into potential multicollinearity.

![image](https://github.com/sesan-81/Split-Data/assets/104377031/6e5f5048-0c68-4ad9-bfe6-940805084a63)



Correlation Heatmap 


7. Data Preprocessing:

7.1 Handling Imbalanced Classes:

Imbalanced classes can impact model performance. Synthetic Minority Over-sampling Technique (SMOTE) was applied to address this issue, resulting in a more balanced distribution.

7.2 Scaling Features:

Min-Max scaling was applied to ensure uniformity and prevent the dominance of specific features during model training.

Results: SMOTE improved the distribution of classes, and feature scaling enhanced the model's performance.

8. Model Training:

8.1 Random Forest Classifier:

A Random Forest Classifier was trained on the preprocessed data to predict the "Claim" status, considering the balanced dataset.


9. Model Evaluation:

9.1 Metrics Calculation:

The model was evaluated using key metrics, including accuracy, recall, precision, and F1-score, providing insights into its performance.
Results: The model demonstrated promising performance during training, with an accuracy of 0.97, recall of 0.98, precision of 0.96, and F1-score of 0.97.

9.2 Confusion Matrix:

A confusion matrix was visualized to understand the model's ability to classify instances correctly.

Results: The confusion matrix indicated 15103 true positives, 15241 true negatives, 279 false positives, and 577 false negatives.

Confusion Matrix
 
![image](https://github.com/sesan-81/Split-Data/assets/104377031/5a413b45-af8d-498e-bb48-c02ebf6d701c)


10. Hyperparameter Tuning (Optional):

10.1 Grid Search:

Hyperparameter tuning using Grid Search was explored to find the optimal set of hyperparameters for the Random Forest model.

Results: The best hyperparameters were 'max_depth': None, 'min_samples_leaf': 1, 'min_samples_split': 5, 'n_estimators': 150 resulting in an almost improved model.


11. Visualization :

11.1 ROC Curve:


![image](https://github.com/sesan-81/Split-Data/assets/104377031/857453bb-9686-42ec-8c89-2a2ec0b0fb07)


The Receiver Operating Characteristic (ROC) curve was plotted to visualize the trade-off between the true positive rate and false positive rate.

11.2 Precision-Recall Curve:

The Precision-Recall curve was visualized to understand the precision-recall trade-off.

Results: The ROC curve demonstrated AUC_score = 0.99, and the Precision-Recall curve depicted.

ROC Curve
 
Precision-Recall Curve
 
![image](https://github.com/sesan-81/Split-Data/assets/104377031/8daac9b0-5bb9-4623-9729-a26ff806f870)


12. Conclusion

In conclusion, the analysis provided a detailed exploration of the travel insurance dataset, encompassing data cleaning, EDA, feature engineering, and model training. The Random Forest model showcased promising results, with potential for further improvement through hyperparameter tuning. The comprehensive evaluation and visualization steps contribute to a robust understanding of the dataset and model performance.
