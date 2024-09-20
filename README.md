# Spam Email Classification using Logistic Regression

## Project Overview

This project demonstrates a machine learning-based solution for spam email classification using Logistic Regression. The goal is to predict whether an email is spam or not (ham) based on its content. The dataset used consists of 5,572 email samples, with labels indicating whether each email is spam or ham. The model is trained on features extracted from the email text using the TF-IDF (Term Frequency-Inverse Document Frequency) vectorization technique.

## Project Workflow

1. **Data Collection**: 
   The dataset, `mail_data.csv`, contains two columns: `Category` (spam or ham) and `Message` (email content). This data was loaded into a Pandas DataFrame for analysis.

2. **Data Preprocessing**:
   - Missing values were handled by replacing them with empty strings.
   - The email category was label-encoded: spam = 0, ham = 1.
   - The dataset was split into features (`Message`) and labels (`Category`).

3. **Data Splitting**:
   The data was split into training and test sets using an 80/20 ratio to ensure the model could be properly evaluated on unseen data.

4. **Feature Extraction**:
   The `TfidfVectorizer` from Scikit-learn was used to convert the text data into numerical feature vectors. This step transformed the email content into a format suitable for the Logistic Regression model.

5. **Model Training**:
   A Logistic Regression model was trained on the extracted TF-IDF features from the training set.

6. **Model Evaluation**:
   The model was evaluated based on its accuracy on both the training and test sets. The accuracy achieved was approximately 96.7% on the training data and 96.6% on the test data, indicating good performance.

7. **Predictive System**:
   A simple system was built to classify new email messages as either "Spam" or "Ham" based on the trained Logistic Regression model.

## Results

- **Training Data Accuracy**: 96.7%
- **Test Data Accuracy**: 96.6%

These results demonstrate the effectiveness of the Logistic Regression model in accurately classifying emails as spam or ham.

## How to Run the Project

1. **Clone the repository**:
   ```
   git clone https://github.com/yourusername/spam-email-classification.git
   ```

2. **Install the required dependencies**:
   ```
   pip install numpy pandas scikit-learn
   ```

3. **Run the project**:
   Load the dataset, preprocess the data, and train the model using the provided Python scripts.

## Dataset

The dataset used for this project is publicly available and contains 5,572 emails labeled as either spam or ham.

- **Number of samples**: 5,572
- **Features**: Email text (message)
- **Labels**: Spam (0), Ham (1)

## Conclusion

This project demonstrates the application of logistic regression and natural language processing techniques for classifying emails as spam or ham. It showcases how machine learning can be effectively used to build spam detection systems.

## Future Improvements

- Exploring other machine learning algorithms (e.g., Random Forest, SVM, Neural Networks) to compare performance.
- Implementing additional preprocessing techniques like stemming or lemmatization to improve the model.
