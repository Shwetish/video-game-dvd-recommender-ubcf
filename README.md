# video-game-dvd-recommender-ubcf
A User-Based Collaborative Filtering (UBCF) recommendation engine built on customer survey data to suggest top-selling video gaming DVDs and boost retail sales.

# Video Gaming DVD Recommender System (UBCF)

## 1. Business Problem
### 1.1. What is the business objective?
The primary business objective is to analyze customer survey data from a video gaming store to build an automated User-Based Collaborative Filtering (UBCF) recommendation engine. By suggesting top-selling and relevant gaming DVDs to customers, the store aims to improve customer experience, increase cross-selling opportunities, and drive overall sales.

### 1.2. Are there any constraints?
* **Data Sparsity:** Survey-based recommendation datasets often suffer from high sparsity since users only rate a small fraction of available video games.
* **Cold Start Problem:** Handling new users or new gaming DVDs with minimal or no rating history.
* **Scalability:** The algorithm must efficiently compute similarity scores between users as the customer base and product catalog grow.

---

## 2. Data Dictionary
| Feature Name | Data Type | Description |
| :--- | :--- | :--- |
| `CustomerID` / `User_ID` | Integer / Categorical | Unique identifier for each surveyed customer. |
| `DVD_ID` / `Game_ID` | Integer / Categorical | Unique identifier for each video gaming DVD. |
| `Rating` | Numeric | Customer preference score or rating given to the gaming DVD. |
| *(Add other dataset-specific columns here)* | ... | ... |

---

## 3. Exploratory Data Analysis (EDA)
* **3.1. Summary:** Overview of dataset dimensions, missing values, data distributions, and overall data types.
* **3.2. Univariate Analysis:** Distribution of customer ratings, frequency of ratings per user, and popularity distribution of individual gaming DVDs.
* **3.3. Bivariate Analysis:** User-item interaction patterns, rating frequency correlations, and identifying clusters of high-affinity gamers.

---

## 4. Data Pre-processing & Cleaning
* **Data Cleaning:** Handling missing values, duplicate entries, and inconsistent formatting in user/DVD identifiers.
* **Data Mining:** Transforming tabular survey responses into a user-item sparse matrix suitable for collaborative filtering.
* **Normalization:** Centering or standardizing user rating scales to account for optimistic or critical raters.

---

## 5. Model Building
* **UBCF Implementation:** Developed a User-Based Collaborative Filtering model using Python (utilizing libraries such as `Surprise`, `pandas`, and `scikit-learn`).
* **Similarity Metric:** Computed cosine similarity or Pearson correlation between users to find nearest neighbors.
* **Prediction & Recommendation:** Generated top-$N$ personalized DVD recommendations for store customers based on the preferences of similar user profiles.

---

## 6. Business Benefits & Impact
* **Increased Sales:** Directly targets high-probability buyers with personalized top-selling DVD recommendations.
* **Automation:** Replaces manual staff suggestions with a scalable, data-driven recommendation workflow.
* **Enhanced Customer Engagement:** Delivers tailored product discoveries, improving customer satisfaction and repeat store visits.
