# NLP-solution-CW1
Identification of Randomised Controlled Trials (RCT) (for performing better systematic literature review and evidence-based healthcare)



**Project Overview**

This project focuses on classifying Randomized Controlled Trial (RCT) abstracts using multiple machine learning models, including Naïve Bayes, Logistic Regression, and a CNN-based deep learning model. The dataset consists of RCT and non-RCT abstracts, with text preprocessing and feature extraction techniques applied to improve model performance.

**Dependencies & Installation**

Before running the code, ensure you have installed the required dependencies:


pip install wordcloud tensorflow nltk seaborn joblib pandas numpy matplotlib scikit-learn

**Dataset**

The dataset is loaded from a text file (rct_data.txt) and is structured with the following columns:

PMID: Unique identifier for each record

Label: Binary classification (1 = RCT, 0 = Non-RCT)

Year: Year of publication

Title: Title of the paper

Abstract: The abstract text

**Preprocessing Steps**

Data Cleaning: Removing numbers, punctuation, and converting text to lowercase.

Tokenization & Stopword Removal: Using NLTK to clean and preprocess text.

TF-IDF Feature Extraction: Converting cleaned text into numerical features using TfidfVectorizer.

Splitting Data: Training and testing split using an 80-20 ratio.

**Models Implemented**

1. Naïve Bayes Classifier

Uses TF-IDF vectorized text for classification.

Evaluated using accuracy, precision, recall, and confusion matrix.

2. Logistic Regression

Similar workflow as Naïve Bayes, with additional performance metrics.

3. Convolutional Neural Network (CNN)

Tokenizes and pads sequences.

Uses an embedding layer, Conv1D, and GlobalMaxPooling1D for classification.

Compiled with binary cross-entropy loss and Adam optimizer.

**Model Evaluation & Results**

Accuracy scores are compared across all models.

Confusion matrices are generated for each model.

Precision and recall metrics are visualized using bar plots.

**Visualization**

Several visualization techniques are applied, including:

WordClouds: Visualizing frequent words in RCT vs. Non-RCT abstracts.

Bar Charts: Comparing accuracy, precision, and recall across models.

Confusion Matrices: Evaluating misclassification.
