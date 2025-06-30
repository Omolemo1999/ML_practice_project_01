🏫 2026 QS World University Rankings Analysis
This project analyzes the 2026 QS World University Rankings dataset, including data cleaning, exploratory data analysis (EDA), feature engineering, and model selection using regression techniques.

📂 Dataset
Source: Kaggle - 2026 QS World University Rankings

Downloaded using kagglehub.

📊 Objective
The goal is to build a regression model that can predict a university's overall score using other numerical features in the dataset. The project includes a baseline model and a pipeline-driven approach to evaluate different models and select the best-performing one based on MAE (Mean Absolute Error).

🔧 Steps Performed
1. 📥 Data Loading
The dataset was loaded using the kagglehub API and pandas.

python
Copy
Edit
import kagglehub
path = kagglehub.dataset_download('akashbommidi/2026-qs-world-university-rankings')
2. 🧹 Data Cleaning
Removed or imputed missing values.

Checked for and dropped duplicate rows.

Cleaned/renamed columns for consistency.

Ensured all numeric features were in the correct format.

3. 📈 Exploratory Data Analysis (EDA)
Used seaborn and matplotlib for visualizations.

Analyzed feature distributions, correlation matrix, and outliers.

Checked for multicollinearity to inform feature selection.

4. 🧪 Baseline Model
A naive baseline model was created using the mean of the target variable for comparison.

Baseline MAE was calculated as a reference.

5. ⚙️ Model Pipeline & Selection
Created a pipeline using StandardScaler and regression models.

Evaluated the following models:

Linear Regression ✅ (chosen due to lowest MAE)

Ridge Regression

Lasso Regression

ElasticNet

Used train_test_split and mean_absolute_error for evaluation.

python
Copy
Edit
pipeline = Pipeline([
    ('scaler', StandardScaler()),
    ('model', LinearRegression())
])
6. 📊 Evaluation Metrics
MAE (Mean Absolute Error)

RMSE (Root Mean Squared Error)

R² Score

Linear Regression was chosen as the final model due to its best performance on the test data.

📌 Key Results
Linear Regression outperformed other models in terms of MAE.

StandardScaler improved model performance by normalizing features.

The final model demonstrated good predictive ability on unseen data.

🧠 Tools & Libraries
Python

pandas, numpy

matplotlib, seaborn

scikit-learn

kagglehub

🏁 How to Run
Clone the repo:

bash
Copy
Edit
git clone https://github.com/Omolemo1999/ML_practice_project_01
cd qs-university-rankings-analysis
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Run the script:

bash
Copy
Edit
python main.py
📬 Contact
Omolemo Tlomatsane
📧 Email: tlomatsaneomolemo@gmail.com
🔗 LinkedIn: https://www.linkedin.com/in/omolemo-tlomatsane/

