# Linear Regression Project: Predicting E-commerce Customer Spending

This project implements a linear regression model in Python to predict the "Yearly Amount Spent" by customers of an e-commerce clothing store. The model is built to understand the relationships between customer engagement (e.g., time on app, website usage, membership length) and their total spending.

This project follows the end-to-end data science workflow demonstrated in the tutorial by **Alejandro AO - Software & Ai** on YouTube.
* **Original Video:** [Linear Regression in Python - Full Project for Beginners](https://www.youtube.com/watch?v=O2Cw82YR5Bo)

---

## 📈 Project Workflow

The project follows these key steps:

1.  **Data Import:** Loaded the `ecommerce.csv` dataset using **Pandas**.
2.  **Exploratory Data Analysis (EDA):**
    * Investigated the dataset using `.info()` and `.describe()` to find statistical summaries and data types.
    * Used **Seaborn** to create visualizations (`jointplot`, `pairplot`) to find correlations between variables.
    * The `pairplot` revealed the strongest linear relationship is between `Length of Membership` and `Yearly Amount Spent`.
3.  **Data Preprocessing:**
    * Separated the data into `X` (the features/predictors) and `y` (the target variable, `Yearly Amount Spent`).
    * Split the data into training and testing sets (70% train, 30% test) using `train_test_split` from **Scikit-learn**.
4.  **Model Training:**
    * Imported the `LinearRegression` model from `sklearn.linear_model`.
    * Created an instance of the model.
    * Trained (fit) the linear regression model on the training data.
5.  **Model Evaluation:**
    * **Coefficients:** Inspected the model's coefficients (`lm.coef_`) to understand the importance of each feature.
    * **Predictions:** Used the trained model to predict `Yearly Amount Spent` for the unseen `X_test` data.
    * **Metrics:** Calculated key regression metrics to measure the model's performance:
        * Mean Absolute Error (MAE)
        * Mean Squared Error (MSE)
        * Root Mean Squared Error (RMSE)
6.  **Residual Analysis:**
    * Calculated the residuals (the difference between actual values and predicted values).
    * Plotted a **histogram of the residuals** to check for a normal distribution, which is a key assumption of linear regression.
    * Plotted a **Q-Q plot** (`scipy.stats.probplot`) as a second graphical check for normality.

---

## 📊 Dataset

* **File:** `ecommerce.csv`
* **Description:** A synthetic e-commerce dataset containing customer data.

### Features (X)
* `Avg. Session Length`: Average time (in minutes) of in-store styling sessions.
* `Time on App`: Average time (in minutes) spent on the mobile app.
* `Time on Website`: Average time (in minutes) spent on the store's website.
* `Length of Membership`: Number of months the customer has been a member.

### Target Variable (y)
* `Yearly Amount Spent`: The total amount (in dollars) spent by the customer in that year.

---

## 🛠️ Libraries Used
* **Pandas:** For data loading, manipulation, and analysis.
* **NumPy:** For numerical operations (used implicitly by other libraries).
* **Matplotlib:** For basic plotting and customizing visualizations.
* **Seaborn:** For advanced and statistical data visualization (e.g., `pairplot`, `jointplot`, `lmplot`).
* **Scikit-learn (sklearn):** For the core machine learning workflow, including `train_test_split`, `LinearRegression`, and metrics.
* **SciPy:** For creating the Q-Q (probability) plot.
