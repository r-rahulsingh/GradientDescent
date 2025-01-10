# GradientDescent

![image](https://github.com/user-attachments/assets/52556c23-1cc6-42fa-ac77-46b7d39adfdd)

Find the content details on my [Medium Post](https://medium.com/@r-rahulsingh/gradient-descent-6b8b1316079c)

## How convex functionality of MSE cost function provides an ideal landscape for optimization?

Since the MSE is convex and continuous, gradient descent will:
- Always move towards the global minimum.
- Avoid getting stuck in local minima (since they don't exist).
- Converge to the optimal solution as long as the learning rate is appropriate.

The Mean Squared Error (MSE) cost function for linear regression has a special property: it is convex. Here's a breakdown of what this means and its implications:

**Convex Function:**
Definition: A function is convex if, for any two points on the function ![image](https://github.com/user-attachments/assets/3a47ce2d-09ce-4ed5-9eb0-e6d3e04e172f) 
, the line segment joining these points lies above or on the curve of the function.

- The MSE cost function satisfies this property.
- Convexity guarantees that the function has no "valleys" or local minima. It means there is a single global minimum that gradient descent can reach if we start at any point.
- This is important for optimization because we don't have to worry about getting "stuck" in suboptimal points (local minima).

**MSE for Linear Regression:**
The MSE cost function for linear regression is:
![image](https://github.com/user-attachments/assets/8ed317df-e38d-4d93-9b52-becf7dcda907)

- Is a paraboloid in higher-dimensional space (if we visualize it for a single parameter, it looks like a "bowl").
- Has a single minimum point, where the gradient (slope) of the cost function is zero.

**Continuous Function:**
- The MSE function is continuous, meaning there are no sudden jumps or breaks in the curve.
- This makes the gradient descent algorithm stable because the gradient (or slope) changes smoothly.

**Slope Changes Gradually:**
- The derivative of the MSE cost function is continuous. This ensures that gradient descent does not encounter any abrupt or unpredictable changes in direction.
- Smooth changes allow for better convergence during optimization.

## How to find a good learning rate, you can use grid search - learn how?

Grid search is a systematic way to determine the optimal learning rate by trying out multiple predefined values and evaluating their performance.

Finding a good learning rate is critical for the convergence and performance of gradient-based optimization algorithms. Here’s how you can find a good learning rate using grid search:

**Define the Range of Learning Rates:**
- Choose a range of learning rates to test, e.g., [0.0001,0.001,0.01,0.1,1][0.0001,0.001,0.01,0.1,1].
- Include a mix of small and large values to observe their effects.

**Train the Model for Each Learning Rate:**
- Train the model (e.g., SGDRegressor) with each learning rate.
- Use the same number of iterations and random seed to ensure fair comparison.

**Evaluate the Performance:**
- Use metrics like Mean Squared Error (MSE) or R-squared (R2) on the validation set to evaluate performance.

**Choose the Best Learning Rate:**
- Select the learning rate that minimizes the error or maximizes R2.

**Benefits of Grid Search:**

Systematic Exploration: 
- Tests all values in the predefined range.

Cross-Validation: 
- Ensures robustness by evaluating performance on multiple splits of the data.

Reproducibility: 
- Consistent process for comparing hyperparameters.













