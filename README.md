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
Curated a balanced dataset consisting of 50K COVID-19 related tweets, with two classes: positive and negative. 
utilized tweet id's from “COVID-19: The First Public Coronavirus Twitter Dataset”[1] to create the dataset.
Training Set =  25000 samples
Validation Set = 7500 samples
Test Set = 17500 samples

[1] Emily Chen, Kristina Lerman, Emilio Ferrara, “COVID-19: The First Public Coronavirus Twitter Dataset”,arXiv:2003.07372 [cs.SI]. 

## Machine Learning Problem Statement
This is a Text classification (Sentiment Analysis) problem with the goal to produce a reliable model that is immune to adversarial attacks.

## Approach
1. In this project a Bi directional LSTM (Bi-LSTM) is used to develop an adversarially robust model for sentiment analysis.
2. Generate adversarial samples to attack the model.
3. Use generated adversarial samples with natural samples to train the model for adversarial robustness.
4. Use the learned model to correctly predict both natural and adversarial samples. 

## Evaluation Metric (KPI)
Accuracy

## Result
![alt text](https://github.com/supriyatskumar/Adversarially-Robust-Sentiment-Analysis/blob/main/results_table.jpg?raw=true)
1. This project successfully builds an adversarially robust sentiment analysis model with an accuracy of 84.7% on generated adversarial samples and 88.39% on clean samples.
2. The experimental results show that model generalization approach results in better generalized and adversarially robust model compared to data augmentation approach. 
3. Possible extensions for this work-<br />
   * Implement stronger attack methods and see if Adversarial Training will generalize for all types of attacks.<br />
   * Extend this approach to other NLP tasks.<br />
