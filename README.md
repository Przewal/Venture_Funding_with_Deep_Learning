# Venture Funding with Deep Learning

## Overview:
The projects contains efforts to optimize a neural network model for binary classification of Alphabet Soup–funded startups. The primary aim was to predict whether a startup would be successful based on various features within the dataset.

## Model Development Steps:

### Data Preparation:
* Read and preprocess the data from "applicants_data.csv".
* Dropped irrelevant columns: "EIN" and "NAME".
* Encoded categorical variables using OneHotEncoder.
* Combined encoded variables with numerical features.
* Split the data into features (X) and target (y) datasets.
* Performed standard scaling on the features.

### Baseline Neural Network Model:
* Created a two-layer deep neural network using TensorFlow's Keras.
* Utilized ReLU activation function for hidden layers.
Compiled the model with 'binary_crossentropy' loss, 'adam' optimizer, and accuracy metric.
* Fit the model with 50 epochs and evaluated on the test set.
* Saved the model as 'AlphabetSoup.h5'.


### Optimization Attempts:
* __Attempt 1: Batch Normalization__
  * Increased epochs to 100 for extended training.
  * Achieved highest accuracy at 73%.
  * Model saved as 'Attempt1_BatchNorm.h5'.

* __Attempt 2: Drop Out Regularization__
  * Increased epochs to 100 for extended training.
  * Achieved highest accuracy at 73%.
  * Model saved as 'Attempt1_BatchNorm.h5'.

## Conclusion:
After attempting Batch Normalization and Drop Out Regularization with an increased epoch of 100 (initially 50 epochs), the highest accuracy achieved remained at 73%. This accuracy signifies that 1 out of 4 times, the model incorrectly classified the outcome, predicting a success when the company fails (false positive) or failing to fund a company that would have been a success (false negative).

Despite these adjustments and extended training epochs, the model's performance plateaued, suggesting that the available data might not contain additional discernible patterns or information that could be effectively extracted through further alterations to the neural network architecture or training duration.