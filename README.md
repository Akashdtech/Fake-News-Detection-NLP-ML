# Fake-News-Detection-NLP-ML
This project implements a text classification pipeline to detect fake news using a Kaggle dataset. It uses a LinearSVC model for classification, employing a TF-IDF vectorizer to process the text data. Here’s a breakdown of the workflow:

Data Loading:

    The script loads the dataset from a CSV file containing text data and corresponding labels (FAKE and REAL news).
    The labels are then mapped to numerical values (FAKE = 0, REAL = 1).

Data Preprocessing:

    The data is split into training and testing sets (80% for training, 20% for testing) using train_test_split.
    A TfidfVectorizer is used to transform the text data into TF-IDF features. It removes common English stop words and restricts the maximum document frequency to 70% (max_df=0.7) to reduce the impact of overly common words.

Model Training:

    A LinearSVC model is trained on the vectorized training data (X_train_vectorized) and the corresponding labels (y_train).

Model Evaluation:

    The trained model is evaluated on the test data (X_test_vectorized), and accuracy is computed using accuracy_score.

Prediction on New Data:

    The script opens and reads a new text file (test.txt), which contains a new news article for classification.
    This new text is transformed into TF-IDF features and passed to the trained model for prediction. The result (0 for fake, 1 for real) is printed.

Expected Output:

    The accuracy of the model on the test data is printed.
    The content of the test.txt file is printed.
    The model’s prediction for the new news article is printed, indicating whether it is classified as FAKE or REAL.

This code provides a simple yet effective pipeline for fake news detection using text data and the LinearSVC classifier.
