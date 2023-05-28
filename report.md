
Overview
In this challenge, a model is built to help selecting applicants that have a better chance of success. A nonprofit foundation, Alphabet Soup, has funded more than 34,000 organisations in the past. Using the successful and unsucessful cases from previous data, a deep learning mdoel is developed to predict an organisation will be more likely to be successful or not. The model will consider several characterisitic of organisation, such as, application type, organisation type, affiliated sector of industry etc.

Outcomes:
Data Preprocessing
In data preprocessing, we modified the columns as below:

Target variable: [IS_SUCCESSFUL]
Features variables：[APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT]
Variables removed from the dataset:[ EIN, NAME]

Compiling, Training, and Evaluating the Model

Number of layers:  two hidden layers and output layer
Number of neurons: 60, 100 and 1
Reason: the output layer always require only one neuron because there will be only one result output from the model (success or not success)
Activation functions: relu for hidden layer, sigmoid for output layer;
Reason: All the features variables are positive and the target variable is a binary variable
Steps attempt to imporve model performance:

Increased the numbers of nuerons
Increased the numbers of hidden layers
Adjusted the ratio of trainning and testing data
Creating more bins for rare occurrences in columns
Adding the number of epochs to the training regimen
Unfortunately, the model performance still not improved after all the changes

Summary
The loss and accuracy of this model are 0.551 (55%) and 0.729 (almost 73%), that doesnot satisfy the requirements because accuracy is low and loss is high. In order to improve the model, we can consider about adding the hidden layer but this can lead to over or under train the model creating more complication. Hence, I will recommend using random forrest or decision tree to solve this classification problem as it can handle both both numerical and categorical data.

