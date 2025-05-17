# deep-learning-challenge
Module 21 Challenge Files

### Overview
The purpose of this is to create a model to assist the nonprofit Alphabet Soup seelct applications for funding. The model is based on data provided by Aphabet Soup and uses a neural network model to create a predictive analysis. The model uses a target value and creates two datasets, a training and test set. The results are compared to determine the most successfully optimizated model. 


### Setup
Datasource
 - Target: The target value is the "Is_Successful" column. 
 - Other values are Application Type, Affiliation, Classification, Use Case, Organization, Status, Income Amt, Special Considerations, and Ask Amount. 

### Results
The model was optimized by adjusting the number of neurons per layer, removing the column "SPECIAL_CIRCUMSTANCES", and adjusting the number of bins for small values in the CLASSIFICATION and APPLICATION_TYPE columns. The model was run 7 times making adjustments each time as shown below. The best results in all 7 trials was accuracy of 72.48% and loss of 55.27%. No attempt hit the target value of 75% accuracy. The graphs below show the accuracy and loss for attempt 7. 

![8th Model Accuracy] (/deep-learning-challenge/21-Neural-Networks-Deep-Learning/accuracy_plot.png)

**1st Model**

Setup:
 - 2 Hidden Layers, 50 & 20 Neurons
 - 1 output layer, sigmoid
 - 100 Epochs

Results:
 - accuracy: 0.7248
 - loss: 0.5527
 - The high loss rate could indicate overfitting the model. Try again with fewer neurons per hidden layer. 

**2nd Model**

Setup:
 - 2 Hidden Layers, 30 & 10 Neurons, activation relu
 - 1 output layer, sigmoid
 - 100 Epochs
 - 
Results:
 - accuracy: 0.7264
 - loss: 0.5535
 - The results are almost exactly the same. Try again adding another hidden layer of 5 neurons. 

**3rd Model**

Setup:
 - 3 Hidden Layers, 30, 10 & 5 Neurons, activation relu
 - 1 output layer, sigmoid
Results:

 - accuracy: 0.7238
 - loss: 0.5555
 - The results are even more loss. Try again changing the input from Relu to tanh and epochs back to 100. 

**4th Model**

Setup:
 - 3 Hidden Layers, 30, 10 & 5 Neurons, activation tanh
 - 1 output layer, sigmoid

Results:
 - accuracy: 0.7259
 - loss: 0.5520
 - The results are not much better. Try again removing the SPECIAL_CONSIDERATIONS column. 

**5th Model**

Setup:
 - 3 Hidden Layers, 30, 10 & 5 Neurons, activation tanh
 - 1 output layer, sigmoid

Results:
 - accuracy: 0.7259
 - loss: 0.5536
 - The results are almost exactly the same. Run again with MORE neurons. Try 80 and 50, relu. 

**6th Model**

Setup:
 - 2 Hidden Layers, 80, 50, activation relu
 - 1 output layer, sigmoid

Results:
 - accuracy: 0.7263
 - loss: 0.5594
 - The results are also not great. 

**7th Model**

Setup:
 - 2 Hidden Layers, 80, 50, activation relu
 - 1 output layer, sigmoid
 - Changed APPLICATION_TYPE 'other' bin to < 700 cut off. 

Results:
 - accuracy: 0.7257
 - loss: 0.5589
 - Not a significant difference. 

