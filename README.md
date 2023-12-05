# Predict-Password-Strength
The project focuses on analyzing and classifying passwords based on their strength using various data analysis and machine learning techniques. Here's a breakdown of the key steps and findings:

# Data Retrieval and Cleaning:
- Data was retrieved from an SQLite database containing user information, specifically the "password" column.
- No duplicate or missing values were found in the dataset.
- The dataset was cleaned by dropping the index column.
# Semantic Analysis:
- Semantic analysis was performed to understand the characteristics of passwords.
- The analysis included identifying passwords with numerical, uppercase, alphanumeric, title case, special characters, and alphabetic-only characters.
# Feature Engineering:
Several new features were engineered to enhance the dataset for machine learning:
- Password length
- Frequency of lowercase characters
- Frequency of uppercase characters
- Frequency of numerical characters
- Frequency of special characters
# Data Analysis:
- Statistical analysis was conducted on the engineered features grouped by password strength.
- Box plots were generated to visualize the distribution of features across different password strengths.
# Interesting Feature Selection:
- Violin plots and distribution plots were used to visualize the distribution of interesting features, such as password length and frequency of lowercase characters, across different password strengths.
- Password length and lowercase character frequency were identified as interesting features with minimal overlap among different strength categories.
# TF-IDF Transformation:
- The TF-IDF (Term Frequency-Inverse Document Frequency) technique was applied to convert password strings into numerical vectors for machine learning.
- The feature matrix was created using the TfidfVectorizer from scikit-learn.
# Machine Learning:
- A logistic regression model was chosen for classification, considering the multinomial nature of the problem.
- The dataset was split into training and testing sets.
- The logistic regression model was trained on the training set and evaluated on the testing set.
# Model Evaluation:
- The accuracy score and classification report provide insights into the model's ability to classify passwords into different strength categories.
- The precision, recall, and F1-score provide insights into the model's performance for each class.
- Class 1 has the highest precision, recall, and F1-score, indicating good performance for this class.
- Class 0 has lower precision and recall, suggesting challenges in correctly identifying instances of this class.
- Class 2 shows a relatively balanced performance with decent precision, recall, and F1-score.
- Overall accuracy 81%
# Stratified k-fold Cross-Validation
- The cross-validation scores indicate the accuracy of the model across different folds
- In this case, the mean accuracy is approximately 81.57%, suggesting that the model performs consistently well across different subsets of the data.
# Key Findings:
- The analysis identified interesting features, such as password length and lowercase character frequency, that contribute significantly to password strength.
- The logistic regression model achieved a certain level of accuracy(81%) in classifying passwords into different strength categories.
