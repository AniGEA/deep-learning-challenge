# Report on the Neural network and deep learning model

## Background
The nonprofit foundation Alphabet Soup aims to enhance its funding process by identifying applicants with the highest likelihood of success. To achieve this, we developed a binary classification model using machine learning and neural networks. The dataset provided contains over 34,000 entries of organizations that have applied for funding from Alphabet Soup. Each entry includes various metadata columns, such as:

- EIN and NAME: Identification columns
- APPLICATION_TYPE: Type of Alphabet Soup application
- AFFILIATION: Sector of industry affiliation
- CLASSIFICATION: Government organization classification
- USE_CASE: Purpose of funding
- ORGANIZATION: Type of organization
- STATUS: Active status of the application
- INCOME_AMT: Income classification
- SPECIAL_CONSIDERATIONS: Special considerations for the application
- ASK_AMT: Amount of funding requested
- IS_SUCCESSFUL: Indicator of whether the funding was used effectively


## Overview of the Analysis
The objective of this analysis was to develop a deep learning model capable of predicting the success of funding applications. The focus was on preprocessing the data, building and training a neural network, and evaluating its performance to ensure it meets the desired accuracy benchmark.

## Results
### Data Preprocessing
+ **Target Variable(s):** The target variable is IS_SUCCESSFUL, which indicates whether an application was successful (1) or not (0).
+ **Feature Variable(s):** Features include all columns except IS_SUCCESSFUL, specifically after dropping non-beneficial columns like EIN and NAME.
+ **Variables to Remove:** Columns such as EIN and NAME were removed as they are identifiers and not useful for predictive modeling.




## Compiling, Training, and Evaluating the Model
Different models were applied to achieve the desired accuracy percentage; however, the highest achieved was 73%. Despite adjustments, the model's accuracy improved slightly but remained below the target of 75%.

+ **First Try**

Hidden Layers: 2
First Hidden Layer: 80 units, ReLU activation
Second Hidden Layer: 30 units, ReLU activation
Output Layer: 1 unit, sigmoid activation
Accuracy: 73.14%

The deep neural network model, with its sequential architecture featuring two hidden layers and an output layer, achieved an accuracy of 73.14% on the test dataset. While the model performed reasonably well, there remains potential for further optimization to reach the target accuracy.

+ **Second Try**

Hidden Layers: 3
First Hidden Layer: 80 units, ReLU activation
Second Hidden Layer: 30 units, ReLU activation
Third Hidden Layer: 30 units, sigmoid activation
Output Layer: 1 unit, sigmoid activation
Accuracy: 72.79%

In the second attempt, the model was further optimized with three hidden layers. Despite improvements, the accuracy achieved was 72.79%, slightly lower than the previous attempt. Further optimization is needed to meet the 75% target.

+ **Third Try**
Model Configuration:

Hidden Layers: 3
First Hidden Layer: 110 units, ReLU activation
Second Hidden Layer: 45 units, ReLU activation
Third Hidden Layer: 76 units, sigmoid activation
Output Layer: 1 unit, sigmoid activation
Accuracy: 72.85%

After the third attempt, the model achieved an accuracy of 73%. This represented an improvement over previous iterations but still fell short of the 75% target. Further enhancements are necessary to achieve higher accuracy.

+ **Fourth Try**
Model: Random Forest
Accuracy: 72.1%

The Random Forest model was evaluated and achieved an accuracy of 72.1%. The confusion matrix revealed that the model correctly predicted 2,236 instances of class 0 and 2,709 instances of class 1, while misclassifying 1,023 instances of class 0 as class 1 and 892 instances of class 1 as class 0. The classification report showed a precision of 0.71 and recall of 0.69 for class 0, and a precision of 0.73 and recall of 0.75 for class 1. The F1-scores were 0.70 for class 0 and 0.74 for class 1. Despite a balanced performance, further optimization is required to improve accuracy.

+ **Fifth Try**
Model: Logistic Regression
Accuracy: 72.2%

The Logistic Regression model, trained with a maximum of 1000 iterations and a fixed random seed of 75, achieved an accuracy of 72.2%. The confusion matrix showed that the model correctly predicted 2,711 instances of class 0 and 3,477 instances of class 1, while misclassifying 1,282 instances of class 0 as class 1 and 1,105 instances of class 1 as class 0. The classification report detailed a precision of 0.71 and recall of 0.68 for class 0, and a precision of 0.73 and recall of 0.76 for class 1. The F1-scores were 0.69 for class 0 and 0.74 for class 1. With macro and weighted averages around 0.72, the model demonstrated balanced performance, but further optimization may be necessary to achieve higher performance benchmarks.
