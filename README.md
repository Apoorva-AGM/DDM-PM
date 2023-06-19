# DDM-PM

Data Driven Methodology for Predictive Maintenance using the Dataset AI4I2020 is submitted towards the Studienarbeit for Mechatronics course at Universität Siegen. The goal of this work is to create a model which can accurately predict machine failure based on given data and provide an evaluation of the performance metrics. Questions that will be answered are -
1. Which model performs the best for binary classification?
2. Which model performs the best for multi-class classification?
3. Which features contribute to failure?
4. Which features result in a specific failure?
5. Does re-sampling really help?
6. How to evaluate the performance metrics?
7. Hyperparameter tuning?

In conclusion, the dataset is evaluated against Logistic Regression, Decision Tree Classifier, Random Forest Classifier, Gradient Boosting Classifier and Extreme Gradient Boosting Classifier with variations of 
1. All the features,
2. Engineered features,
3. Tuned Hyperparameters
4. Oversampling the dataset.
Also the following questions are answered, 
1. Which model performs the best for binary classification?
    Extreme Gradient Boosting Classifier with tuned hyperparameters proves to be the best performing model for binary classification. Following are the evaluations for the model.
    Accuracy 0.985464 	
    Precision 0.985464 	
    Recall 0.984568 	
    F1 Score 0.984277 	
    MCC 0.747356 	
    ROC_AUC 0.987951
    
2. Which model performs the best for multi-class classification?
    Extreme Gradient Boosting Classifier with and without tuned hyperparameters result in similar performing models and fare the best compared to other models for multi-class classification. Following are the evaluations for the model.
    XGB:
        Accuracy 0.985965 	
        Precision 0.985965 	
        Recall 0.981726 	
        F1 Score 0.983675 	
        MCC 0.780547 	
        
   XGB with tuned Hyperparameters:
        Accuracy 0.985464 	
        Precision 0.985464 	
        Recall 0.980330 	
        F1 Score 0.982866 	
        MCC 0.771324 	
        
3. Which features contribute to failure? Which features result in a specific failure?
    TWF: Quality variants add 5/3/2 min of tool wear. Depends mainly on the features Tool wear and Type of the machine. Occured 120 times in the dataset where the tool wear ranged between 200 and 240 mins.
    PWF: Mainly dependent on Torque and Rotational speed. When the product of Torque and Rotational speed is either less than 3500 or greater than 9000, it results in Power Failure. Occured 97 times in the dataset. 
    HSF: Mainly dependent on the air temperature and process temperature difference. When the range of (Air Temperature – Process Temperature) is less than 8.6 K and Rotational speed is less than 1380 rpm, the Heat dissipation failure is flagged.
    OSF: Dependent on the type of the machine, the Tool wear and Torque:
    For L – Tool wear * Torque > 11000, 
        M - > 12000, 
        H - 13000 
    Occured at 98 points in dataset.
    RNF: Random no particular feature results in random failure
    
4. Does re-sampling really help?
    Based on the performance metrics, it can be clearly seen that the re-sampling did not result in better performance for both binary and multi-class classification.
    
6. How to evaluate the performance metrics?
    Accuracy
    Precision
    Recall
    F1 Score
    MCC

7. Hyperparameter tuning?
    Hyperparameter tuning led to a slight improvement in the performance for models both binary and multi-class classification.
