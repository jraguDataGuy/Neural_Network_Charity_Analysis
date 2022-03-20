# Neural Network Charity Analysis
## Overview
Is there a way to predict success amongst applicants funded by Alphabet Soup? Using the data provided, we have created a neural network model to predict the success rate of applicants. We will use the 34,000 data points provided as a guide to develop our model.

## Results
### Data Pre-Processing
- Targets: Looking at our data, the column IS_SUCCESSFUL has a binary pattern indcating success/non success of the applicant. Given the binary nature, this becomes our target in the data.
- Features: Once we removed EIN and NAME columns, we can identify which columns are features. When analyzing our data, the name and EIN numbers are not pertinent in training our model. The features based on unique values are as follows:
![Features]()

### Compiling, Training, and Evaluating the Model
#### 1st Version of the Model:
- Hidden Layer 1: 80 Neurons; reLU activation
- Hidden Layer 2: 30 Neurons; reLU activation
- Output Layer: Sigmoid Activation
- We ended up with a sequential mode with 5,981 total parameters
- We trained the model with 100 Epochs
- The first iteration came back with a 62.99% Accuracy

Ultimately, our goal was to get 75% accuracy or better. The next 3 methods, we adjusted our model in an attempt to increase accuracy

#### Test 1 of the Model: Increase the Neurons
This attempt to increase the neurons who increase our complexity, but potentially increase our accuracy
- Hidden Layer 1: 100 Neurons; reLU activation (Increased from 80)
- Hidden Layer 2: 30 Neurons; reLU activation
- Output Layer: Sigmoid Activation
- We ended up with a sequential mode with 7,461 total parameters
- We trained the model with 100 Epochs
- The second iteration came back with a 63.02% Accuracy

This was a slight increase, but has not achieved our goal. 

#### Test 2 of the Model: Adding another Hidden Layer
This attempt to increase the neurons who increase our complexity, but potentially increase our accuracy
- Hidden Layer 1: 80 Neurons; reLU activation 
- Hidden Layer 2: 30 Neurons; reLU activation
- Hidden Layer 3: 5 Neurons; reLU activation
- Output Layer: Sigmoid Activation
- We ended up with a sequential mode with 6,111 total parameters
- We trained the model with 100 Epochs
- The third iteration came back with a 52.38%% Accuracy

This was a significant decrease in accuracy, firmly putting aonther hidden layer as a poor strategy to increase our accuracy.

#### Test 2 of the Model: Increase Epochs
When we increase EPOCHs, our curve potentially moves from underfitting ot optimal or overfitting. 
- Hidden Layer 1: 80 Neurons; reLU activation 
- Hidden Layer 2: 30 Neurons; reLU activation
- Output Layer: Sigmoid Activation
- We ended up with a sequential mode with 5,981 total parameters
- We trained the model with 250 Epochs
- The third iteration came back with a 61.91% Accuracy

Ultimately, this was not the desired result. If anything, it increased our curve fit, but had no effect on accuracy. 

## Summary
Ultimately, we did not achieve our goal of 75% accuracy, leaving us with a model in need of some work. A few ideas of what we can try to increase our accuracy:
- There was not an attempt to change the activation of our Hidden Layers
- A third hidden layer did not increase our accuracy. The two hidden layers seem appropriate
- I would potentially look at our neurons, as increasing them had an effect on accuracy
