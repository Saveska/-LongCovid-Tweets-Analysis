# LongCovid Tweet Classification

## Overview

This project aims to classify tweets related to Long COVID into different categories, such as symptoms, treatments, personal experiences, or scientific research. By categorizing these tweets, we can gain insights into the topics and trends surrounding Long COVID in social media.

## Table of Contents

- [Overview](#overview)
- [Data](#data)
- [Data Preparation](#data-preparation)
- [Data Cleaning](#data-cleaning)
- [Data Processing](#data-processing)
- [Feature Extraction](#feature-extraction)
- [Model Training](#model-training)
- [Evaluation](#evaluation)
- [Data Visualization](#data-visualization)

## Data

The data for this project is collected from tweets related to Long COVID. The dataset is stored in a CSV file, and it contains information about the tweets, including their text.

## Data Preparation

We begin by reading the data from the CSV file and preparing it for analysis. This includes handling missing values and cleaning the text data.

## Data Cleaning

To clean the text data, we perform several preprocessing steps:

- Removing URLs
- Removing hashtags
- Removing mentions
- Removing punctuation marks
- Removing numbers
- Removing stop words
- Removing multiple whitespaces
- Removing emojis

After cleaning, the text data is transformed into a suitable format for analysis.

## Data Processing

We determine the category of each tweet using keyword matching. We create lists of relevant keywords or phrases for each category, such as symptoms, treatments, personal experiences, and scientific research. By matching these keywords against the tweet text, we assign tweets to the appropriate category.

## Feature Extraction

To represent the tweet data numerically, we use Word2Vec embeddings. We tokenize the text data and build a Word2Vec model to create embeddings for each tweet. These embeddings serve as features for our classification model.

## Model Training

We train a Support Vector Machine (SVM) classifier using the Word2Vec embeddings as input features. The SVM model is used to predict the category of each tweet.

## Evaluation

We evaluate the performance of the model using classification metrics such as accuracy, precision, recall, and F1-score. These metrics provide insights into how well the model classifies tweets into different categories.
The results exhibit a varying degree of success across the different categories. Notably, the "Personal Experiences" and "Scientific Research" categories exhibit higher precision and recall values, indicating a strong ability of the classifier to correctly identify and categorize these types of tweets. On the other hand, the "Symptoms" and "Treatments" categories show relatively lower precision and recall, suggesting that the classifier faces challenges in consistently identifying tweets belonging to these categories.
The overall accuracy of approximately 81% reflects the model's ability to correctly classify the majority of the tweets in the dataset.

## Data Visualization

We visualize the distribution of tweet categories using bar plots. These visualizations help us understand the distribution of Long COVID-related tweets across different categories.

From visualization it can be seen that the ‘personal experiences’ category prevails, then ‘scientific research’ and ‘symptoms’ follow with similar numbers and the least number of tweets are in the ‘treatments’ category.

## Requirements

- Python
- Google Colaboratory or Jupyter Notebook (for running the code) 
- Libraries such as pandas, numpy, scikit-learn, nltk, and seaborn (for data analysis and modeling)
