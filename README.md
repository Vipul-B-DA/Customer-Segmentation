# Customer Segmentation using Unsupervised Learning

---

## Project Overview
This project is an end-to-end implementation of customer segmentation utilising unsupervised machine learning model and K-means clustering to segregate the given raw data into meaningful distribution chunks. The primary goal is to analyse a marketing campaign dataset to identify distinct customer groups based on their profiles and purchasing behaviours.

By leveraging unsupervised machine learning, specifically K-Means Clustering, this project demonstrates how to transform raw customer data into actionable business insights. The resulting segments allow businesses to understand their customer base on a deeper level, enabling personalised marketing, improved product development, and more effective customer engagement strategies. This repository serves as a practical, real-world example of a classical machine learning project for a data analyst portfolio.

---

## Project Motivation & Goals

### Why This Project- The Industry Need
In today's competitive market, businesses are shifting from mass marketing to personalized, data-driven strategies. Companies across all sectors (retail, e-commerce, finance, etc.) are investing heavily in understanding their customers to gain a competitive edge. This project directly addresses this industry need by demonstrating the ability to extract meaningful patterns from raw data and translate them into strategic business actions. It showcases a core competency that data analysts are expected to possess: turning data into value.


### What does Customer Segmentation helps us unravel?
Customer segmentation is one of the most fundamental and impactful applications of data science in business. Instead of treating the entire customer base as a single entity, segmentation allows a company to:

- **Allocate Marketing Resources Effectively**: Focus budget and effort on the most profitable or high-potential customer groups.

- **Enhance Customer Retention**: Identify at-risk customers or high-value segments and develop tailored retention campaigns.

- **Personalise the Customer Experience**: Deliver relevant product recommendations, offers, or even employ a reward system based on customer groups that resonate with specific customer needs.

### Aim:
The primary goal of this project is not just to build a machine learning model, but to provide a complete analytical solution. The specific aims are:

- To Identify Distinct Customer Personas: To move beyond raw data and identify 3-5 clear, understandable customer segments (e.g., "Loyal High-Spenders," "Budget-Conscious Shoppers").

- To Create Actionable Insights: To analyse the characteristics of each segment and provide clear recommendations for targeted marketing strategies.

- To Build a Reusable Framework: To create a documented, end-to-end workflow in a Jupyter Notebook that can be adapted for similar business problems in the future.

---

## Dataset Used:
The sample raw-unprocessed dataset is taken from GeeksForGeeks website in the csv file format, which enlists records of a marketing campaign of different customers detailing customer demographics, product preferences, and campaign engagement.

### Key features include:

- **Demographics**: `Year_Birth, Education, Marital_Status, Income, Kidhome, Teenhome`

- **Purchasing History**: `MntWines`, `MntFruits`, `MntMeatProducts`, etc.

- **Campaign Engagement**: `AcceptedCmp1, AcceptedCmp2`, `Response`

- **Customer Relationship**: `Dt_Customer`, `Recency`

---

## Technologies & Libraries Used:
- **Python**: Core for data analysis and modeling.
- **Pandas & NumPy**: For efficient data manipulation, cleaning, and numerical operations.
- **Matplotlib & Seaborn**: For creating insightful and comprehensive data visualizations.
- **Scikit-learn**: For the machine learning pipeline, including StandardScaler, TSNE, and KMeans.
- **Jupyter Notebook**: For creating a structured, reproducible, and well-documented analytical report.

---

## Project Working & Methodology:
This project follows a structured, multi-step data science workflow:

1. **Data Loading & Preprocessing**: Loaded the dataset, handled missing Income values by dropping the few affected rows (~1%), and engineered the `Dt_Customer` feature into numerical `day`, `month`, and `year` columns to ensure data quality for the model.

2. **Exploratory Data Analysis (EDA)**: Performed a deep dive using statistical summaries and visualisations to understand data distributions and uncover initial patterns. This step builds crucial business intuition before modelling.

3. **Feature Scaling & Engineering**: Standardised all numerical features using **StandardScaler**. This is a vital step for distance-based algorithms like K-Means, ensuring all features contribute equally to the result.

4. **Dimensionality Reduction (`t-SNE`)**: Applied t-SNE to reduce the high-dimensional data into a 2D representation, allowing for visual inspection of the data's natural clustering tendencies.

5. **K-Means Clustering**: Trained the K-Means algorithm with `n_clusters=5` on the scaled data to partition customers into distinct segments based on their characteristics.

6. **Visualisation & Interpretation**: Visualised the 5 identified clusters on a `2D scatter plot` and analysed the segments to translate the model's output into actionable business insights.

---

## Machine Learning Model Details:  


- **Model Selection** `K-Means`: Chosen for its efficiency, scalability, and ease of interpretation, making it a powerful baseline for customer segmentation tasks.

- **Hyperparameter Tuning** `K=5`: The number of clusters (K) was set to 5 based on the business case. The optimal K can also be found empirically using the Elbow Method by plotting the Within-Cluster Sum of Squares (WCSS).

- **Model Evaluation** `Inertia`: The model's performance is measured by its inertia (WCSS), which indicates how dense and internally coherent the identified clusters are. A lower value signifies better clustering.

- **Key Assumptions**: The model works best with spherical clusters and requires mandatory feature scaling. Its sensitivity to initial centroid placement is mitigated by Scikit-learn's multiple initialisations (n_init=10).

---

## Conclusion & Business Impact
This project successfully achieved its primary goal of identifying distinct customer segments from a raw marketing dataset. The end-to-end workflow, from data cleaning and EDA to model training and visualization, provides a comprehensive and reusable framework for tackling similar business problems. By grouping customers into 5 distinct personas, we have translated complex data into actionable business intelligence.

| Segment Persona                 | Key Characteristics                                                                                               | Recommended Business Strategy                                                                                             |
| :------------------------------ | :---------------------------------------------------------------------------------------------------------------- | :------------------------------------------------------------------------------------------------------------------------ |
| **3. Wealthy Seniors** | • **Highest Income** & High Spending <br> • Oldest age group (avg. 70) <br> • Likely retired with high disposable income. | Engage with premium product offerings (e.g., fine wines, gourmet food), and focus on comfort, quality, and catalog-based marketing. |
| **0. High-Value Spenders** | • High Income & **Highest Spending** <br> • Youngest age group (avg. 47) <br> • Likely professionals or DINKs (Dual Income, No Kids). | Target with loyalty programs, exclusive access to new products, and personalized digital marketing to maximize lifetime value.      |
| **2. Prudent Mid-Tier** | • Moderate Income & Moderate Spending <br> • Older age group (avg. 59) <br> • Consistent but cautious shoppers.        | Nurture with seasonal promotions, cross-selling opportunities, and content marketing to encourage higher purchase frequency. |
| **4. Family Bargain Hunters** | • Low-to-Moderate Income <br> • Mid-age group (avg. 54) <br> • Spending is responsive to deals and discounts.       | Target with family-focused bundle deals, value-based digital marketing, and promotions on everyday essentials to drive sales volume. |
| **1. Low-Income, Low-Spenders** | • **Lowest Income** & **Lowest Spending** <br> • Mid-age group (avg. 52) <br> • Infrequent or entry-level buyers.            | Drive initial engagement with welcome discounts, promotions on low-cost items, and educational content to build brand trust.       |


By tailoring marketing efforts to these specific segments, a business can significantly improve its return on investment (ROI), enhance customer satisfaction, and foster long-term loyalty.

---
## License


This project is licensec under the [MIT License](LICENSE). Feel free to use, share this repository under proper attribution.

