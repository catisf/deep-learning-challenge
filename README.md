# deep-learning-challenge
Challenge 21 of UoB Data Analytics bootcamp - Deep Learning

## Overview
The aim of this project was to build a binary classifier, to help the nonprofit foundation Alphabet Soup to allocate their funds more effectively, as the classifier should be able to predict which funding applicants have the best chance of succeeding in their endeavours. 

## Results
### Data processing
- The model's target variable was whether an organisation had been successful or not, after receiving funding from Alphabet Soup 
- The features used to train the model included:
    - Application type: Alphabet Soup application type
    - Affiliation: Affiliated sector of industry
    - Classification: Government organization classification
    - Use case: Use case for funding
    - Organisation: Organisation type
    - Status: Active status
    - Income amount: Income classification
    - Special considerations: Special considerations for application
    - Ask amount: Funding amount requested


### Compiling, Training, and Evaluating the Model
- **Model architecture**: the model was initiated with an input and output layer, as well as 2 hidden layers, with 80 and 30 neurons each. Hidden layers used a 'ReLU' activation function, and the output layer used a 'Sygmoid' activation function.
- **Model performance**: this model came short of the target performance, with an accuracy of 73%.
- **Model optimization**: in order to optimise the model, the several approaches were taken, including adding an extra hidden layer, changing the activation function in the hidden layers, trialing a different number of trailing epochs, and using auto-optimisation with keras-tuner. None of these optimisation approaches (including using kera-tuner) reached the target performance. 

More details on data processing, and on model compilation, training and evaluation can be found in the [full report](https://github.com/catisf/deep-learning-challenge/blob/main/Report.md). 

### Summary
This deep learning model fell short from the target performance, with an accuracy of only 73%. The model's accuracy remained consistently under the target performance even after different optimisation attempts. 

In the next steps, Alphabet Soup might want to consider the use of a random forest model. Random forests can map non-linear relationships in data, which would likely be more appropriate for the dataset at hand. Moreover, tree-based algorithms, like random forests, would allow Alphabet Soup to trace how the model reached any decisions about funding, which could provide valuable insight to the foundation.
