# Banana Xanthomonas Wilt Detection Project

## Project Overview

Rwanda heavily relies on agriculture, with bananas being a primary staple crop. However, Banana Xanthomonas Wilt (BXW) poses a severe threat to banana production, causing up to 100% yield loss in heavily infected areas, leading to economic hardship for farmers. The disease spreads rapidly through infected plant material, insect vectors, and contaminated tools, making it a pressing concern for Rwanda's agriculture sector. This project aims to develop an ML-based model to detect BXW in banana crops using image recognition, enabling early and accurate disease diagnosis.  

## Dataset

The dataset used in this project is from Roboflow (www.roboflow.com) and contains images of banana leaves labeled as either healthy or infected with BXW. The dataset is already split into training, validation, and test sets, with each folder containing an annotations CSV file and an images folder.

## Discussion of Findings

### Neural Network Training Instances


| Training Instance                        | Optimizer Used | Regularizer Used | Epochs | Early Stopping | Number of Layers | Learning Rate | Accuracy | F1-score  | Precision | Recall |
|------------------------------------------|----------------|------------------|--------|----------------|------------------|---------------|----------|-----------|-----------|--------|
| Instance 1                               | None           | None             | 10     | No             | 8                | Default       |          |           |           |        |
| Instance 2                               | Adam           | None             | 10     | Yes            | 9                | 0.001         | 0.97     | 0.97      | 0.97      | 0.97   |
| Instance 3                               | RMSprop        | L2               | 10     | Yes            | 8                | 0.001         | 0.76     | 0.69/0.80 | 1.00/0.67 | 0.53/1.00 |
| Instance 4                               | SGD            | L1               | 10     | No             | 8                | 0.0001        | 0.97     | 0.97      | 0.97      | 0.97   |
| Instance 5                               | ML Algorithm-Logistic Regression |              |        |                |                  |               | 0.99     | 0.99      | 0.99      | 0.99   |

### Summary

#### Best Combination

The combination that worked best was Instance 2 and 4, which performed equally well. Both instances achieved an accuracy of 0.97, and they excelled in F1-score, precision, and recall metrics.

Instance 2 used the Adam optimizer with a learning rate of 0.001, no regularization, and early stopping enabled. This combination of optimizer and learning rate proved effective in achieving high performance.

Instance 4 used the SGD optimizer with L1 regularization and a lower learning rate of 0.0001. Despite the lower learning rate, the model managed to achieve excellent performance, showcasing the benefit of regularization.

#### Comparison of ML Algorithm and Neural Network

- The ML algorithm (Linear Regression) outperformed the neural network models in terms of accuracy and F1-score, achieving a perfect score of 0.99 in all metrics.
- The ML algorithm utilized for comparison was Logistic Regression with the following hyperparameters:
  - Regularization: None
  - Solver: lbfgs
  - Maximum Iterations: 1000
- The linear regression model's ability to achieve such high performance highlights its effectiveness in this particular task. Meanwhile, the neural network models, while powerful, did not reach the same level of accuracy and F1-score as the linear regression model.

### Video Presentation

The video covers the discussion of the table above, the libraries used, and the comparison of the neural network and ML algorithm. 


### Instructions for Running the Notebook

1. Clone the repository to your local machine.
2. Install the required dependencies.
3. Open the notebook in Jupyter Notebook or any compatible environment.
4. Follow the instructions in the notebook to run the code and navigate to the /saved_models directory to load the models.
5. Use the provided code cells to make predictions on new data.

Thank you for reviewing this project!
