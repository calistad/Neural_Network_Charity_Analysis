# Neural Network Charity Analysis

## Overview 

We will create a binary classifier with machine learning and neural networks to predict whether applicants will be successful if funded by Alphabet Soup. 

For this analysis, we have a dataset containing various measures on 34,000 organizations that have been funded by Alphabet Soup.

## Results

### Data Preprocessing

![Screen Shot 2021-12-26 at 10 18 42 PM](https://user-images.githubusercontent.com/88747464/147430912-add59fdd-85e0-418a-b3b9-5f17bef3deac.png)

#### Target Variable
- IS_SUCCESSFUL column

#### Features Variables
- Every column except for IS_SUCCESSFUL

#### Removed Variables
- EIN and NAME columns

### Compiling, Training, and Evaluating the Model

Since this is a large dataset, we select

![Screen Shot 2021-12-26 at 10 20 09 PM](https://user-images.githubusercontent.com/88747464/147431038-3c08e1b2-8a61-4b83-99b9-817a7edff020.png)

- 2 layers
- First layer: 80 neurons, Second layer: 30 neurons
- Input activation functions: RELU 
- Output activation functions: Sigmoid

![Screen Shot 2021-12-26 at 10 20 01 PM](https://user-images.githubusercontent.com/88747464/147431030-c988fa29-7062-4f0e-8315-feba034bb194.png)

However, the loss 55.6%, and the accuracy is 72.4%, which does not meet our expectations.

![Screen Shot 2021-12-26 at 10 20 35 PM](https://user-images.githubusercontent.com/88747464/147431056-ec71e472-17d1-4a31-8ad5-0db07d79a8bf.png)

### Optimization

We optimize the model to try to increase the model performance by:

- Creating more bins for rare occurrences in columns. (ASK_AMT)

![Screen Shot 2021-12-26 at 10 22 09 PM](https://user-images.githubusercontent.com/88747464/147431127-b26af28d-ba7c-4524-b7f1-251af311adac.png)

- Increasing the number of values for each bin. (APPLICATION_TYPE)

![Screen Shot 2021-12-26 at 10 22 54 PM](https://user-images.githubusercontent.com/88747464/147431160-4347266f-02a9-4189-8d79-c026904be976.png)

- Added more neurons to each hidden layer.
- Added one more hidden layer.

![Screen Shot 2021-12-26 at 10 24 31 PM](https://user-images.githubusercontent.com/88747464/147431277-db0f5d9d-6bff-48e2-8c80-5774078831b3.png)

## Summary

Overall, the model ended up with an accuracy score of 72.7% after optimization. 

![Screen Shot 2021-12-26 at 10 25 02 PM](https://user-images.githubusercontent.com/88747464/147431301-81ba409d-385c-4c0b-be0e-9e6fa4c3e1a7.png)

Although the accuracy of model performance does not improve, it’s still worth attempting. 

Additionally, we could optimize our neural network by removing more features, since the dataset may be too complex. 

Furthermore, we could have used the Random Forest classifiers. The random forest models have faster performance than neural networks and could have avoided the data from being overfitted.
