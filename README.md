# First-Neural-Network
This project is a simple neural network. It has a iPython file that has the entire code. 
This project requires Python3, Matplotlib and Pandas


# About the model and predictions
The model is predicting good when I tune the paramters. I tried the following to tune my parameters.
I increased the number of epochs and observed that at certain point the error plot was becoming flat for both training and validation errors. It wouldnt change no matter how much increment I do. I stopped at 1500 epochs where I was getting the most optimum plot
I changed the learning rate and observed that error loss increased for higher rates and started getting lower when decreasing. I decresed in the steps of 1/3 everytime. After decreasing to certain limit I observed no changes in the validation and training errors hence I stopped at 0.01
I increased the number of hidden units and found that the model was fitting better with the increment. each time I doubled the hidden units I saw it getting better results. However when I increased it to equal to number of input units the error loss reduced a lot but there were lot of fluctuations in the values and it seemed to have overfit the data. I stopped at 8 hidden units which seemed to fit the data properly with lesser fluctuations.
After finding the hidden units I again went back and tuned epochs and finally here are the parameters that fit this model well:

```epochs = 1600
learning_rate = 0.01
hidden_nodes = 10```

There is one observation I found from the predictions plot is a huge variance in the records towards the last days of the month. This could possibly be due to lesser training data used to train the network. We just used 20 days of training data which is not sufficient to get the complete picture. when we use the data for the entire year the predictions will get right. General rule of thumb says use 60% of data for training, 20% for cross validation and 20% for testing.
