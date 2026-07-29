# Customer Segmentation using K-Means Clustering

Name: Avyay J Das
MUID: avyayjdas@mulearn

---

# Project Summary

This project applies the K-Means clustering algorithm to segment supermarket customers based on their demographic and spending behavior. Customer segmentation helps identify groups with similar characteristics, enabling businesses to design targeted marketing strategies, improve customer satisfaction, and increase revenue.

---

# Approach

The following steps were performed to complete the project:

- Loaded and explored the customer dataset.
- Removed the `CustomerID` column as it does not contribute to clustering.
- Encoded the `Gender` feature into numerical values.
- Checked for missing values and outliers.
- Applied **StandardScaler** to normalize all features.
- Used the **Elbow Method** to determine the optimal number of clusters.
- Trained a **K-Means** clustering model with **5 clusters**.
- Assigned each customer to a cluster.
- Profiled each cluster based on the average feature values and assigned meaningful business names.
- Applied **Principal Component Analysis (PCA)** to reduce the data to two dimensions for visualization.
- Visualized the customer segments and analyzed the resulting clusters.

---

# Important Observations and Findings

- No missing values were found in the dataset.
- A single outlier was observed in the Annual Income feature, but it was retained as it represents a valid customer.
- Feature scaling was performed since K-Means is distance-based and requires features to be on a similar scale.
- The Elbow Method indicated that **5** is the optimal number of clusters.
- PCA reduced the dataset to two principal components, explaining **59.92%** of the total variance.
- The clustering process identified five distinct customer segments with different income and spending patterns.

---

# Final Conclusions and Business Insights

The K-Means model successfully segmented customers into five meaningful groups, allowing the supermarket to better understand customer behavior.

### Customer Segments

- **HIGH-VALUE CUSTOMERS** – High-income customers with relatively high spending.
- **HIGH-INCOME LOW SPENDERS** – Customers with high income but low spending potential.
- **YOUNG HIGH SPENDERS** – Young customers who spend frequently despite moderate income.
- **BUDGET SHOPPERS** – Young customers with lower income and moderate spending.
- **SENIOR MODERATE SPENDERS** – Older customers with moderate income and spending.

### Business Insights

- Reward **HIGH-VALUE CUSTOMERS** with loyalty programs and exclusive benefits.
- Encourage **HIGH-INCOME LOW SPENDERS** through personalized promotions and premium product recommendations.
- Retain **YOUNG HIGH SPENDERS** with targeted marketing campaigns and special offers.
- Provide discounts and value-for-money deals for **BUDGET SHOPPERS**.
- Offer personalized services and loyalty incentives to **SENIOR MODERATE SPENDERS** to improve customer retention.
