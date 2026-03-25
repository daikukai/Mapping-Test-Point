 Mapping-Test-Point: Least Squares Optimization & Function Selection

This repository contains a Python-based implementation for selecting ideal functions from a candidate pool and mapping test data points based on minimum deviation criteria. This project was developed as part of research into the Advantages and Limitations of the Least Square Method at the International University of Applied Sciences.

Overview

The core objective of this software is to automate the identification of mathematical models that best represent a given training dataset. By utilizing the Ordinary Least Squares (OLS) method, the system:
1.  Ingests raw CSV data into a structured **SQLite** database.
2.  Analyzes 50 candidate ideal functions to find the four best fits for the training data.
3.  Maps test data points to these functions using a calculated maximum deviation threshold ($\sqrt{2} \times \text{max deviation}$).
4.  Provides statistical validation (MSE, RMSE, MAE, and R-squared) and visual diagnostics.

Key Features

- Automated Database Management: Full integration with SQLAlchemy and sqlite3 for persistent data storage.
- Robust Visualization: Automated generation of scatter plots, box plots (for outlier detection), and residual plots.
- Performance Metrics: Integrated model evaluation using scikit-learn to calculate:
  - Mean Squared Error (MSE)
  - Root Mean Squared Error (RMSE)
  - R-squared (R2) Score
- Validation Logic: Implements mathematical constraints to ensure test points are only mapped when they fall within acceptable deviation ranges.

Installation

Prerequisites
- Python 3.8 or higher
- pip package manager

Setup
Clone the repository and install the required dependencies:

System Architecture

DataProcessor: Handles table creation and CSV-to-SQL data migration.

visulization: Manages the graphical output of data distributions and model performance.

calculate_deviations: Executes the OLS-based logic to pair training sets with ideal functions.

mapping_points: Maps the test dataset to the chosen functions based on criteria defined in the research.

Mathematical Context: The selection logic is based on minimizing the sum of squared residuals.

git clone [https://github.com/daikukai/Mapping-Test-Point.git](https://github.com/daikukai/Mapping-Test-Point.git)
cd Mapping-Test-Point
pip install pandas numpy sqlalchemy matplotlib seaborn scikit-learn statsmodels bokeh

The mapping criterion for test points uses a threshold of: Threshold = sqrt(2) times Max Deviation

License
Distributed under the MIT License. See LICENSE for more information.

Acknowledgements
Developed as part of academic research at the International University of Applied Sciences.

