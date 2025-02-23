# Neural Network and ML Algorithm Comparison Project

## Project Overview

Rwanda heavily relies on agriculture, with bananas being a primary staple crop. However, Banana Xanthomonas Wilt (BXW) poses a severe threat to banana production, causing up to 100% yield loss in heavily infected areas, leading to economic hardship for farmers. The disease spreads rapidly through infected plant material, insect vectors, and contaminated tools, making it a pressing concern for Rwanda's agriculture sector. This project aims to develop an ML-based model to detect BXW in banana crops using image recognition, enabling early and accurate disease diagnosis.  

## Dataset

The dataset used in this project is from Roboflow (www.roboflow.com) and contains images of banana leaves labeled as either healthy or infected with BXW. The dataset is already split into training, validation, and test sets, with each folder containing an annotations CSV file and an images folder.

## Discussion of Findings

### Neural Network Training Instances

| Training Instance | Optimizer Used | Regularizer Used | Epochs | Early Stopping | Number of Layers | Learning Rate | Accuracy | Loss | F1-score | Precision | Recall |
|-------------------|----------------|------------------|--------|----------------|------------------|---------------|----------|------|----------|-----------|--------|
| Instance 1        | Default        | None             | 10     | No             | 6                | Default       |          |      |          |           |        |
| Instance 2        | Adam           | L2               | 10     | Yes            | 6                | 0.001         |          |      |          |           |        |
| Instance 3        | RMSprop        | L1               | 10     | No             | 6                | 0.0001        |          |      |          |           |        |
| Instance 4        | Adam           | L1 + L2          | 10     | Yes            | 6                | 0.01          |          |      |          |           |        |
| Instance 5        | RMSprop        | None             | 10     | Yes            | 6                | 0.001         |          |      |          |           |        |

### Summary

#### Best Combination

- The combination that worked best was Instance X (e.g., Instance 2) with the following configuration: 
  - Optimizer: Adam
  - Regularizer: L2
  - Early Stopping: Yes
  - Learning Rate: 0.001
  - Accuracy: X%
  - F1-score: X
  - Precision: X
  - Recall: X

#### Comparison of ML Algorithm and Neural Network

- The neural network model with optimized hyperparameters outperformed the classical ML algorithm in terms of accuracy and F1-score.
- The ML algorithm utilized for comparison was [insert ML algorithm name, e.g., Logistic Regression] with the following hyperparameters:
  - Regularization: L2
  - C: 1.0
  - Solver: lbfgs
  - Accuracy: X%
  - F1-score: X
  - Precision: X
  - Recall: X

### Video Presentation

The video covers the discussion of the table above, the libraries used, and the comparison of the neural network and ML algorithm.


### Instructions for Running the Notebook

1. Clone the repository to your local machine.
2. Install the required dependencies.
3. Open `notebook.ipynb` in Jupyter Notebook or any compatible environment.
4. Follow the instructions in the notebook to run the code and load the best saved model.
5. Use the provided code cells to make predictions on new data.

Thank you for reviewing this project. If you have any questions or feedback, please feel free to reach out!

