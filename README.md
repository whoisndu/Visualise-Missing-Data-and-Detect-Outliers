# Visualise-Missing-Data-And-Detect-Dutliers
## Visualizing Missing Data and Detecting Outliers
### **Introduction**
This Jupyter Notebook aims to visualize missing data in the City of Los Angeles crime dataset, starting from 2020. We would also attempt to visualize outliers in the data set and eliminate these outliers. The dataset contains comprehensive records of crime incidents sourced from original crime reports, some of which were originally typed on paper, leading to potential inaccuracies. For privacy reasons, address fields are limited to the nearest hundred blocks. While the data is generally reliable, any questions or concerns can be addressed through comments.

### **Dataset Description**
The dataset provided consists of various columns representing different attributes of crime incidents in Los Angeles. We will read the CSV file and perform an analysis to visualize the presence of missing data using Plotly. The original dataset can be found here: https://www.kaggle.com/datasets/venkatsairo4899/los-angeles-crime-data-2020-2023.

### **Steps**
1. Importing Libraries and Reading the Data
2. Exploring the Data
3. Visualizing Missing Data
4. Detecting Outliers using Isolation Forest
5. Detecting Outliers using Seasonal Hybrid ESD Test
6. Outlier Detection in Categorical Data based on Frequency Distributions

Outliers were detected primarily using machine learning techniques like the Isolation Forest Algorithm and Statistical outlier detection techniques like the seasonal hybrid ESD test. 

#### Detecting Outliers using Isolation Forest:
**Overview**: Isolation Forest is an unsupervised machine learning algorithm used for detecting outliers in datasets. It is particularly effective for high-dimensional datasets and works well when the majority of data points are close together, and outliers are few and far apart.

**When to Use Isolation Forest:**
- High-Dimensional Data: Isolation Forest performs well in high-dimensional datasets where traditional distance-based outlier detection methods struggle due to the curse of dimensionality.
- Few Outliers: If your dataset contains a small proportion of outliers compared to inliers, Isolation Forest is a good choice as it can efficiently identify those rare anomalies.
- Numerical Data: Isolation Forest works best with numerical data, so it is suitable for detecting outliers in continuous variables.
- No Prior Knowledge: Isolation Forest is an unsupervised method, meaning it does not require any labeled data for training, making it convenient when you lack labeled anomaly data.
- Quick Detection: The algorithm can be computationally efficient, making it suitable for large datasets with many features.

#### Detecting Outliers using Seasonal Hybrid ESD Test:

**Overview**
The Seasonal Hybrid ESD Test is a method for detecting outliers in time series data. It combines statistical and machine learning techniques to identify anomalies that deviate from the expected seasonal behavior.

**When to Use Seasonal Hybrid ESD Test**:
- Time Series Data: This method is specifically designed for detecting outliers in time series data, where observations are collected at successive time intervals.
- Seasonal Patterns: The Seasonal Hybrid ESD Test works best when the data exhibits seasonal or periodic patterns. It can identify outliers that deviate from the expected seasonal behavior.
- Environmental Data: It is commonly used in environmental monitoring, where data often exhibit seasonal fluctuations.
- Anomaly Detection in Time Series: If you need to identify unusual events or deviations from the regular patterns in your time series data, this method can be useful.

#### Outlier Detection in Categorical Data based on Frequency Distributions:

**Overview**

This method is used to detect outliers in categorical data by analyzing the frequency distribution of categories. It identifies categories that deviate significantly from the majority and might require further investigation or handling.

**When to Use Outlier Detection in Categorical Data**:
- Categorical Data: If your dataset contains categorical variables, such as area names, product categories, or customer segments, you can use this method to identify unusual or rare categories.
- Frequency Analysis: This method is based on frequency analysis, so it is particularly suitable when you want to analyze the distribution of categories and identify those with significantly higher or lower occurrences.
- Identifying Rare Events: Outlier detection in categorical data can help identify rare events, categories, or occurrences that may be of interest or concern.
- Preliminary Data Exploration: This method can be used as a preliminary step in data exploration to understand the distribution of categorical variables and uncover potential anomalies.

In summary, the choice of outlier detection method depends on the nature of your data and the specific problem you are trying to solve. Isolation Forest is effective for high-dimensional numerical data with few outliers, while the Seasonal Hybrid ESD Test is tailored for time series data with seasonal patterns. Outlier detection in categorical data is useful when dealing with categorical variables and analyzing the frequency distribution of categories. Consider the characteristics of your data and the type of outliers you expect to find when selecting the appropriate outlier detection technique.

The analysis provides valuable insights into data quality and potential anomalies in the crime dataset. This information can be used to guide data preprocessing, cleansing, and modeling processes in crime data analysis and forecasting. The methods demonstrated here can be applied to similar datasets for visualizing missing data and detecting outliers in various applications.
