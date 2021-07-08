# Overview: 
This purpose of this project is to build a binary classifier to help a Non-Profit Organization decide which organizations and causes are reliable to be funded.

# Results: 
Using bulleted lists and images to support your answers, address the following questions.

### Data Preprocessing
* **Target Variable**: IS_SUCCESSFUL
* **Feature Variables**: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS
* **Non-beneficial Variables**: EIN, NAME, ASK_AMT

### Compiling, Training, and Evaluating the Model
* My Keras model was built with 3 layers, 130 neurons, and RELU and Sigmoid activation functions.
* The model achieved an **accuracy of 73%**, but failed to achieve the target performance of 75%
* Below improvements were implemented to optimize the model:
  *  2 RELU and 2 Sigmoid activation functions were used.
  *  The 'ASK AMT' was dropped because it had 8747 unique values, which was adding noise to the dataset.
  *  500 epochs were used to fit the model.

<p align='centre'>
<img src='https://github.com/yazhcodes/Neural_Network_Charity_Analysis/blob/main/Resources/Result.png'></img>
</p>

# Summary: 
Despite the several attempts to optimize the model, the desired 75% accuracy could not be achieved. I would recommend to bin the 'ASK AMT' column into categories and utilizing it to train the model better, instead of dropping the column altogether. Also, the dataset is too small with too many variable making the input very noisy. Either the volume of data should be expanded or more insights could be gathered about the variables to determine if any of those features could be non-benificial and just adding noise to the model. 
