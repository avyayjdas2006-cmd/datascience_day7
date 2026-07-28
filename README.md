# Mall Customer Segmentation via K-Means

Name: Avyay J Das
MUID: avyayjdas@mulearn

# What this project does
This project applies unsupervised machine learning to group mall retail customers into distinct segments based on their age, gender, annual income, and spending scores. The goal is to identify actionable target audiences for marketing teams.

# My Approach
1. **Data Prep:** Loaded the customer data (200 rows, no missing values), handled the categorical `Gender` column by mapping it to binary values (0 = Male, 1 = Female), and dropped the arbitrary `CustomerID` column.
2. **Feature Scaling:** Applied `StandardScaler` because K-Means relies completely on Euclidean distance math, meaning columns with large ranges (like income) would completely drown out smaller metrics (like age or the binary gender flag).
3. **Finding K:** Used the Elbow Method to plot the within-cluster sum of squares (WCSS) for K = 1 to 10. The rate of decrease slows down noticeably around **K = 5**, so 5 clusters was chosen (matching the assignment's target segment count).
4. **Dimension Reduction:** Since humans can't visualize 4D data, I used Principal Component Analysis (PCA) to compress the dataset into 2 dimensions. This captured **54.80%** of the total variance, letting us see the clusters on a scatter plot. A supplementary raw Annual Income vs Spending Score plot is also included since those two features separate the segments most visibly.

# The 5 Customer Segments Identified
Gender turned out to be a strong natural separator once Age and Income were factored in — three of the five clusters ended up single-gender:

* **Cluster 0 (Young High Spenders):** Mostly female (73%), younger crowd (avg age 27), mid income (~$63k) but very high spending score (~79). 37 customers.
* **Cluster 1 (Middle-Aged Moderate Women):** 100% female, avg age 55, mid income (~$48k), moderate spending score (~44). 42 customers.
* **Cluster 2 (Older Affluent Active Men):** 100% male, avg age 57, high income (~$74k), solid spending score (~61). 46 customers.
* **Cluster 3 (High-Earning Cautious Men):** 100% male, younger-middle age (avg 34), high income (~$94k) but very low spending score (~28). 44 customers.
* **Cluster 4 (High-Earning Reserved Women):** 100% female, avg age 47, the highest income of any segment (~$114k), but low-moderate spending score (~37). 31 customers.

# Business Strategies
* **Retain Cluster 0 (Young High Spenders):** Already highly engaged — keep them with loyalty programs, trend-driven collections, and early access to new drops.
* **Grow Cluster 1 (Middle-Aged Moderate Women):** Increase wallet share with targeted bundle offers and seasonal promotions matched to mid-range budgets.
* **Maintain Cluster 2 (Older Affluent Active Men):** A dependable revenue base — sustain the relationship with premium loyalty perks and personalized service.
* **Prioritize Cluster 3 & 4 (High-Earning, Low-Spending):** These two segments have the money but aren't spending it. This is the biggest untapped opportunity — target them with premium/exclusive product positioning, high-touch personal shopping, or invite-only VIP events to convert income into spend.

# Conclusions
The combination of Age, Gender, Income, and Spending Score reveals more nuanced segments than income and spending alone would — in particular, it surfaces that spending behavior at similar income levels diverges sharply by gender and age. The clearest business opportunity lies in the two high-income, low-spending clusters (3 and 4), which together represent 75 of the 200 customers (37.5%) and are prime candidates for targeted premium marketing.
