# 📊 **Big Basket Mini Project** 🚀

Welcome to my **Data Analysis Project**! In this project, I explore a **sales dataset** to uncover meaningful insights like top-selling products, handling missing values, detecting outliers, and visualizing trends. All analyses were conducted using **Python** on **Google Colab**. 

![Data Analysis](https://img.shields.io/badge/Language-Python-blue?style=flat-square) ![Status](https://img.shields.io/badge/Status-Completed-green?style=flat-square)

---

## ✨ **Project Overview**

This project covers a range of data analysis tasks. Here are the main steps we'll cover:

| **Step**        | **Action**                                                       |
|-----------------|------------------------------------------------------------------|
| 1. **Load Data** | Import and load the dataset into a Pandas DataFrame.            |
| 2. **Explore Data** | Preview the first 12 rows to understand its structure.        |
| 3. **Describe Data** | Generate summary statistics for data distribution.            |
| 4. **Dataset Info** | Analyze data types, missing values, and column details.       |
| 5. **Top & Least Sold Products** | Identify the top 5 most and least sold products.  |
| 6. **Discount Analysis** | Calculate discount percentages on selected items.         |
| 7. **Missing Values** | Check for and handle missing data in the dataset.             |
| 8. **Outlier Detection** | Detect and handle outliers using IQR method.               |
| 9. **Visualization** | Create meaningful charts and graphs for data insights.         |

---

## 🛠️ **Technologies Used**

- **Python** - The programming language used for analysis
- **Pandas** - Data manipulation and analysis library
- **Matplotlib** - Plotting library for static charts
- **Seaborn** - Statistical data visualization library

---

## 📦 **Dataset Information**

The dataset contains the following key columns:

| **Column**     | **Description**                           |
|----------------|-------------------------------------------|
| **product**    | Name of the product.                      |
| **sales**      | Number of units sold.                     |
| **price**      | Price of the product.                     |
| **discount**   | Discount offered on the product.          |

---

## 🚶 **Steps Performed**

### 1. **Load the Dataset** 📥

2. Explore the Data 🔍
We use the head() function to view the first 12 rows and examine the structure of the data.

df.head(12)
3. Generate Data Description 📝
Using the describe() method, we generate summary statistics to understand the distribution of numeric data.

df.describe()
4. Check Dataset Info 🧑‍💻
We check the information about the dataset using info(), including column types, missing values, and memory usage.

df.info()
5. Top & Least Sold Products 🏅
We group data by product and calculate the total sales to find the top 5 most and least sold products.

top_sold = product_sales.nlargest(5)
least_sold = product_sales.nsmallest(5)
6. Discount Analysis 💸
We calculate the discount percentage for a selected product (e.g., "Product A").

product_data['discount_percentage'] = (product_data['discount'] / product_data['price']) * 100
7. Handle Missing Values ❓
We identify missing values in the dataset and handle them accordingly.

missing_values = df.isnull().sum()
missing_values[missing_values > 0]
8. Outlier Detection & Handling 🚨
Using the IQR method, we detect and handle outliers in numeric columns and fill them with the mean.

outliers = ((df < (Q1 - 1.5 * IQR)) | (df > (Q3 + 1.5 * IQR)))
df_cleaned = df.apply(lambda x: x.fillna(x.mean()) if x in outliers else x)
9. Create Visualizations 📊
We visualize insights such as the top 5 most sold products using a bar chart.

import matplotlib.pyplot as plt
top_sold.plot(kind='bar', color='skyblue', figsize=(10,6))
plt.title('Top 5 Sold Products')
plt.xlabel('Product')
plt.ylabel('Total Sales')
plt.show()
🌟 Key Findings
Top Products: Identifying bestsellers helps optimize stock and marketing strategies.
Sales Trends: Visualizing trends helps understand the sales behavior of products over time.
Discount Insights: Analyzing discounts allows for better pricing strategies.
Data Quality: Handling missing values and outliers ensures more accurate results.
🎨 Sample Visual Output
Here’s an example of the Top 5 Most Sold Products visualization:


🏁 How to Run the Project
Upload your dataset to Google Colab.
Run the provided Python code in the cells.
Install necessary libraries (pandas, matplotlib, seaborn) if not already available.
🚀 Contribute
Feel free to fork the repository, make improvements, or open issues if you encounter bugs or have ideas for enhancements. Contributions are always welcome!

📜 License
This project is licensed under the MIT License.

📝 Author
Your Name
LinkedIn | GitHub
💬 Get In Touch
If you have any questions, suggestions, or comments, don't hesitate to reach out! I’d love to hear from you.

Thank you for checking out my project! 🎉













