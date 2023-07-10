# Natural Language Processing Class - Project 1: Tweet Emotions Predictor
### author: Dominik Mikołajczyk

## The task the of project
The aim of the project was to create classification model that, based on tweet text content; is able to predict the emotions that guided the user while writing the tweet and label them correctly.

## Requirements:
1. Install jupyter:
    <!-- -->
    
        pip install jupyter
        
2. Install other required python libraries:
    <!-- -->
    
        pip install numpy==1.21.5
        pip install matplotlib==3.5.2
        pip install pandas==1.4.4
        pip install scikit-learn==1.0.2
        pip install nltk==3.7
        pip install contractions==0.1.73
        pip install wordcloud==1.9.2
        
## Dataset
The data comes from the Kaggle platform. The data can be found at [this](https://www.kaggle.com/datasets/praveengovi/emotions-dataset-for-nlp) link. At the beginning, 20000 records were counted in the dataset and after rejecting irrelevant records, tokenizing sentences ​​and augmenting data, 38988 records were obtained. After division into training and testing sets, we have:
- 31190 examples for the training set (80% of all records)
- 7798 examples for the testing set (20% of all records)

### [Original dataset](https://github.com/ShakinBruno/tweet-emotions-predictor/blob/main/Data/tweet_emotions.csv)

![image](https://github.com/ShakinBruno/tweet-emotions-predictor/assets/71774757/e5bb2dd6-b20d-48b4-9ddd-d47eb306452e)

### [Preprocessed dataset](https://github.com/ShakinBruno/tweet-emotions-predictor/blob/main/Data/tweet_emotions_preprocessed.csv)

![image](https://github.com/ShakinBruno/tweet-emotions-predictor/assets/71774757/106280cb-c1c9-4216-a05f-f7c0a7b9db4a)

## Results

![image](https://github.com/ShakinBruno/tweet-emotions-predictor/assets/71774757/1d923bc6-e71f-4ecf-91ba-90c81bc42189)

The best results in every aspect were achieved by the SVC algorithm, although the difference between the other models except for the dummy one isn't strongly significant. I have included dummy model for evaluation results to show significant difference between randomly choosing labels and machine learning algorithms. The metrics Accuracy, Precision, Recall and F1 Score were used for evaluation.
