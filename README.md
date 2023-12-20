# Breast Cancer Classification

## Introduction
Breast cancer is a significant global health concern, affecting millions of lives each year. Early detection plays a crucial role in improving patient outcomes and reducing mortality rates. In this context, we present a deep learning-based approach for breast cancer classification using featured dataset.

## Code Dependencies:
Install required imported libraries in your runtime environment
```
numpy
pandas
matplotlib
```

## Execution
To run the code, type
```
python B_Cancer_DL.py
```
## Objective
The primary objectives of this project are as follows:
1) Early Detection: Develop a deep neural network to accurately classify histopathological images as benign or malignant, enabling early detection of breast cancer.
2) Automation: Provide an automated and efficient tool that can assist pathologists in diagnosing breast cancer, thereby reducing the time and effort required for manual analysis.
3) Performance Evaluation: Implement metrics such as accuracy, precision, recall, and the confusion matrix to comprehensively evaluate the model's performance.

## Dataset
- The data is structured in CSV files, with "cancer_data.csv" containing feature values and "cancer_data_y.csv" containing corresponding labels.
- Data preprocessing involves steps such as normalization and handling missing values to ensure the data is suitable for model training.
- The dataset is split into training and testing sets, enabling the evaluation of the model's performance on unseen data.
- Each sample in the dataset is labeled as either malignant (1) or benign (0), indicating the nature of the tumor.

## Data Preprocessing
- The code uses Pandas to read CSV files ("cancer_data.csv" and "cancer_data_y.csv") containing the features and labels, respectively.
- Neural network parameters are initialized using the ‘initialize_parameters_deep’ function.
- The forward propagation steps are implemented in the ‘L_model_forward’ function, which performs [LINEAR -> RELU]*(L-1) -> LINEAR -> SIGMOID operations.
- The cost is computed using the ‘compute_cost’ function, which calculates the binary cross-entropy loss.
- Backward propagation is implemented in the ‘L_model_backward’ function, which computes gradients for each layer.
- The ‘update_params’ function updates the parameters using gradient descent.
- The model is trained for a specified number of iterations, and the training and test accuracy, as well as other metrics, are printed.

## Neural Network Architecture
- I defined the architecture of neural network by the variable ‘dims’.
- The input layer has 30 neurons (features), as indicated by dims[0].
- There are two hidden layers with 50 and 20 neurons, respectively (specified by ‘dims[1]’ and ‘dims[2]’ ).
- The output layer has 1 neuron, corresponding to binary classification (specified by ‘dims[3]’ ).
- Input Layer: 30 neurons
- Hidden Layer 1: 50 neurons (using ReLU activation)
- Hidden Layer 2: 20 neurons (using ReLU activation)
- Output Layer: 1 neuron (using Sigmoid activation)

## dims = [30, 30, 20, 11, 1]
dims = [30, 50, 20, 11, 1]

![image](https://github.com/harika136/edunetproject/assets/104025509/15702502-088a-4364-95dd-8f584ce62ff8)

## Training, Testing and Confusion Matrix
Accuracy on training set: 91.63%

On Train set:
- True Positive:   153
- True Negative:   230
- False Negative:   23
- False Positive:   12
- True Positive Rate / Recall: 86.93%
- Precision: 92.73%
- False Positive Rate / Fallout: 4.96%

Accuracy on test set: 91.28%

On Test set:
- True Positive:   30
- True Negative:   106
- False Negative:   5
- False Positive:   8
- True Positive Rate / Recall: 85.71%
- Precision: 78.95%
- False Positive Rate / Fallout: 7.02%

# Output

![B_Cancer_DL py - Edunet - Visual Studio Code 20-12-2023 16_41_27](https://github.com/harika136/edunetproject/assets/104025509/c2a6be59-2220-4333-a555-b85d476ca30f)

## Model Performance

![lr](https://github.com/harika136/edunetproject/assets/104025509/b86298ff-4371-424b-b63b-c5942e9050e0)

## Conclusion
The project concludes with an analysis of the model's performance on both training and test datasets. Metrics such as accuracy, precision, recall, and the confusion matrix contribute to a comprehensive understanding of the model's effectiveness.
