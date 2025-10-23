# 🛍 Customer Segmentation using K-Means – Google Colab Notebook

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1L1iiD7nK3surZyEcqQuAQ7URoyC1JOHU?usp=sharing)  
[![Python](https://img.shields.io/badge/python-3.10-blue.svg)](https://www.python.org/)  

This project performs **Customer Segmentation** using **K-Means clustering** on customer data from a mall.  
The goal is to identify distinct customer groups based on **Annual Income** and **Spending Score**, which helps businesses target marketing strategies and improve sales.

---

## 📂 Dataset

- **Source:** [Mall Customers Dataset](https://1drv.ms/x/c/381fbc963ba3e5bd/EWUHXyvcietAiyfH6heRlZ8BAhI3piI6VOxs-oJ7finCHA?e=WPlXWp)
- **Number of records:** 200 customers
- **Columns:**
  - `CustomerID`: Unique ID for each customer
  - `Genre`: Gender of customer
  - `Age`: Age of the customer
  - `Annual Income (k$)`: Annual income in thousand dollars
  - `Spending Score (1-100)`: Customer’s spending behavior score

---

## 🌟 Features

- Data exploration: head, info, describe, correlation
- Visualization of:
  - Annual Income distribution
  - Age distribution
  - Spending Score distribution
  - Gender count
- K-Means clustering:
  - Elbow Method to determine optimal clusters
  - Cluster assignment and 2D visualization
- Cluster interpretation with descriptive labels:
  - High Income, High Spending
  - High Income, Low Spending
  - Low Income, High Spending
  - Low Income, Low Spending
  - Average Income/Spending
- Display of customers in each cluster

---

## 📊 Methodology

1. **Data Loading and Exploration**
   - Load the CSV dataset
   - Check for missing values and data types
   - Explore statistical summaries and correlations

2. **Data Visualization**
   - Plot distributions of numeric features
   - Count plot for gender

3. **Feature Selection for Clustering**
   - Use `Annual Income (k$)` and `Spending Score (1-100)` as clustering features

4. **Finding Optimal Clusters**
   - Apply **Elbow Method** to WCSS (Within-Cluster Sum of Squares)
   - Choose the number of clusters where the elbow is observed (5 in this case)

5. **K-Means Clustering**
   - Fit K-Means with the chosen number of clusters
   - Assign cluster labels to each customer

6. **Cluster Analysis**
   - Calculate cluster centroids
   - Assign descriptive labels based on income and spending behavior
   - Visualize clusters in a 2D scatter plot

7. **Result Interpretation**
   - Identify customer segments
   - Number of customers in each segment
   - Customer IDs per segment for targeted strategies

---

## 📈 Results

| Cluster | Label                       | # Customers | Characteristics |
|---------|-----------------------------|-------------|----------------|
| 0       | Average Income/Spending     | 81          | Medium income and spending |
| 1       | High Income, High Spending  | 39          | Wealthy and active shoppers |
| 2       | Low Income, High Spending   | 22          | Low income but high spending |
| 3       | High Income, Low Spending   | 35          | Wealthy but low spending |
| 4       | Low Income, Low Spending    | 23          | Low income and low spending |

---

## 📸 Visualizations

**Annual Income Distribution**  
![Annual Income](images/annual_income.png)

**Spending Score Distribution**  
![Spending Score](images/spending_score.png)

**Customer Clusters (2D Scatter Plot)**  
![Clusters](images/clusters.png)

> Replace the above placeholders with actual screenshots from your Colab notebook outputs.

---

## 🛠 How to Run

1. Open the notebook in Google Colab:  
   [Open in Colab](https://colab.research.google.com/drive/1L1iiD7nK3surZyEcqQuAQ7URoyC1JOHU?usp=sharing)
2. Run all cells sequentially.
3. Upload the dataset if prompted (or ensure the file path matches).

---

## 📦 Dependencies

- Python 3.x
- Libraries:
  - `numpy`
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `scikit-learn`

Google Colab comes pre-installed with these libraries. To run locally:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
