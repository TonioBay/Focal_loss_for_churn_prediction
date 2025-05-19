# Binary classification for customer churn detection

This project tests and evaluates different ML models and a simple NN model for binary classification.

## Project information
The data was obtained from [Kaggle](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers). 

## Imbalanced data
The main issue with these dataset is that we have more information about existing customers thant attrited ones and most of the models struggle with imbalanced data, this imbalance can lead to biased model predictions, where the majority class dominates the learning process, and the minority class is often overlooked.

To solve this problem we can use different approaches such as assigning higher weights to the samples of the minority class and lower weights to the majority class during the training process(weighing), but for this project a different solution is taken.

## Focal Loss

[Focal Loss](https://arxiv.org/abs/1708.02002) is a loss function designed to address class imbalance in tasks like object detection by focusing more on hard-to-classify examples. It modifies the standard cross-entropy loss by adding a scaling factor that reduces the loss contribution from well-classified examples, allowing the model to learn better from difficult cases.

This loss function was implemented for the Logistic Regression model and the Feed Forwar NN  giving better results than the ML models from Skicit-Learn.

## Models
The models being used are from the Skicit Learn library and programmed with Pytorch.
- Logistic Regression
- SGDClassifier
- C-Support Vector Classification.
- Logistic Regression + Focal Loss
- Feed Forward Neural Network




