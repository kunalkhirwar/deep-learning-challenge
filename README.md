**OVERVIEW**

The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With my knowledge of machine learning and neural networks, I used the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.
From Alphabet Soup’s business team, I had received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

**RESULTS**

- Data Preprocessing
  
  - Features of my model - 'APPLICATION_TYPE',	'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS' and 'ASK_AMT'.
  
  - Target of my model - 'IS_SUCCESSFUL'
  
  - Dropped variables - 'EIN' and 'NAME' because they are neither targets nor features.

- Compiling, Training, and Evaluating the Model
  - Description of the neural network model:
    - First Hidden Layer - Dense Layer
                         - Number of neurons - 80
                         - Activation Function - RELU (Rectified Unit Layer)
                         - Reason for choosing the activation function - returns 0 if it receives any negative input, but for any positive value x it returns that value back.
    - Second Hidden Layer - Dense Layer
                         - Number of neurons - 30
                         - Activation Function - RELU (Rectified Unit Layer)
                         - Reason for choosing the activation function - returns 0 if it receives any negative input, but for any positive value x it returns that value back.
    - Output Layer       - Dense Layer
                         - Number of neurons - 1
                         - Activation Function - Sigmoid
                         - Reason for choosing the activation function - outputs (0 or 1) can be easily interpreted as probabilities, which makes it natural for binary 
                           classification problems.

  - Target model performance achieved is 72.47%.
  - Steps taken to increase the model performance:
    - used KerasTuner to optimize the hyperparameters of the deep learning model.
    - used Principal Component Analysis (PCA) to summarize the information content in large data tables by means of a smaller set of “summary indices” that can be more 
      easily analyzed.
    - Increasing the number of values for each bin
   
**SUMMARY**
  
The deep learning model achieved a 72.47% accuracy rate in predicting funding success. While efforts like hyperparameter optimization and PCA were made to improve it, performance could still be enhanced. A recommendation is to try gradient boosting algorithms like XGBoost or LightGBM. These methods offer ensemble learning, handle nonlinear relationships efficiently, provide feature importance scores, and are computationally efficient, potentially leading to better predictions and insights into factors affecting funding success.
