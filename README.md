# ACL-Emotional_Analysis

## Overview

This is a proof of concept for the Emotional Analysis shared task organized by the ACL DravidanLangTech 2022.

## Dataset
The dataset was given by the organizers of Emotional Analysis - DravidanLangTech 
Tamil is a low resource South Indian Dravidan Language, the emotional analysis dataset contains 5940 datapoints with 8 classes and the abusive comment detection dataset contains 9440 datapoints with 

## Preprocessing

We converted the dataset into a pandas data frame and started preprocessing. We removed emoticons and unmatched data points from the data frame along with stop words. We then printed out the distribution of the data frame and found the data was highly imbalanced.

## Data Balancing

To address imbalance, we used 'SMOTE - Synthetic Oversampling Technique' to balance the data.

## Modeling 

We then applied a LaBSE transformer which is a derivate of the BERT model. This was passed to a SVM classifier, attaining an accuracy of 0.44.

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


## 📝 Notebook: [`colabs at`](./notebooks/Copy of run1_tfidf+labse.ipynb)

## papers published 

- `Emotion Analysis in Tamil Text using Language Agnostic Embeddings`
published in ACL 2022 Anthology. https://aclanthology.org/2022.dravidianlangtech-1.17/
- `Abusive Comment Detection in Tamil Code-Mixed Data Using Custom Embeddings with LaBSE`
- published in ACL 2022 Anthology. https://aclanthology.org/2022.dravidianlangtech-1.18/




