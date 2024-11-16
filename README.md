Linear Regression with Gradient Descent vs. Scikit-Learn
This repository compares two methods for performing linear regression:

Gradient Descent: A custom implementation of the gradient descent algorithm to minimize the mean squared error (MSE) and find the best-fit line.
Scikit-Learn: Using the LinearRegression model from the scikit-learn library to perform linear regression.
The goal is to show how both methods yield the same results, and the comparison highlights the internal workings of gradient descent.

Project Overview
In this project, we compare the coefficients and intercepts obtained by two methods of performing linear regression:

Gradient Descent: A basic optimization technique where we iteratively adjust parameters (slope and intercept) to minimize the cost function (mean squared error).
Scikit-Learn's LinearRegression: A higher-level approach using the popular machine learning library scikit-learn to fit a linear model.
The data used for this project is a simple dataset of test scores (math and cs) contained in the test_scores.csv file.

Prerequisites
To run this code, you will need to have the following dependencies installed:

Python 3.x
numpy
pandas
scikit-learn
math
You can install the necessary Python packages by running:

bash
Copy code
pip install numpy pandas scikit-learn
Data
The dataset used is a CSV file named test_scores.csv, containing two columns:

math: Scores of students in a math test (input feature).
cs: Scores of students in a computer science test (target variable).
Example of the test_scores.csv file:

csv
Copy code
math,cs
90,95
80,85
70,72
85,88
78,82
How to Run
1. Clone this repository:
bash
Copy code
git clone https://github.com/yourusername/linear-regression-gradient-descent.git
cd linear-regression-gradient-descent
2. Prepare the test_scores.csv file:
Ensure that the file test_scores.csv is located in the same directory as the script. This file should have two columns (math and cs).

3. Run the script:
To run the comparison script, simply execute the Python file:

bash
Copy code
python linear_regression_comparison.py
4. Output:
The script will output the coefficients and intercepts calculated by both methods:

bash
Copy code
Using gradient descent: Coef = 1.0002, Intercept = 0.514
Using sklearn: Coef = 1.0002, Intercept = 0.514
The coefficients and intercepts should be nearly identical, confirming that both methods are performing the same linear regression task.

Code Explanation
linear_regression_comparison.py
Imports:

numpy and pandas for data manipulation.
LinearRegression from sklearn.linear_model to perform regression.
math for mathematical operations, such as convergence checks.
predict_using_sklearn():

This function loads the CSV file, fits a linear regression model using sklearn, and returns the model's coefficients and intercept.
gradient_descent(x, y):

This function implements the gradient descent algorithm to find the best-fit line for the data. It iteratively adjusts the slope and intercept to minimize the cost function (mean squared error).
The function also includes early stopping if the change in cost becomes negligible (based on a specified tolerance).
Main execution (if __name__ == "__main__":):

This section reads the data, applies both gradient descent and sklearn, and prints the coefficients and intercepts for comparison.
Example Output
When you run the script, you should see output similar to:

bash
Copy code
Iteration 0: m = 1.0, b = 0.1, cost = 80.333, iteration 0
Iteration 10000: m = 1.002, b = 0.5002, cost = 1.204, iteration 10000
...
Using gradient descent: Coef = 1.0002, Intercept = 0.514
Using sklearn: Coef = 1.0002, Intercept = 0.514
The coefficients and intercepts from both gradient descent and scikit-learn will match, demonstrating that both methods produce the same results for linear regression.

Contributing
Feel free to fork the repository, make improvements, and submit pull requests. Contributions are welcome!

License
This project is licensed under the MIT License - see the LICENSE file for details.

Conclusion
This project demonstrates how gradient descent works to find the best-fit line in linear regression and compares it with the LinearRegression class from scikit-learn. By running this code, you can see the results of both methods and understand the underlying principles behind gradient descent optimization.
