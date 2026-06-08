# Sentiment Analysis Using Social Media Comments

## Project Overview

This project focuses on sentiment analysis using Reddit comments. The main objective is to classify user-generated social media text into sentiment categories such as positive, negative, and neutral.

Social media platforms like Reddit contain large volumes of informal and emotional text. These comments can reflect public opinion, emotional behavior, and possible mental health signals. However, Reddit comments often contain slang, sarcasm, short forms, noisy text, and class imbalance, which makes sentiment classification challenging.

This project compares traditional machine learning models and transformer-based deep learning models to identify which approach performs better for real-world social media sentiment analysis.

## Problem Statement

Sentiment misinterpretation and lack of early detection of emotional distress in social media content are major challenges in digital public health and online moderation.

Manual sentiment analysis is time-consuming, inconsistent, and difficult to scale because social media generates huge amounts of text every day. Also, sentiment datasets are often imbalanced, where some classes such as neutral or negative may be underrepresented.

This project addresses these challenges by building an automated sentiment classification system using Reddit comments and comparing different machine learning and deep learning models.

## Objectives

The main objectives of this project are:

- To preprocess and clean Reddit comment data
- To classify comments into positive, negative, and neutral sentiments
- To compare traditional machine learning and transformer-based models
- To handle class imbalance using techniques such as RandomOverSampler and class weighting
- To perform hyperparameter tuning for improving model performance
- To evaluate models using accuracy, precision, recall, F1-score, and confusion matrix
- To identify the best-performing model for sentiment classification

## Dataset

The project uses a Reddit comments dataset containing text comments and sentiment labels.

The dataset includes:

- Reddit comments
- Sentiment labels
- Positive, negative, and neutral classes

The dataset is preprocessed before training to remove noise and improve model performance.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- NLTK
- Matplotlib
- Seaborn
- Imbalanced-learn
- Hugging Face Transformers
- BERT
- RoBERTa
- Logistic Regression
- SVR
- RandomOverSampler

## Methodology

## 1. Data Collection

Reddit comment data is collected and stored in CSV format. Each comment is associated with a sentiment label.

## 2. Data Preprocessing

The raw text data is cleaned before model training.

Preprocessing steps include:

- Removing null values
- Removing duplicate records
- Converting text to lowercase
- Removing punctuation
- Removing special characters
- Removing unnecessary spaces
- Tokenization
- Stopword removal
- Text normalization

## 3. Feature Extraction

For traditional machine learning models, TF-IDF Vectorization is used to convert text into numerical features.

TF-IDF helps identify important words by considering both word frequency and importance across the dataset.

For transformer models like BERT and RoBERTa, pretrained tokenizers are used to convert text into token IDs, attention masks, and padded sequences.

## 4. Handling Class Imbalance

The dataset may contain an unequal number of samples for each sentiment class. This can make the model biased toward the majority class.

To solve this problem, the project uses:

- RandomOverSampler
- Class weighting
- Stratified train-test split

These techniques help improve the model's performance on minority sentiment classes.

## 5. Model Training

The following models are trained and compared:

- TF-IDF with Logistic Regression
- Support Vector Regression
- BERT
- RoBERTa
- Ensemble Model

The models are trained under controlled experimental conditions to ensure fair comparison.

## 6. Hyperparameter Tuning

Hyperparameter tuning is performed to improve model performance.

Important hyperparameters include:

- Learning rate
- Batch size
- Number of epochs
- Sequence length
- Dropout rate
- Optimizer settings

Tuned models showed better generalization and reduced overfitting compared to default models.

## 7. Model Evaluation

The models are evaluated using the following metrics:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix
- Classification Report

Special focus is given to macro-average and weighted-average scores because they help evaluate performance across all sentiment classes.

## Results

The tuned models showed strong performance on Reddit sentiment classification.

| Model | Accuracy | Remarks |
|---|---:|---|
| Logistic Regression | 92.33% | Strong baseline model after tuning |
| SVR | 89.57% | Good consistency but slightly lower accuracy |
| Ensemble Model | 93.21% | Best overall performance |
| BERT | High | Strong contextual understanding |
| RoBERTa | High | Effective for complex Reddit comments |

The transformer-based models performed better in understanding contextual and subtle sentiment patterns. RoBERTa showed strong performance in handling complex Reddit comments, while Logistic Regression remained useful as a fast and interpretable baseline.

## System Architecture

```text
Reddit Dataset
      |
      v
Data Ingestion
      |
      v
Data Cleaning and Preprocessing
      |
      v
Feature Extraction
      |
      |-----------------------------|
      |                             |
      v                             v
TF-IDF Vectorization        BERT/RoBERTa Tokenization
      |                             |
      v                             v
Traditional ML Models       Transformer Models
      |                             |
      |------------- Evaluation ----|
                    |
                    v
Accuracy, Precision, Recall, F1-score
                    |
                    v
Final Sentiment Prediction
