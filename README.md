# Logistic Regression with Shifted Clusters

## Project Overview

In this project, I explored the effect of shifting clusters in a dataset on the parameters of a logistic regression model. The goal was to understand how the separation between two classes influences the decision boundary, model parameters, and logistic loss. This project involved generating datasets with varying shift distances between clusters, fitting a logistic regression model, and analyzing how the model's parameters evolve as the shift distance increases.

## Key Features

### 1. **Cluster Generation and Logistic Regression**

- **Dataset Generation:**
  The project begins by generating synthetic datasets with two classes. One of the classes (the second cluster) is shifted along both the x-axis and y-axis by a user-specified distance, simulating different levels of separation between the clusters.
  
- **Fitting Logistic Regression:**
  A logistic regression model is fitted to each generated dataset, and the intercept (β₀) and coefficients (β₁, β₂) are extracted for each shift distance. These parameters define the decision boundary between the two classes.

- **Logistic Loss Calculation:**
  The model's **logistic loss** (cross-entropy loss) is computed for each shift distance, reflecting how well the model is able to classify the data points. A lower logistic loss indicates a better fit of the model to the data.

### 2. **Visualization and Analysis**

- **Data Visualization:**
  Each generated dataset is visualized with different colors for each class. The decision boundary is plotted using the extracted parameters (β₀, β₁, β₂), providing a clear visual separation between the two classes.

- **Parameter and Loss Analysis:**
  As the shift distance between clusters increases, the project tracks how the model parameters change. This includes the intercept (β₀), coefficients (β₁, β₂), and the slope of the decision boundary. Additionally, the logistic loss is plotted to observe how it decreases with larger shifts, indicating improved classification accuracy.

- **Margin Width Analysis:**
  The margin width, which represents the distance between the decision boundary and the nearest data points from each class, is computed for each dataset and plotted against the shift distance.

### 3. **Interactive Web Application**

After implementing the core logistic regression functionality, I integrated the project into an interactive Flask-based web application that allows users to experiment with various shift distances and visualize the results in real time.

#### **User Input:**
- The user specifies the **lower bound**, **upper bound**, and **number of steps** for the shift distance, allowing them to control the range and granularity of the shifts.
  
- The application generates the datasets, fits logistic regression models, and displays:
  - A **scatter plot** of the two classes.
  - The **decision boundary** for each dataset.
  - **Logistic loss** for each model at different shift distances.
  - **Parameter estimates** (β₀, β₁, β₂) and the **margin width**.

#### **Interactive Module:**
To run the Flask application, the user runs the following commands:
```bash
make install   # Installs necessary dependencies
make run       # Starts the Flask application
