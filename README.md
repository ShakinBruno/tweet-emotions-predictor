# Natural Language Processing Class - Project 1: Tweet Emotions Predictor

### Author: Dominik Mikołajczyk

## Project Overview
The aim of this project is to create a classification model that can predict the emotions guiding a user while writing a tweet based on its text content. The model labels the tweets with the appropriate emotion. This project involves data preprocessing, model training, and evaluation to achieve the best possible accuracy in emotion prediction.

## Requirements
To run this project, you need to have the following Python libraries installed:

1. Jupyter Notebook:
   ```bash
   pip install jupyter
   ```

2. Other required Python libraries:
   ```bash
   pip install numpy==1.21.5
   pip install matplotlib==3.5.2
   pip install pandas==1.4.4
   pip install scikit-learn==1.0.2
   pip install nltk==3.7
   pip install contractions==0.1.73
   pip install wordcloud==1.9.2
   ```

## Dataset
The dataset used in this project is sourced from Kaggle and can be found [here](https://www.kaggle.com/datasets/praveengovi/emotions-dataset-for-nlp). Initially, the dataset contained 20,000 records. After preprocessing, which included rejecting irrelevant records, tokenizing sentences, and augmenting data, the dataset expanded to 38,988 records. The dataset was then split into training and testing sets:
- 31,190 examples for the training set (80% of all records)
- 7,798 examples for the testing set (20% of all records)

### [Original dataset](https://github.com/ShakinBruno/tweet-emotions-predictor/blob/main/Data/tweet_emotions.csv)

![image](https://github.com/ShakinBruno/tweet-emotions-predictor/assets/71774757/e5bb2dd6-b20d-48b4-9ddd-d47eb306452e)

### [Preprocessed dataset](https://github.com/ShakinBruno/tweet-emotions-predictor/blob/main/Data/tweet_emotions_preprocessed.csv)

![image](https://github.com/ShakinBruno/tweet-emotions-predictor/assets/71774757/106280cb-c1c9-4216-a05f-f7c0a7b9db4a)

## Data Preprocessing
The preprocessing steps involved:
- **Contraction Fixing**: Expanding contractions to their full forms.
- **Tokenization**: Splitting text into individual words.
- **Stop Word Removal**: Removing common words that do not contribute to the emotional content.
- **Lemmatization**: Reducing words to their base or root form.
- **Data Augmentation**: Using synonyms to increase the dataset size and balance class distribution.

## Model Training and Evaluation
Several machine learning models were trained and evaluated to determine the best performer. The models include:
- Dummy Classification
- Logistic Regression
- K Nearest Neighbor Classification
- Random Forest Classification
- Linear Support Vector Classification

The performance of these models was evaluated using metrics such as Accuracy, Precision, Recall, and F1 Score. The table below summarizes the results:

| Model                              | Accuracy | Precision | Recall  | F1 Score |
|------------------------------------|----------|-----------|---------|----------|
| Dummy Classification               | 0.163119 | 0.163117  | 0.163078| 0.163084 |
| Logistic Regression                | 0.873429 | 0.874003  | 0.873605| 0.872992 |
| K Nearest Neighbor Classification  | 0.804052 | 0.806763  | 0.804055| 0.803134 |
| Random Forest Classification       | 0.829956 | 0.834035  | 0.830209| 0.829537 |
| Linear Support Vector Classification | 0.888305 | 0.888718  | 0.888579| 0.887865 |

The best results were achieved by the Linear Support Vector Classification model. The Dummy Classification model was included to highlight the significant difference between random label selection and machine learning algorithms.

## Conclusion
This project demonstrates the effectiveness of various machine learning models in predicting tweet emotions. The preprocessing steps and model evaluations provide a comprehensive approach to handling text data in natural language processing tasks. Future work could explore deep learning models for potentially improved performance.
