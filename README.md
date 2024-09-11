# IS41070_Final
Capstone project for the Machine Learning Foundation course (IS41070) at the UCD iSchool, as part of my MSc in Information Systems program.

### Project Overview

Note: CSV file used - '50.csv'.

This project, titled **"News Classification Using Machine Learning and Deep Learning Models,"** is the final project of the Machine Learning Foundation (IS41070) course at UCD iSchool for my MSc Information Systems. The objective of the project is to classify news articles into appropriate categories using machine learning and deep learning models, addressing challenges like class imbalance and optimizing for key metrics like the F1-score.

The workflow is divided into three main tasks:

### Task 1: Data Understanding and Visualization

**Data Exploration and Cleaning:**  
In this initial phase, we began by exploring the dataset to identify potential issues such as missing values, incorrect data formats, and unnecessary features. Missing values were handled by imputing with appropriate statistical measures (mean, median, or mode), and irrelevant columns were dropped to streamline the data for analysis.

**Text Preprocessing:**  
Text data, including features like headlines, authors, categories, and short descriptions, were cleaned and preprocessed. This involved converting text to lowercase, removing punctuation, filtering out stopwords using NLTK, and stemming words to their root forms. These steps helped standardize the textual data, making it suitable for further analysis.

**Common Terms Analysis:**  
To gain insights into the most frequent terms in each feature, we performed word frequency analysis. This allowed us to identify common patterns and keywords within the dataset, which could be significant for the classification models.

**Domain Extraction and Visualization:**  
From the URLs in the dataset, domains were extracted to standardize the sources of the news articles. Various visualizations, including word clouds and bar plots, were created to depict the most common terms across different features. A time series plot was also generated to analyze the distribution of articles over time, providing a temporal view of the data.

### Task 2: Data Preparation and Modeling

**Feature Engineering and Encoding:**  
The date column was engineered into day, month, and year components, enhancing the data's predictive power by breaking down the temporal element into more granular features. Text columns were vectorized using techniques like TF-IDF, transforming them into numerical format suitable for model training. The target feature, categories, was encoded into numeric form to facilitate classification.

**Binary Classification Models:**  
For the initial classification task, we implemented Logistic Regression and Decision Tree Classifiers. These models were trained and evaluated to determine their effectiveness in categorizing the news articles. The Logistic Regression model achieved a validation accuracy of 88.28%, while the Decision Tree Classifier performed slightly better with a validation accuracy of 90.94%. Classification reports and confusion matrices highlighted the strengths and weaknesses of each model, particularly in handling class imbalance.

**Deep Learning Classifier:**  
A deep learning model was developed using Keras Sequential API with layers including Dense, Dropout, and activation functions like ReLU and Softmax. The deep learning model aimed to capture complex patterns within the data that traditional models might miss. Despite a decent performance with an accuracy of 74.84%, the model's ability to generalize across classes needed further tuning due to observed class imbalance.

### Task 3: Evaluation and Optimization

**Primary Metric Selection:**  
The F1-score was chosen as the primary evaluation metric, especially due to the class imbalance in the dataset. This metric considers both precision and recall, providing a balanced measure of the model's performance across different classes.

**Model Optimization and Error Analysis:**  
To improve the models, techniques like class weighting and SMOTE (Synthetic Minority Over-sampling Technique) were applied. These approaches helped address class imbalance, significantly enhancing the model's performance, particularly for the minority class (class 1).

**Cross-Validation and Final Model Selection:**  
Cross-validation was conducted by merging the training and validation sets, ensuring robust performance across different data subsets. The Decision Tree Classifier with class weighting emerged as the best-performing model, demonstrating consistent F1-scores across folds and a strong performance on the test set.

### Conclusion

This project demonstrates a comprehensive approach to news article classification using various machine learning and deep learning models. By addressing class imbalance and focusing on key evaluation metrics, the final model provides a reliable solution for categorizing news content, making it applicable for real-world scenarios.
