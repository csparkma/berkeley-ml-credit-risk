# Credit Risk Challenge
Module 17 in Berkeley Data Analytics Bootcamp

# Resampling
  While Oversampling has the highest Balanced Accuracy score of 69% as well as a fairly medium to high Recall (i.e. accurately classifying "High Risk" loans), the Precision score for all of the sampling methods would cause me to stray away from advising the use of any of the models. The Precision score is terribly unbalanced, meaning that out of the population that the model classified as "High Risk", very few actually were.
  For the sake of this use-case, I believe Recall is more important as it would take very minimal manual research to find the users that were misclassified as "High Risk" that are actually current on their loans. It is more important to catch the ones that are "High Risk". That being said, due to the imbalance being so drastic in Precision and Recall/Balanced Accuracy Score still being <70%, I would advise that we attempt to improve both score (with an emphasis on Recall) before moving it into production.
 
 ##### Logistic Regression
 - **Oversampling:**
    - **Naive Random Oversampling**
      - Precision: 99% avg
          - 1% for High Risk
          - 100% for Low Risk
      - Recall: 64% avg
          - 74% for High Risk
          - 63% for Low Risk
      - Balanced Accuracy Score: 69%
    - **SMOTE Oversampling:**
      - Precision: 99% avg
          - 1% for High Risk
          - 100% for Low Risk
      - Recall: 68% avg 
          - 64% for High Risk
          - 68% for Low Risk
      - Balanced Accuracy Score: 66%
- **Undersampling:**
    - Precision: 99% avg 
        - 1% for High Risk
        - 100% for Low Risk
    - Recall: 41% avg
        - 66% for High Risk
        - 41% for Low Risk
    - Balanced Accuracy Score: 53%
 - **Combination:**
    - Precision: 99% avg
        - 1% for High Risk
        - 100% for Low Risk
    - Recall: 59% avg
        - 66% for High Risk
        - 41% for Low Risk
    - Balanced Accuracy Score: 65%
    
# Ensemble Classifiers
We were attempting to improve our overall Balanced Accuracy Score with an emphasis on Recall. The reason being that it is more important for us to find all actual "High Risk" loans rather than accurately classifying "High Risk". It is not ideal to inaccurately classify individuals that are current with their loans, however, it is easier to monitor more acconts that end up paying on time than missing ones that are delinquent.
 Based on the findings below, I believe we should test and track the Easy Ensemble Classifier in production on a trial basis. The Balanced Accuracy Score and Recall are both very high (93% and 94% respectively). The Precision is low, but as we discussed, we are more worried about catching all "High Risk".
 While we are testing, we should still attempt to refine and increase the Precision, as we do not want to miss out on giving loans to those that will actually pay it back. However, since the volume of those that the model predicts are "High Value" are a small % of the total, we should be able to still handle these on a case-by-case basis.
 
  High Sensitivity means that among people who actually are **High Risk**, most of them will be identified correctly. 
  High precision means that if they are classified as **High Risk**, there’s a high likelihood that they actually are High Risk.
  
##### Balanced Random Forest Classifier:**
  - Precision: 99%
    - 81% for High Risk
    - 100% for Low Risk
  - Recall: 100%
    - 29% for High Risk
    - 100% for Low Risk
  - Balanced Accuracy Score: 64%
##### Easy Ensemble Classifier:**
- Precision: 99%
    - 9% for High Risk
    - 100% for Low Risk
- Recall: 94%
    - 92% for High Risk
    - 94% for Low Risk
- Balanced Accuracy Score: 93%
      
      
      
      
      
      
      
      
      
      
