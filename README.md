# Predicting the Preferred Foot of Soccer Players

### Introduction

This project aims to build and evaluate machine learning models for predicting a soccer player's preferred
foot based on various player attributes. The dataset was preprocessed, and several machine learning models
were implemented, including Logistic Regression, Random Forest, Support Vector Machine (SVM), and
Deep Neural Networks (DNN). Different hyperparameter configurations for the DNNs were also explored.
The performance of each model was evaluated using various metrics, including accuracy, precision, recall,
and F1 score. The fundamental goal of this classification task is to furnish invaluable insights into a player's
attributes, which have considerable significance in team formation, strategy development, and player
scouting.

### Dataset Description

The dataset encompasses a rich collection of attributes related to soccer players, encompassing features
like age, skill moves, weak foot proficiency, and performance metrics in areas such as pace, shooting,
passing, dribbling, defending, physical ability, overall player status, and the player's preferred foot. In total,
the dataset comprises approximately 160,000 records. To ensure data quality and consistency, essential
preprocessing was applied, including encoding the preferred foot as 0 for "Left" and 1 for "Right." Moreover,
any records with missing data in the shooting column were meticulously removed from the dataset.

![1](https://github.com/amido84/Deep-Learning/assets/71293836/26c2f7c3-d770-43e2-a56d-895bb90fa272)

![Screen Shot 2024-01-26 at 07 16 55 AM](https://github.com/amido84/Deep-Learning/assets/71293836/19f64650-1043-471d-aa55-10d8bd59a6db)




### Data Visualization
![Screen Shot 2024-01-26 at 07 17 48 AM](https://github.com/amido84/Deep-Learning/assets/71293836/23f6bd64-a274-4a18-aefe-0f0557c0fff1)
![Screen Shot 2024-01-26 at 07 18 02 AM](https://github.com/amido84/Deep-Learning/assets/71293836/4e01edb6-a456-4448-af97-71034da50f6d)



A preliminary dataset analysis revealed that the number of right-footed players significantly outweighed that of left-footed players. Out of approximately 160,000 players, about 120,000 favored their right foot, while only 40,000 preferred their left foot.

### Model Selection and Evaluation

Four machine learning models were implemented and evaluated: Logistic Regression, Random Forest Classification, Support Vector Machine (SVM), and Deep Neural Networks (DNN). Additionally, hyperparameter tuning was performed for DNN models with different numbers of hidden layers (5, 50, and 100).

### Logistic Regression

-	Training Accuracy: 0.75
-	Validation Accuracy: 0.75
-	Test Accuracy: 0.75
-	Precision, Recall, and F1 Score: 0.75, 1.00, and 0.86

Logistic Regression demonstrated consistent and balanced performance on training, validation, and test datasets, making it a reliable classifier for predicting preferred foot.

### Random Forest

- Training Accuracy: 1.00
- Validation Accuracy: 0.80
- Test Accuracy: 0.81
- Precision, Recall, and F1 Score: 0.81, 0.97, and 0.88

Random Forest achieved perfect training accuracy, indicating strong predictive capability. Validation and test sets showed slightly lower accuracy but maintained high precision, recall, and F1 score, suggesting good generalization.


### Support Vector Machine (SVM)

- Training Accuracy: 0.75
- Validation Accuracy: 0.75
- Test Accuracy: 0.75
- Precision, Recall, and F1 Score: 0.75, 1.00, and 0.86, respectively

SVM demonstrated balanced performance with 75% accuracy, indicating reliable predictions. High recall and F1 score suggest its effectiveness in predicting preferred foot.

### Deep Neural Networks (DNN)

Two DNN models were created, one with dropout layers and one without:

* DNN without Dropout:
  - Training Accuracy: 0.75
  - Validation Accuracy: 0.75
  - Test Accuracy: 0.75
  - Precision, Recall, and F1 Score: 0.75, 1.00, and 0.86, respectively
    
![Screen Shot 2024-01-26 at 07 19 31 AM](https://github.com/amido84/Deep-Learning/assets/71293836/87e936d4-00ec-407c-a71f-476f8d576443)

* DNN with Dropout:
   - Training Accuracy: 0.76
   - Validation Accuracy: 0.75
   - Test Accuracy: 0.76
   - Precision, Recall, and F1 Score: 0.76, 0.98, and 0.86, respectively
    
![Screen Shot 2024-01-26 at 07 20 11 AM](https://github.com/amido84/Deep-Learning/assets/71293836/45ca9692-b6de-4a6c-95a3-6055ca3c3e03)

Both DNN models show reasonable accuracy and high recall, indicating their effectiveness in identifying players' preferred feet. The dropout model performs slightly better in terms of precision, recall, and F1 score, showing improved generalization capabilities.


### Hyperparameter Tuning for DNN

DNN models with different numbers of hidden layers (5, 50, and 100) were evaluated:

*	All three models exhibited consistent performance with an accuracy of approximately 0.75.
*	Precision, recall, and F1 scores were consistent across the training, validation, and test sets, ranging from 0.85 to 0.86.
	
![Screen Shot 2024-01-26 at 07 23 11 AM](https://github.com/amido84/Deep-Learning/assets/71293836/056df3d2-93c3-44fe-b907-0c366e8579d1)

In summary, all DNN models with varying hidden layer configurations performed similarly, and the choice of the number of hidden layers did not significantly impact performance.



### Recommendations

-	Random Forest performed the best among the models but showed signs of overfitting. Further tuning is required to enhance its generalization.

-	Deep Neural Networks did not exhibit significant advantages over simpler models for this task. Considering the computational cost of DNN, it is recommended to use Logistic Regression or SVM for this classification task.

-	To further improve the models, data resampling techniques like SMOTE can be employed to address the class imbalance in the dataset. This may lead to more accurate predictions for soccer players' preferred foot.

 In conclusion, while the Random Forest model stands out as the top performer, it requires further optimization to address overfitting. Logistic Regression and SVM are effective alternatives, and data resampling techniques should be considered for improved predictive performance.



