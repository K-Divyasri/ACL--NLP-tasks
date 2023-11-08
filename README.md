# ACL-Emotional_Analysis
This is a proof of concept for the Emotional Analysis shared task organized by the ACL DravidanLangTech 2022. We converted it into a pandas data frame and started preprocessing We removed the emoticons and removed unmatched data points from the data frame along with the stop words, we then printed out the distribution of the data frame and found the data was highly imbalanced, so we used 'SMOTE -  Synthetic Oversampling Technique' to balance the data and applied a LaBSE transformer which is a derivate of the BERT model, we passed it to a SVM classifier attaining an accuracy of 0.44
Load the given dataset as 'df' at line 8 in the given code to run it.
In particular, we will require the following packages in the environment to run the above code:

datasets==1.17.0
nltk==3.5
pandas==1.3.5
Pillow==9.0.0
scikit-learn==0.23.2
torch==1.8.2+cu111
transformers==4.15.0
dvc==2.9.3 (for automating the training pipeline)



