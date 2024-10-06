# MLP Weather Prediction

## Project Overview

This project was developed as part of the **Artificial Intelligence Degree** at **Universitat Politècnica de Catalunya**. The objective is to explore the application of **machine learning** to weather data for the task of **rain prediction**. The project uses a **Multilayer Perceptron (MLP)** neural network to predict whether it will rain the next day based on various weather features from a dataset that spans over 10 years of meteorological data in Australia.

## Dataset

The dataset contains 16 variables, including temperature, humidity, wind speed, cloud cover, and other meteorological indicators. The target variable, **RainTomorrow**, is categorical and represents whether or not it will rain the next day.

Data preprocessing included:
- **Recoding** categorical variables (e.g., converting cities to regions).
- **Handling outliers** by removing extreme and unlikely values.
- **Imputing missing values** using the K-Nearest Neighbors (KNN) method.
- **Balancing** and **normalizing** the data to ensure proper model performance.

## Exploratory Data Analysis (EDA)

The dataset underwent **univariate** and **bivariate** analysis:
- **Univariate analysis** examined each variable’s distribution using histograms and summary statistics.
- **Bivariate analysis** involved using bar plots and box plots to observe the relationships between individual variables and the target.

## Model Development

Two main models were tested:

1. **Logistic Regression**: A linear model used as the baseline. Regularization techniques (L1 and L2) were applied to improve its performance.
   
2. **Multilayer Perceptron (MLP)**: The core of the project, trained iteratively to optimize performance. The following key experiments were performed:
   - Different **activation functions** (softmax, relu, tanh).
   - **Optimizer** (Adam and SGD).
   - **Regularization** techniques (L1, L2).
   - **Dropout** to prevent overfitting.
   - Multiple architectures with 1 to 3 hidden layers.

### Final Model

The best-performing model used 2 hidden layers, L2 regularization, and dropout. This model generalizes well and achieves a high **F1 score** of 0.813, outperforming the baseline logistic regression model.

Below is a visualization of the training and validation loss, along with the accuracy of the final model over 200 epochs:
![image](https://github.com/user-attachments/assets/b13e8b76-e3ca-4b90-b130-caea0e01c4a8)

Additionally, here is the **confusion matrix** for the final model:
![image](https://github.com/user-attachments/assets/6e4bb4cd-a11d-4869-a7b5-e72289004fed)

## Results

The following table summarizes the performance of the different models:

| Model                | Accuracy | F1 Score | Recall | Precision |
|----------------------|----------|----------|--------|-----------|
| Logistic Regression   | 0.803    | 0.800    | 0.791  | 0.809     |
| MLP (Final)           | 0.813    | 0.813    | 0.813  | 0.813     |

## Conclusion

The project demonstrated that a **Multilayer Perceptron** can outperform logistic regression for rain prediction. The final model showed an improvement in generalization and perf
