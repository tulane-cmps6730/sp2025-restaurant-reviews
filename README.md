**A Comprehensive Restaurant Review Sentiment Classifier Using a Transformer Model**

**CMPS 6730 - Aaron Dumont and Jacob Schenck**

**Introduction:** The restaurant industry is highly competitive and reviews strongly influence success. Restaurants need timely and detailed feedback for continuous improvement and innovation. The goal of the present study is to build a multi-label sentiment classifier for restaurant reviews that analyzes overall and aspect-based (food, service, ambiance, price, context) sentiment to provide timely and granular feedback for restaurants.

**Methods:** Using keyword spotting for aspect identification and data from the Yelp open database, we compared a TF-IDF + Logistic regression baseline model with a fine-tuned DistilBERT transformer model to predict sentiment for the 5 aspects and an overall review sentiment. VADER was used to generate proxy labels for sentiment classification for the entire Yelp database review set due to the large data scale. However, our approach was corroborated by using human-labeled star ratings to predict overall sentiment and training/testing both models using this data.

**Results:** 1.5 million reviews were included (80%/20% train/test split).The transformer-based model had superior precision, recall, weighted F1-score, accuracy and micro/macro averages across all 6 labels compared to the baseline logistic regression model. For the overall sentiment, the superior performance was corroborated using data with human-generated manual labels to complement experiments with VADER generated proxy labels. 

**Conclusions:** A fine-tuned transformer (DistilBERT) model is highly effective for multi-aspect and overall sentiment classification for restaurant reviews, significantly outperforming a logistic regression model. This should prove useful for the provision of rapid granular and summary review analysis for restaurants for continuous improvement.

Here is a summary of key quantitative results for the model with aspect and overall sentiment classification, trained using >1.5 million reviews (proxy-labeled with VADER):
 
![image](https://github.com/user-attachments/assets/b4796812-bf30-4006-9536-9906f1b55f98)

Here is a summary of key quantitative results for the model with overall sentiment classification using human-labeled data, trained using > 1.5 million reviews. This was to complement the approach using VADER proxy-labeled data. It demonstrates similar results and the continued superiority of the transformer model over the baseline logistic regression model.

![image](https://github.com/user-attachments/assets/6677a19d-5ddd-42d6-9f50-ac719736f509)

Here is the initial input prompt:
![image](https://github.com/user-attachments/assets/e6cbbdb1-11ba-47b3-bbdd-3b8c99f12f25)
 
Examples using the initial sentiment classifier:
 
 ![image](https://github.com/user-attachments/assets/8f1e6620-b7eb-4710-8ea8-9f699aaf0f30)
 ![image](https://github.com/user-attachments/assets/50c8053c-52dd-497a-8e1f-91a0c94e5c41)
![image](https://github.com/user-attachments/assets/4f5ddcde-f181-4cfc-8406-34548f95c03a)

Examples using or human-labeled overall sentiment classifier:
![image](https://github.com/user-attachments/assets/09f5180f-b964-45db-9e05-cc5ce3a98b2f)
 

