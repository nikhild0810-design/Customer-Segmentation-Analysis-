Customer Segmentation & Spending Prediction

Project Overview

This project focuses on analyzing customer data to:

- Understand customer behavior
- Segment customers based on demographics
- Predict customer spending using Machine Learning

The workflow includes data cleaning, exploratory data analysis (EDA), segmentation, and model building.

 Dataset

The dataset ("customer_data.csv") contains customer-related attributes such as:

- Age
- Gender
- Education
- Income
- Country
- Purchase Frequency
- Spending

Project Workflow

1. Data Loading

data = pd.read_csv("customer_data.csv")

2. Data Exploration

- View dataset:
  data.head(), data.tail()
- Check structure:
  data.info(), data.shape
- Summary statistics:
  data.describe()

3. Data Cleaning

- Handle missing values:
  data.dropna(inplace=True)
- Remove duplicates:
  data.drop_duplicates(inplace=True)

4. Customer Segmentation

 Age Group Segmentation

Customers are grouped into:

- 18–35
- 36–50
- 51–65
- 65+

pd.cut(data["age"], bins=[18,36,51,66,100])

 Education-Based Segmentation

- Analyze total spending per education level
- Calculate percentage contribution

Country-Based Analysis

- Calculate average spending per country
- Identify high-value markets

 Exploratory Data Analysis (EDA)

The notebook includes:

- Distribution analysis
- Group-based aggregations
- Spending trends

Machine Learning Model

Model Used:

- Decision Tree Regressor

Features:

- Age
- Gender
- Education
- Income
- Country
- Purchase Frequency

Target:

- Spending

Model Training

model = DecisionTreeRegressor()
model.fit(X_train, y_train)

 Prediction System

The model takes user input and predicts customer spending.

Example inputs:

- Age
- Gender
- Education
- Income
- Country
- Purchase Frequency

Output:

Predicted Customer Spending

Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

How to Run

1. Clone the repository
2. Install dependencies:
   pip install pandas numpy matplotlib scikit-learn
3. Run the notebook:
   jupyter notebook

 Key Insights

- Customer spending varies significantly by education and country
- Age grouping helps identify target segments
- Purchase frequency strongly impacts spending behavior

 Future Improvements

- Use advanced models (Random Forest, XGBoost)
- Deploy using a web app (Gradio / Streamlit)
- Improve feature engineering
- Add real-time prediction system


Author

Nikhil D

Conclusion

This project demonstrates how data analysis and machine learning can be used to:

- Understand customer behavior
- Segment users effectively
- Predict spending for business decisions
