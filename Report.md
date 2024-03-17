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

   During pre-processing, some of these features were binned, to reduce the amount of categories.

- Two columns were removed from the input data: EIN and NAME. These were used to identify the organisations and were not used as targets or features. 

### Compiling, Training, and Evaluating the Model
- **Model architecture**: the model was initiated with an input and output layer, as well as 2 hidden layers, with 80 and 30 neurons each. 


![alt text](model1.png)
Fig. 1 - Model architecture

- **Activation functions**: the hidden layers used a 'ReLU' activation function - a good starting point given its faster learning. The output layer used a 'Sygmoid' activation function, which is ideal for binary classification
- **Model performance**: this model came short of the target performance, with an accuracy of 73%

![alt text](model1_acc.png)
Fig. 2 - Model accuracy

- **Model optimization**: in order to optimise the model, the following approaches were taken:
    - *Data preprocessing*: different cut-off values for the binned features (classification and application type) were trialed. As amount of funding requested was the feature with the most unique values, in one iteration of the model, this features was binned into 4 categories: funding bids under 10.000, under 100.000, under 1.000.000 and over 1.000.000
    - *Model architecture*: an additional hidden layer was added, the number of neurons in each layer changed (to 90, 60, and 30). In one attempt, the activation function of the hidden layers was changed to 'Tahn'

    
    - *Model training*: different epochs were trialed to train the model
    - *Auto optimisation*: in an attempt to understand whether there were any changes to the model's parameters missed, kera-tuner was used to assess a potential best model. 

    ![alt text](image-3.png)
    Fig. 3 - Model accuracy after auto-optimization

None of these optimisation approaches (including using kera-tuner) reached the target performance. 

### Summary
This deep learning model fell short from the target performance, with an accuracy of only 73%. The model's accuracy remained consistently under the target performance even after different optimisation attempts. 

In the next steps, Alphabet Soup might want to consider the use of a random forest model. Random forests can map non-linear relationships in data, which would likely be more appropriate for the dataset at hand. Moreover, tree-based algorithms, like random forests, would allow Alphabet Soup to trace how the model reached any decisions about funding, which could provide valuable insight to the foundation.