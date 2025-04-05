# New York Airbnb Price Prediction & EDA


This project performs **Exploratory Data Analysis (EDA)** and applies **Machine Learning** techniques on New York City Airbnb listings. By leveraging libraries such as Pandas, Numpy, Matplotlib, Seaborn, and **Random Forest Regression**, the goal is to uncover pricing trends, room type distributions, and host behaviors, while predicting prices based on room type and location.

---

## 📝 **Project Overview**

The objective of this project is to:
- **Analyze room types, prices, and availability** across different neighborhoods in New York City.
- Understand **host behavior** and **listing patterns**.
- Detect potential **outliers in pricing**.
- Use **Machine Learning** to predict Airbnb prices based on room type and neighborhood.

---

## 📊 **Dataset**

The dataset contains **20,765 listings** and **22 features**, including:

- **id**: Unique listing identifier.
- **price**: Nightly rental price.
- **room_type**: Type of accommodation (e.g., Entire home/apt, Private room).
- **neighborhood_group**: Borough of the listing.
- **latitude/longitude**: Geographical location.
- **availability_365**: Number of available days in the year.

---

## 🔍 **Data Cleaning & Preprocessing**

1. **Handling Missing Data**: Rows with missing values in key columns such as `price`, `room_type`, and `neighborhood` were dropped.
2. **Categorical Encoding**: 
   - Applied **Label Encoding** to transform categorical features (`room_type` and `neighborhood_group`) into numerical values.
3. **Outliers Handling**: Listings with prices greater than $1,000 were capped to avoid skewed visualizations.

---

## 📈 **Exploratory Data Analysis (EDA)**

- **Room Type Distribution**:  
   Visualized the distribution of room types, finding that **Entire homes/apartments** are the most common.

- **Price Trends by Neighborhood**:  
   Explored how average prices vary by borough, with **Manhattan** having the highest average prices.

- **Price Distribution**:  
   Most listings are priced between **$50 and $300** per night.

- **Host Behavior**:  
   Identified hosts with multiple listings using boxplots, showing trends toward **professional hosting**.

- **Availability Insights**:  
   Listings with high availability tend to have **lower prices** and **more reviews**, indicating better guest experiences.

---

## 🤖 **Machine Learning for Price Prediction**

Using **RandomForestRegressor**, we predicted the price of Airbnb listings based on **room type** and **neighborhood**:

1. **Data Preprocessing**:
   - Dropped rows with missing values in key columns.
   - Encoded **room type** and **neighborhood** using **Label Encoding**.

2. **Modeling**:
   - Split the data into **training** and **test** sets (80/20 split).
   - Trained the model with 100 estimators in the **RandomForestRegressor**.

3. **Evaluation**:
   - **Mean Squared Error (MSE)**: 12,526.29  
   - **R-squared (R²)**: 0.21  
     - The model performed moderately well, but there is room for improvement, indicating that other features might be needed to improve predictions.

4. **Visualizations**:
   - **Actual vs Predicted Prices**:  
     ![image](https://github.com/user-attachments/assets/35e40f23-2a0f-4e5b-a76d-1a1c26dbea36)
)
)  
     Scatter plot showing how well the model's predictions align with actual prices.
   
   - **Feature Importance**:  
     ![image](https://github.com/user-attachments/assets/0b391776-7291-4590-97ce-686ccbcd96e0)
)
)  
     Bar plot showing the importance of **Room Type** and **Neighborhood** in predicting prices.

---

## 🔑 **Key Findings**

- **Price Trends**:  
   - **Manhattan** listings are significantly more expensive than those in other boroughs.
   - **Entire homes/apartments** are the most expensive type, while **private rooms** are more budget-friendly.

- **Outliers**:  
   Extreme price outliers, such as listings over $10,000 per night, were identified and filtered.

- **Availability & Price**:  
   Listings with more availability tend to have lower prices and more reviews, suggesting that higher availability is correlated with better guest experiences.

- **Model Performance**:  
   - The **Random Forest model** provides a decent level of accuracy, but could be enhanced with additional features or tuning.

---

## 💡 **Recommendations**

### For Guests:
- Choose listings with **high availability** and **good reviews** for a better overall experience.
- If you’re looking for **affordable stays**, **private rooms in Brooklyn** offer better value than those in Manhattan.

### For Hosts:
- Improve **availability** and **review response rates** to attract more bookings.
- Adjust pricing using **predictions** based on **room type** and **location** to remain competitive.

---

## ⚙️ **Technologies Used**

- **Python**: The primary programming language.
- **Pandas**: For data manipulation and analysis.
- **Numpy**: For numerical operations.
- **Matplotlib & Seaborn & Plotly**: For data visualization.
- **Scikit-Learn**: For machine learning model development.

---

## 📈 **Project Results**  
The machine learning model was trained to predict **Airbnb rental prices** based on **room type** and **location**. The **R-squared** value of 0.21 suggests that, while the model makes reasonable predictions, there is significant room for improvement.

```python
Mean Squared Error: 12526.29
R-squared: 0.21
