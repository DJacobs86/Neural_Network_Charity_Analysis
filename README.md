# Neural_Network_Charity_Analysis
## Overview
Alphabet Soup is a "humanitarian focused charity" that lends money to just causes to promote public health, safety, and sustainability. They have asked for a model to help make efficient and meaningful investments by testing whether their past investments have proven fruitful or sour.
### Purpose
We are tasked to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

# Results
## Data Preprocessing
What variable(s) are considered the target(s) for your model? The target variable for our model is the IS_SUCCESSFUL column, which indicates whether a charity was successful in receiving donations or not.

What variable(s) are considered to be the features for your model? The features for our model are all columns except for IS_SUCCESSFUL, EIN, and NAME.

What variable(s) are neither targets nor features, and should be removed from the input data? The EIN and NAME columns were removed from the input data as they were not useful for the model.
## Training, Compling, and Evaluating the Model
For the initial neural network model, we used two hidden layers with 80 and 30 neurons respectively, and ReLU activation function. For the optimized neural network model, we used four hidden layers with 80, 30, 20, and 10 neurons respectively, and ReLU activation function. Both models used a binary crossentropy loss function and Adam optimizer, and were trained on 15 epochs. The initial model achieved an accuracy of 72.9% on the test data, while the optimized model achieved an accuracy of 72.6%. Although the optimized model did not significantly improve the accuracy, it may be able to generalize better to new data.
# Summary
After viewing the results of the model and my manually created optimization, I would recommend using an automated optimized such as the keras-tuner package. The keras-tuner package would optimally select which activation function to use, how many neurons would be in the first hidden layer, and the number of subsequent hidden layers as well as the neurons within those layers.

After creating a keras-tuner optimization function and running the training data through the tuning model, it can return the best hyperparameters and best models to use based on the parameters set in the function. We could then run the testing data against the best models to receive a model with high accuracy and low loss. It would be possible to store and rerun the model after this process.

We would need to be wary of overfitting based on training data, but dilligence and attention can help gaurd against this possibility. This method would also not help with the preparation of the input data, meaning there are some data points that could be excluded to make a more efficienct model.

