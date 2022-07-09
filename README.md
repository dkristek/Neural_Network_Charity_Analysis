# Neural_Network_Charity_Analysis
### Overview
The objective of this project was to build a neural network for a philantrhopic foundation to predict whether a given charity will be successful if the foundation donates to the charity.

### Results
#### Data Preprocessing
- The dataframe's columns can be seen in the image below
![List of dataframe columns](https://github.com/dkristek/Neural_Network_Charity_Analysis/blob/main/images/df_columns.png)
- The target variable of the model is the "IS_SUCCESSFUL" column
- EIN and NAME are unneeded and were therefore dropped
- The features are the remaining columns ('APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT',
'SPECIAL_CONSIDERATIONS', 'ASK_AMT')

#### Modelling
- The original model's code is shown below
![Model](https://github.com/dkristek/Neural_Network_Charity_Analysis/blob/main/images/nodes_layers.png)
- 1 hidden layer and 30 nodes were chosen. These numbers were chosen based on suggestions from [this StackExchange post](https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw) There were 43 input nodes and 1 output node so 30 hidden layer nodes were chosen as it was between the two numbers.
- The results of the original model can be seen below
![Model Results](https://github.com/dkristek/Neural_Network_Charity_Analysis/blob/main/images/og_model.png)
- The target accuracy was 75% but this was not achieved as the accuracy was only 73.01%
- Several different variations of the model were tested in an attempt to reach 75% accuracy. Activation functions were changed, nodes and hidden layer amounts were adjusted, and feature selection was adjusted. For a closer look at the changes made checkout the AlphabetSoupCharity_Optimization.ipynb
- In the end none of these were able to achieve an accuracy rate of 75%. The highest rate obtained was 73.07%

#### Summary
The overall results of the neural network failed to meet the 75% accuracy objective. However, 73% accuracy was obtained which is not excellent accuracy but it is decently accurate. One suggestion to improve accuracy would be to use a different machine learning model. As this is a classification problem, a supervised learning model would be appropriate. There are two classes in this data set, Successful or Not Successful, and the results are rather balanced across the two classes. Therefore, I would choose a decision tree ensemble or random forest model to solve this classification problem.
