# Adversarially-Robust-Sentiment-Analysis

## Problem Statement
Sentiment Analysis: scoring or classifying a piece of text based on the emotions of the text.

  Applications: 
  
  
  Adversarial Robustness: Are deep neural networks robust to adversarial samples?
  
  Adversarial sample: Strategically modified input sample that fools the model to give wrong predictions.

  Importance of adversarial robustness:
  1. Reliability
  2. Generalizability

### Use Case
1. Product Recommendation
2. Social media monitoring
3. Market research
4. Customer service

## Dataset
Curated a balanced dataset consisting of 50K COVID-19 related tweets, with two classes: positive and negative.<br />
Utilized tweet id's from “COVID-19: The First Public Coronavirus Twitter Dataset”[1] to create the dataset.<br />
Training Set =  25000 samples<br />
Validation Set = 7500 samples<br />
Test Set = 17500 samples<br />

[1] Emily Chen, Kristina Lerman, Emilio Ferrara, “COVID-19: The First Public Coronavirus Twitter Dataset”,arXiv:2003.07372 [cs.SI]. 

## Machine Learning Problem Statement
This is a Text classification (Sentiment Analysis) problem with the goal to produce a reliable model that is immune to adversarial attacks.

## Approach
1. In this project a Bi directional LSTM (Bi-LSTM) is trained to develop an adversarially robust model for sentiment analysis.
2. Adversarial samples to attack the model are generated using DeepWordBug[2] : a Black-box attack<br />
   * Scoring<br /> 
   * Transformation-Swap; Delete; Insert<br />
3. Adversarial Training is used as the Defense method<br />
   The two adversarial training approcahes considered are-<br />
    * Data Augmentation
    * Model Regularization
4. Generated adversarial samples with natural samples are used to train the model for adversarial robustness to correctly predict both natural and adversarial samples. 

[2] J. Gao, J. Lanchantin, M. L. Soffa and Y. Qi, "Black-Box Generation of Adversarial Text Sequences to Evade Deep Learning Classifiers," 2018 IEEE Security and Privacy Workshops (SPW), San Francisco, CA, 2018, pp. 50-56.

## Evaluation Metric (KPI)
Accuracy

## Result
![results_table](https://user-images.githubusercontent.com/24207916/138027766-1d1fb39d-d9ef-4903-b816-f6d739264ade.JPG)
1. This project successfully builds an adversarially robust sentiment analysis model with an accuracy of 84.7% on generated adversarial samples and 88.39% on clean samples.
2. The experimental results show that model generalization approach results in better generalized and adversarially robust model compared to data augmentation approach. 
3. Possible extensions for this work-<br />
   * Implement stronger attack methods and see if Adversarial Training will generalize for all types of attacks.<br />
   * Extend this approach to other NLP tasks.<br />
