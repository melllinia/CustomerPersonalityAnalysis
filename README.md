# Customer Personality Analysis

## Overview
Customer Personality Analysis is a detailed examination of a company’s ideal customers. It helps businesses better understand their customers, allowing them to tailor products, marketing strategies, and services to meet the specific needs, behaviors, and concerns of different customer segments.

Instead of marketing a product to all customers, businesses can use customer personality analysis to identify the most relevant customer segment and focus marketing efforts accordingly, improving efficiency and effectiveness.

---

## Data Analysis and Preprocessing
The initial dataset contained **2240 samples (rows) and 29 features (columns)**. The following preprocessing steps were applied:

- **Transformed** birth date into age (reference date: *01.01.2015*) and converted `Dt_Customer` into days since enrollment.
- **Dropped unnecessary columns** that did not contribute to meaningful insights.
- **Removed invalid marital status entries** (`YOLO`, `Absurd`, `Alone`).
- **Encoded categorical variables**:
  - *Label-encoded* marital status and education level.
- **Handled outliers**:
  - Removed outliers in *Age* and *Income* using the **Interquartile Range (IQR) method**.

After cleaning and preprocessing, the final dataset consists of **2198 rows and 20 columns**.

---

## Key Insights from Correlation Analysis

### **Income**
- Positively correlated with spending on all product categories, especially **wine** and **meat**.
- Negatively correlated with the **number of children at home**.
- High-income customers **avoid discounts**, indicating **lower price sensitivity**.

### **Education**
- Higher education levels correlate with increased **wine purchases**.

### **Family-Oriented Customers**
- Customers with **more children at home** tend to have **higher web visits**.
- They exhibit different spending behaviors compared to households without children.

### **Complaint Behavior & Clustering**
- Customers who frequently **complain** form **distinct, small clusters**.
- Within each cluster, **education levels** further segment customer behavior.
- **Marital status** may not be a significant factor for customer segmentation.
- Customers with **children at home ("Kids at Home" and "Teens at Home")** are grouped together within specific clusters.

---

## Technologies Used
- **Python** (Pandas, NumPy, Matplotlib, Seaborn)
- **Scikit-learn** (Dimensionality Reduction & Clustering)
- **Data Cleaning & Preprocessing** (Feature Engineering, Outlier Removal)
- **Visualization** (Correlation Heatmaps, Data Distribution Between Clusters)

---

## Repository Contents

This repository includes:  
- **Jupyter Notebook (`analysis.ipynb`)** – Contains data analysis, preprocessing steps, and visualizations.  
- **Report (`report.pdf`)** – A detailed report summarizing the findings and insights from the analysis.
