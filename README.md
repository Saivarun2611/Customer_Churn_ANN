# Customer Churn Prediction

## Overview
This project aims to predict whether a customer will leave the company or not based on several parameters. An Artificial Neural Network (ANN) model with ReLU activation functions has been used for this prediction.

## Dataset
The dataset contains the following features:
- `customerID`
- `gender`
- `SeniorCitizen`
- `Partner`
- `Dependents`
- `tenure`
- `PhoneService`
- `MultipleLines`
- `InternetService`
- `OnlineSecurity`
- `OnlineBackup`
- `DeviceProtection`
- `TechSupport`
- `StreamingTV`
- `StreamingMovies`
- `Contract`
- `PaperlessBilling`
- `PaymentMethod`
- `MonthlyCharges`
- `TotalCharges`

## Model

An Artificial Neural Network (ANN) with the following structure was used:

**Input Layer**: Number of neurons = number of features \
**Hidden Layers**: 2 layers with ReLU activation \
**Output Layer**: 1 neuron with sigmoid activation (for binary classification)

## Training
The model was trained using the Adam optimizer and binary cross-entropy loss function. The dataset was split into training and testing sets, with 80% of the data used for training and 20% for testing.

## Results
The model achieved the following performance metrics:

Accuracy: 78% \
Precision: 86% \
Recall: 85% \
F1 Score: 85% 



## Model Example
 ``` python
import tensorflow as tf
from tensorflow import keras
model=keras.Sequential([
    keras.layers.Dense(20,input_shape=(26,),activation='relu'),
    keras.layers.Dense(15,activation='relu'),
    keras.layers.Dense(1,activation='sigmoid')
])
model.compile(optimizer='adam',loss='binary_crossentropy',metrics=['accuracy'])
model.fit(X_train,y_train,epochs=100)
```


## Installation
To run this project, you need to have Python installed. Clone the repository and install the required packages:

```bash
git clone https://github.com/Saivarun2611/Customer_Churn_ANN.git
cd Customer_Chrun_ANN
```

## Conclusion
This project demonstrates the use of an ANN for predicting customer churn. The model can be further improved by tuning hyperparameters, experimenting with different architectures, and incorporating additional features.


