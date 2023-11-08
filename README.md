# ACL-NLP tasks 2022

## Overview

This is a proof of concept for the Emotional Analysis shared task organized by the ACL DravidanLangTech 2022.

## Dataset
The dataset was given by the organizers of Emotional Analysis - DravidanLangTech 
Tamil is a low resource South Indian Dravidan Language, the emotional analysis dataset contains 5940 datapoints with 8 classes and the abusive comment detection dataset contains 9440 datapoints with 11 classes

## Preprocessing

We converted the dataset into a pandas data frame and started preprocessing. We removed emoticons and unmatched data points from the data frame along with stop words. We then printed out the distribution of the data frame and found the data was highly imbalanced.

## Data Balancing

To address the imbalance, we used 'SMOTE - Synthetic Oversampling Technique' to balance the data.

## Modeling - performance scores of model deployed

| Feature | Classifier | Accuracy | Precision | Recall | F1 score |
| :---: | :---: | :---: | :---: | :---: | :---: |
| TF-IDF | SVM | 0.71 | 0.75 | 0.28 | 0.31 |
| TF-IDF | K Nearest Neighbours Classifier | 0.66 | 0.44 | 0.27 | 0.31 |
| TF-IDF | distiluse-base-multilingual-cased-v2 | 0.74 | 0.69 | 0.38 | 0.44 |
| TF-IDF | MLP | 0.70 | 0.52 | 0.41 | 0.45 |
| TF-IDF | sBert | _**0.74**_ | 0.67 | 0.38 | 0.45 |
| LaBSE | SVM | 0.71 | 0.67 | 0.32 | 0.38 |
| LaBSE | MLP | 0.66 | 0.43 | 0.38 | 0.40 |
| TF-IDF +LaBSE | SVM with HiClass | 0.72 | 0.65 | 0.32 | 0.37 |
| TF-IDF +LaBSE | Random Forest | 0.68 | 0.50 | 0.34 | 0.39 |
| TF-IDF +LaBSE | Gradient Boosting Classifier | 0.69 | 0.53 | 0.55 | 0.40 |
| TF-IDF +LaBSE | MLP | 0.67 | 0.49 | 0.44 | 0.45 |
| TF-IDF +LaBSE | SVM on Hierachial Levels | 0.72 | 0.68 | 0.41 | 0.46 |
| TF-IDF +LaBSE | SVM | _**0.74**_ | 0.70 | 0.44 | 0.49 |
| TF-IDF +LaBSE | Linear SVM with class-weights | _**0.74**_ | 0.54 | 0.46 | 0.49 |
| TF-IDF +LaBSE + XAI | SVM | _**0.74**_ | 0.68 | 0.38 | 0.45 |
| TF-IDF +LaBSE + XAI | SVM on Hierachial levels | 0.72 | 0.67 | 0.41 | 0.46 |
| TF-IDF +LaBSE + XAI | Linear SVM with intercept fitting | _**0.74**_ | 0.57 | 0.44 | 0.48 |
| TF-IDF +LaBSE + XAI | Linear SVM with class-weights | _**0.74**_ | 0.54 | 0.46 | _**0.50**_ |






## Instructions

To run the code:

1. Load the given dataset as 'df' at line 8

## Requirements

In particular, we will require the following packages:

- `datasets==1.17.0`
- `nltk==3.5`
- `pandas==1.3.5`
- `Pillow==9.0.0`
- `scikit-learn==0.23.2`
- `torch==1.8.2+cu111`
- `transformers==4.15.0`
- `dvc==2.9.3` *(for automating the training pipeline)*

> _**Note:** It is best to have some GPU available to train the multimodal models (Google Colab can be used)._


## 📝 Notebook: [`colabs at`] (./notebooks/.*.ipynb)

## papers published 

- `Emotion Analysis in Tamil Text using Language Agnostic Embeddings`
published in ACL 2022 Anthology. https://aclanthology.org/2022.dravidianlangtech-1.17/
- `Abusive Comment Detection in Tamil Code-Mixed Data Using Custom Embeddings with LaBSE`
- published in ACL 2022 Anthology. https://aclanthology.org/2022.dravidianlangtech-1.18/




