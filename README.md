# Predicting Success of Kickstarter Projects using Facial Detection

## Project Overview

This repository contains the team report for the "Machine Learning in Applied Settings" course at the University of Cologne. The project focuses on predicting the success of Kickstarter campaigns by leveraging facial detection technologies. By analyzing a dataset of over 15,000 Kickstarter projects, the study investigates whether the presence of human faces in project images can enhance the accuracy of success predictions.

## Methodology

- **Data Collection & Preprocessing:** Data was scraped from Kickstarter using Web Robots, followed by cleaning and feature extraction. Facial detection was performed using OpenCV and RetinaFace to identify the presence of faces in project images.
  
- **Machine Learning Models:** Multiple models were employed, including Logistic Regression, Random Forest, XGBoost, and Neural Networks. Feature selection and hyperparameter tuning were conducted using nested cross-validation and forward feature selection techniques.
  

## Key Findings

- **Model Performance:** XGBoost emerged as the best-performing model with an accuracy of 71.7%. However, the performance of models varied significantly across different iterations due to high variance in feature selection and model training processes. While XGBoost consistently showed superior performance, other models like Random Forest and Logistic Regression also demonstrated competitive accuracy under certain conditions.

- **Impact of Facial Detection:** Incorporating facial detection, particularly with RetinaFace, resulted in a modest improvement in prediction accuracy compared to OpenCV. Projects with detected faces had higher success rates (RetinaFace: 68.27% vs. 48.44%; OpenCV: 38.13% vs. 33.20%) than those without detected faces. However, the inclusion of facial detection features introduced variability in model performance, suggesting that while facial elements can influence funding outcomes, their impact may depend on other interacting factors within the dataset.

- **Variance in Results:** The study observed significant variance in model performance metrics across different cross-validation folds. This variability indicates that the models' ability to generalize may be influenced by the specific data splits and highlights the importance of using robust validation techniques. Nested cross-validation helped mitigate some of this variance, but inconsistencies in feature selection and model stability were still evident, particularly with the Neural Network model where the inclusion of RetinaFace was inconsistent across different data splits.


## Conclusion

The study demonstrates that integrating facial detection into predictive models enhances the ability to forecast the success of Kickstarter projects. RetinaFace, in particular, proved to be a valuable tool in improving prediction accuracy, offering insights for project creators and platform operators to optimize campaign strategies.

