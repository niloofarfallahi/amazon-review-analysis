# Anomaly Detection in E-commerce Reviews

## Project Overview

This project focuses on analyzing a large dataset of Amazon beauty product reviews to identify unusual or potentially fraudulent patterns. Using a data analysis pipeline that combines exploratory data analysis (EDA), natural language processing (NLP), and a machine learning model, the goal is to uncover anomalies that could impact an e-commerce platform's integrity and customer trust.

The analysis demonstrates a complete workflow from raw data to actionable business insights, showcasing skills in data processing, visualization, and machine learning.

## Methodology & Analysis

### 1. Data Source

The dataset used for this analysis is a subset of the **Amazon-Reviews-2023** dataset from the Hugging Face library, specifically focusing on the "All Beauty" product category.

### 2. Exploratory Data Analysis (EDA)

The initial phase involved a comprehensive exploration of key features, including:
* **Ratings:** Analysis of the distribution of star ratings, which were heavily skewed toward 5 stars.
* **Review Length:** Examination of review text length in both characters and words to understand the level of detail provided by users.
* **Helpfulness Votes:** Analysis of the distribution of helpful votes, revealing a small number of reviews received a disproportionately high number of votes.

### 3. Anomaly Detection with Isolation Forest

The **Isolation Forest** model was used to identify statistical outliers. This unsupervised machine learning algorithm is particularly effective for detecting anomalies in large datasets.

The model was trained on numerical features like **review length** and **helpful votes**. It successfully identified reviews that were "easy to isolate" from the rest of the data, such as:
* Extremely short reviews with a perfect 5-star rating.
* Reviews with an unusually high number of helpful votes relative to their length.

## Key Business Insights

The project identified several types of anomalies that can be problematic for an e-commerce business. These findings can be used to:
* **Proactively Flag Spam:** Implement an automated system to flag and investigate reviews with high anomaly scores, helping to filter out spam or fake content.
* **Improve Customer Trust:** By identifying and managing fraudulent reviews, the platform can ensure that customer feedback is genuine, thus building and maintaining trust.
* **Optimize Review Display:** Prioritize and highlight highly helpful and detailed reviews to improve the customer experience and help with purchase decisions.

## How to Run the Project

To replicate this analysis, you can either run the Jupyter notebook or execute the Python script.

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/niloofarfallahi/amazon-review-analysis.git](https://github.com/niloofarfallahi/amazon-review-analysis.git)
    cd amazon-review-analysis
    ```

2.  **Run the Analysis:**
    * **Using the Notebook:** Open the `notebooks/analysis_notebook.ipynb` file in a Jupyter environment.
    * **Using the Script:** Run the main analysis script from the terminal.
    
    ```bash
    python src/analysis_script.py
    ```

---
**Note:** The dataset will be automatically downloaded the first time you run the code, as it's sourced directly from the Hugging Face library.