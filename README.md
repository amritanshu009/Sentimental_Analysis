# Sentiment Analysis Using Social Media Comments

## Project Overview

This project focuses on performing sentiment analysis on social media comments, especially Reddit-based text data. The main goal is to classify user comments into different sentiment categories such as positive, negative, or neutral using machine learning and deep learning techniques.

The project includes text preprocessing, feature extraction, class imbalance handling, model training, evaluation, and comparison of multiple machine learning models. Advanced transformer-based models like BERT and RoBERTa are also used to improve sentiment classification performance.

## Objective

The objective of this project is to build an efficient sentiment analysis system that can understand public opinion from social media comments and classify the emotional tone of text accurately.

This project can be useful in areas such as:

- Social media monitoring
- Mental health trend analysis
- Product review analysis
- Public opinion mining
- Content moderation
- Customer feedback analysis

## Dataset

The dataset used in this project is a Reddit comments dataset named `Reddit.csv`.

The dataset contains social media comments and their corresponding sentiment labels. These comments are used to train and test different machine learning models.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Regex
- Matplotlib
- Seaborn
- XGBoost
- LightGBM
- Imbalanced-learn
- Transformers
- BERT
- RoBERTa

## Project Workflow

## 1. Data Collection

The project uses Reddit comment data stored in CSV format. The dataset contains text-based comments along with sentiment labels.

## 2. Data Preprocessing

Text data is cleaned before training the model. The preprocessing steps include:

- Removing null values
- Removing duplicate records
- Converting text to lowercase
- Removing URLs
- Removing special characters
- Removing numbers
- Removing punctuation
- Removing stopwords
- Tokenization
- Lemmatization
- Cleaning unwanted spaces

## 3. Feature Extraction

For traditional machine learning models, TF-IDF Vectorization is used to convert text data into numerical form.

TF-IDF helps identify important words in a sentence by considering how frequently a word appears in a document and how rare it is across all documents.

## 4. Handling Class Imbalance

The dataset may contain an unequal number of sentiment classes. To solve this problem, RandomOverSampler is used.

RandomOverSampler balances the dataset by increasing the samples of minority classes so that the model does not become biased toward the majority class.

## 5. Model Training

Multiple machine learning models are trained and compared.

The models used in this project include:

- Logistic Regression
- Support Vector Classifier
- Random Forest Classifier
- XGBoost Classifier
- LightGBM Classifier
- BERT
- RoBERTa

## 6. Model Evaluation

The models are evaluated using different performance metrics.

The evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1-score
- AUC score
- Confusion Matrix
- Classification Report

## Model Performance

Transformer-based models such as BERT and RoBERTa achieved the best performance compared to traditional machine learning models.

Approximate best performance:

| Model | Accuracy | F1 Score |
|---|---:|---:|
| Logistic Regression | Good | Good |
| Random Forest | Good | Good |
| SVC | Good | Good |
| XGBoost | Better | Better |
| LightGBM | Better | Better |
| BERT | ~89.6% | ~0.90 |
| RoBERTa | ~89.6% | ~0.90 |

## System Architecture

```text
Reddit Dataset
      |
      v
Data Cleaning and Preprocessing
      |
      v
Text Vectorization using TF-IDF
      |
      v
Class Balancing using RandomOverSampler
      |
      v
Model Training
      |
      v
Model Evaluation
      |
      v
Sentiment Prediction
