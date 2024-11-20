# **Customer Segmentation using RFM Analysis and K-Means Clustering**

## **Project Overview**
This project performs **customer segmentation** using the RFM (Recency, Frequency, and Monetary) framework combined with **K-Means clustering**. The primary goal is to divide customers into distinct groups based on their purchasing behavior to enable better-targeted marketing and customer retention strategies.

By analyzing customer purchase history, this project identifies key customer segments (e.g., loyal, active, or at-risk customers), allowing businesses to optimize their marketing campaigns and improve customer satisfaction.

---

## **Table of Contents**
1. [About RFM Analysis](#about-rfm-analysis)
2. [Data Preprocessing](#data-preprocessing)
3. [Modeling Approach](#modeling-approach)
4. [Results and Insights](#results-and-insights)
5. [How to Run the Project](#how-to-run-the-project)
6. [Future Enhancements](#future-enhancements)

---

## **About RFM Analysis**
RFM is a behavioral model that helps identify customer segments based on:
- **Recency**: How recently a customer made a purchase.
- **Frequency**: How often they make purchases.
- **Monetary**: How much they spend.

Using these metrics, we gain insights into customer loyalty, activity levels, and spending habits.

---

## **Data Preprocessing**
The raw data includes columns like **customer IDs, transaction dates, and purchase amounts**. Key preprocessing steps include:

1. **Calculate RFM Metrics**:
   - **Recency**: Days since the last purchase.
   - **Frequency**: Total number of purchases.
   - **Monetary**: Total spending by the customer.

2. **Remove Outliers**:
   - Outliers were capped to improve model performance and ensure clusters are well-separated.

3. **Standardize Features**:
   - RFM metrics were scaled using **StandardScaler** to normalize values and ensure equal weighting in clustering.

---

## **Modeling Approach**
The customer segmentation process follows these steps:

1. **Data Preparation**:
   - RFM features were computed and scaled.

2. **Clustering with K-Means**:
   - The **K-Means algorithm** was applied to segment customers into distinct groups.
   - The optimal number of clusters was determined using the **Elbow Method**, analyzing within-cluster sum of squares (WCSS).

3. **Cluster Evaluation**:
   - Pairplot visualizations and mean values of RFM metrics per cluster were used to interpret cluster characteristics.

---

## **Results and Insights**
### **Cluster Summary**
| **Cluster** | **Recency (Days)** | **Frequency** | **Monetary (Currency)** | **Description**                  |
|-------------|--------------------|---------------|--------------------------|----------------------------------|
| **0**       | 234.22             | 19.88         | 262.92                  | Inactive Customers              |
| **1**       | 51.83              | 20.71         | 299.32                  | Moderately Active Customers     |
| **2**       | 45.28              | 68.95         | 836.79                  | Active Customers                |
| **3**       | 39.41              | 115.72        | 1709.82                 | High-Value Customers (VIPs)     |

### **Key Insights**:
- **Cluster 3** represents the most loyal and valuable customers who purchase frequently and spend the most.
- **Cluster 0** comprises inactive customers, indicating potential churn.
- **Cluster 1** and **Cluster 2** reflect a middle ground, showing opportunities for engagement and growth.

---

## **How to Run the Project**

### **Prerequisites**
1. Python 3.7 or higher.
2. Required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`.

### **Setup Instructions**
1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo-name/customer-segmentation.git
   cd customer-segmentation
