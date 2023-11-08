# ACL-Emotional_Analysis

## Overview

This is a proof of concept for the Emotional Analysis shared task organized by the ACL DravidanLangTech 2022.

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

The following packages are required:


datasets==1.17.0
nltk==3.5
pandas==1.3.5
Pillow==9.0.0
scikit-learn==0.23.2
torch==1.8.2+cu111
transformers==4.15.0
dvc==2.9.3 (for automating the training pipeline)



