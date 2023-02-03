# Credit Risk Analysis: ***Working with Supervised Machine Learning***
## Overview of Project
### Overview:
In this project, we will program six differnt supervised machine learning algorithms and compare them to eachother to identify which model would be ideal for our purpose. We are creating these algorithms to help a bank predict credit risk. Credit risk overall is an unbalanced classification problem due to the tendency of riskly loans outnumbering good loans, therefore, it creates a need to create a classificatio model that can accurately preditct risky loans. We will use a few different approaches to balance out our classification and aim for the best performance of at least one of the models.

### Purpose:
In order to predict which customers are a credit risk, we will use Python and its library of Scikit-learn to carry on our analysis. We will assest how well a model classifies and predicts data. Additionally, we will compare the following machine learning algorithms to determine which one would be the ideal model to use for our purpose:

- Random Over SAMPLER
- SMOTE
- Cluster Centroids
- SMOTEENN
- Balanced Ranfom Forest Classifier
- Easy Ensemble Classifier

Our results will include a classification report as well as an accuracy score that will help us identify which algorithm performs best with the given dataset.

## Results
#### Oversampling Approach
### Random Oversampling:
In this model, our data is clustered into different classes. After this process is done, the instances in our minority class are randomly selected and added to the training data set until the minority and majority classes are balanced. This model returned the following results:
  - Accuracy score: 0.6463970560994359
  - Confusion Matrix:
   
  ![random_over_confusion_matrix](https://user-images.githubusercontent.com/111034667/216506595-2bc29ef0-6376-4c68-9515-c13f0adc9e31.png)
  
  - Imbalanced classification report:
   
![random_over_report](https://user-images.githubusercontent.com/111034667/216506438-60780961-e707-493e-acf1-6f420cc367c1.png)

  The report shown above tells us the following:

  - Precision: the score for high risk is 0.01 and 1.00 for low risk.
  - Recall/Sensitivity: the score for high risk is 0.71 and 0.58 for low risk.

### SMOTE Oversampling:
This model, similarly to Random Oversampling, the size of the minority is increased by interpolating them. A number of its closest neighbor is chosen, and based on those values, the new values are created.This model returned the following results:
  - Accuracy score: 0.6586230769943224
  - Confusion Matrix:
   
  ![SMOTE_confusing_matrix](https://user-images.githubusercontent.com/111034667/216507072-2d0618c5-1340-4927-90b9-844ad941b0f0.png)
  
  - Imbalanced Classification Report:
   
![SMOTE_report](https://user-images.githubusercontent.com/111034667/216507224-6044bf45-1e99-4471-87f0-267bef9eec57.png)

  The report shown above tells us the following:
  
  - Precision: the score for high risk is 0.01 and 1.00 for low risk.
  - Recall/Sensitivity: the score for high risk is 0.63 and 0.68 for low risk.
    
#### Undersampling
### Cluster Centroids:
In this model, our algorithm clusters the majority class, then generates centroids that are representative of the clusters. Then, the majority class is undersampled down to the size of the minority class.This model returned the following results:
  - Accuracy score:0.5447339051023905
  - Confusion Matrix:
  
  ![centroid_confusion_matrix](https://user-images.githubusercontent.com/111034667/216508259-1af12004-62dc-41d8-a366-cbeaee698ae1.png)
  
  - Imbalanced Classification Report:
  
![centroid_report](https://user-images.githubusercontent.com/111034667/216508270-cebe28f4-87fb-40b6-814d-d383894354a6.png)

 The report shown above tells us the following:
  
 - Precision: the score for high risk is 0.01 and 1.00 for low risk.
 - Recall/Sensitivity: the score for high risk is 0.69 and 0.40 for low risk.
    
#### Combination of Undersampling and Oversampling
### SMOTEENN:
In this model , our algorithm first oversamples the minority class with the approach of SMOTE and later on cleans the resulting data with an undersampling strategy. In the case where the two nearest neighbors points of a data point belong to two different classes, the data point is dropped.The results for this model are the following:
  - Accuracy score:0.5447339051023905
  - Confusion Matrix:
  
  ![SMOTEENN_confusion_matrix](https://user-images.githubusercontent.com/111034667/216508741-fbc06ffa-629d-4dce-911f-552c2734ecd4.png)
  
  - Imbalanced Classification Report:
  
  ![SMOTEENN_report](https://user-images.githubusercontent.com/111034667/216508760-5d5cb39c-3bad-4047-b6eb-c3e8344ba37b.png)
  
 The report shown above tells us the following:
  
 - Precision: the score for high risk is 0.01 and 1.00 for low risk.
 - Recall/Sensitivity: the score for high risk is 0.73 and 0.60 for low risk. 
    
#### Ensamble Learners
### Balanced Random Forest Classifier:
In this model,our data is classified similarly to the Random Forest model but it randomly undersamples each bostrap sample to balance it out. The following are the results of our model

  - Accuracy score: 0.7885466545953005
  - Confusion Matrix:
  
  ![balanced_confusion_matrix](https://user-images.githubusercontent.com/111034667/216509325-34ed379e-f105-4e5f-9593-a6691aa6467a.png)

  - Imbalanced Classification Report:

![balanced_report](https://user-images.githubusercontent.com/111034667/216509350-bc2283a1-9b17-4a11-a67c-fea7dc029ae8.png)

  The report shown above tells us the following:
  
  - Precision: the score for high risk is 0.03 and 1.00 for low risk.
  - Recall/Sensitivity: the score for high risk is 0.70 and 0.87 for low risk.

### Easy Ensamble AdaBoost Classifier:
In this model, our data is classified with the AdaBoost learners which train on different balanced bootstraps samples by randomly under-sampling the samples. The results of this model are the following:

  - Accuracy score:0.9316600714093861
  - Confusion Matrix:
  
  ![Ada_confusion_matrix](https://user-images.githubusercontent.com/111034667/216509672-74784b7e-63ba-4c3d-a0a5-0f78e51f58a2.png)
  
  - Imbalanced Classification Report:
  
  ![Ada_report](https://user-images.githubusercontent.com/111034667/216509684-aadbe999-016c-46ff-bf06-c11cad1d1411.png)
  
  The report shown above tells us the following:
  
  - Precision: the score for high risk is 0.09 and 1.00 for low risk. 
  - Recall/Sensitivity: the score for high risk is 0.92 and 0.94 for low risk.
  
## Summary

Overall, the model that performed the best with the dataset provided was the Easy ensamble AdaBoost classifier. The accuracy, precision and recall score were the highest across all variables. In this case, it would be ideal to use this model since the recall score is the highest for the high risk and low risk categories, meaning that our model will corectly classifiy the customers in their respective category, minimizing the amount of customers that would be identified as a high risk when actually being low risk and vise versa.This can also be seen in the confusion matrix,in which it shows that there were 93 customers that were correctly categorized as low risk and 16,121 correctly categorized as high risk. This model is ideal for the bank since it will correctly categorize most customers.
