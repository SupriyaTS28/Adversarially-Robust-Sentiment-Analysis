# Adversarially-Robust-Sentiment-Analysis

# Introduction

  Sentiment Analysis: scoring or classifying a piece of text based on the emotions of the text.

  Applications: 
  1. Product Recommendation
  2. Social media monitoring
  3. Market research
  4. Customer service
  
  Adversarial Robustness: Are deep neural networks robust to adversarial samples?
  Adversarial sample: Strategically modified input sample that fools the model to give wrong predictions.

  Importance of adversarial robustness:
  1. Reliability
  2. Generalizability

  Goal: 
  1. Learn adversarially robust deep neural networks for sentiment analysis.
  2. Generate adversarial samples to attack the model.
  3. Use generated adversarial samples with natural samples to train the model for adversarial robustness.
  4. Use the learned model to correctly predict both natural and adversarial samples. 

  Conclusion:
  1. This project successfully builds an adversarially robust sentiment analysis model by training the model with both natural and generated adversarial samples.
  2. The experimental results show that both adversarial training approaches, data augmentation and model generalization improve the adversarial accuracy of the models,
     but model regularization results in more generalized and adversarially robust model. 
  3. There are many possible extensions for this work-
       * Try stronger attack methods and see if Adversarial Training will generalize for all types of attacks.
       * Extend this approach to see how it performs on other NLP tasks.
