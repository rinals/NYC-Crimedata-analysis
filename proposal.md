# Final Project Proposal: Analyzing the Impact of Crime on Housing Prices in New York City

## 1. Project Overview

This project aims to explore the relationship between crime data and housing prices in New York City. I will use two datasets:
1. **NYPD Crime Data**: Provides detailed information about reported crimes, including the type of crime, location, and time of occurrence.
2. **NYC Housing Data**: Contains information on real estate transactions, including property prices, property characteristics (e.g., number of bedrooms, square footage), and neighborhood information.

By combining these datasets, the aim is to uncover patterns and relationships between crime rates and housing prices in various neighborhoods and boroughs of New York City. The project will use both **supervised** and **unsupervised** machine learning techniques, as well as **exploratory data analysis (EDA)** and **data visualizations** to present insights.

## 2. Datasets

### Dataset 1: NYPD Crime Data
- **File**: `NYPD_Complaint_Data_Current__Year_To_Date__20240920.csv`
  
### Dataset 2: NYC Housing Data
- **File**: `NY-House-Dataset.csv`

### Project Goal
The main objective is to:
1. **Analyze** crime trends in different boroughs and identify crime hotspots.
2. **Understand** how crime rates impact housing prices in New York City.
3. **Predict** housing prices using both real estate features and crime data.

## 3. Key Questions

1. **What are the most common types of crimes in each borough, and where are crime hotspots located?**
2. **How do housing prices vary across neighborhoods with high vs. low crime rates?**
3. **Can we predict housing prices based on real estate features and crime rates?**
4. **Can we use clustering to identify distinct neighborhoods based on crime rates and housing characteristics?**

## 4. Exploratory Data Analysis (EDA)

### Data Cleaning
- **Handling Missing Data**: Clean and drop any rows with missing or incomplete data from both datasets.
- **Date/Time Transformation**: Convert date columns (e.g., `CMPLNT_FR_DT`) into datetime format and extract useful time-related features (e.g., year, month, day).
- **Borough and Location Matching**: Ensure that both datasets have a consistent naming convention for boroughs (e.g., "Manhattan" vs. "New York") and geographic locations, so that the data can be merged.

### Data Merging
- **Merge Datasets**: Merge the crime and housing data based on the common location feature (e.g., borough or geographic coordinates). If detailed neighborhood information is available, merge by neighborhoods.

### Summary Statistics
- **Crime Analysis**: Calculate summary statistics for crime data, such as the most common crime types, total number of crimes per borough, and crime rates per neighborhood.
- **Housing Data Analysis**: Summarize housing price statistics, average prices per borough, and distributions of house sizes and bedrooms.

### Exploratory Visualizations
- **Crime Trends Over Time**:
  - Line charts to show crime trends over time (e.g., by month or year) across different boroughs.
- **Crime Type Distribution**:
  - Bar plots showing the distribution of crime types across boroughs.
- **Crime Hotspots**:
  - Heatmaps using latitude and longitude to visualize geographic crime hotspots.
- **Housing Prices**:
  - Boxplots to visualize the distribution of housing prices in different boroughs.
  - Scatter plots of housing prices vs. property features like square footage and number of bedrooms.
  
## 5. Machine Learning Models

### **Supervised Learning** (Predicting Housing Prices)
We will use **supervised machine learning** to predict housing prices based on both real estate features and crime data.

1. **Features**:
   - Property characteristics: `Square Footage`, `Bedrooms`, `Borough`
   - Crime-related features: Crime rates, most common crime type, proximity to crime hotspots.
   
2. **Modeling Approach**:
   - **Linear Regression**: To predict housing prices using features such as square footage, number of bedrooms, and crime rate.
   - **Random Forest Regressor**: To capture non-linear relationships between crime and housing prices.
   
3. **Evaluation**:
   - Use metrics like **R² score**, **Mean Absolute Error (MAE)**, and **Root Mean Squared Error (RMSE)** to evaluate the accuracy of the predictions.

### **Unsupervised Learning** (Clustering Neighborhoods)
We will apply **unsupervised learning** to group neighborhoods based on crime rates and housing prices, helping to identify distinct regions in NYC.

1. **K-Means Clustering**:
   - Group neighborhoods based on crime density and average housing prices.
   - Use latitude and longitude coordinates, average housing price, and crime rate as clustering features.
   
2. **Evaluation**:
   - Use **Silhouette Score** and **Inertia** to evaluate the quality of the clusters.
   
3. **Visualization**:
   - Visualize the clustered neighborhoods on a geographic map to show distinct crime-prone and high-value housing areas.

## 6. Tools and Technologies

- **Python Libraries**:
  - **Pandas** and **NumPy** for data manipulation and cleaning.
  - **Matplotlib** and **Seaborn** for data visualizations.
  - **Scikit-learn** for machine learning models (regression and clustering).
  
- **Visualization Tools**:
  - **Tableau** for interactive dashboards showing crime trends, housing price patterns, and the relationship between them.
  - **Plotly** or **Folium** for geographic visualizations of crime hotspots and housing prices.

## 7. Challenges and Considerations

1. **Data Alignment**: Ensuring that both datasets (crime and housing) can be accurately merged based on location (e.g., borough, neighborhood, or geographic coordinates).
2. **Feature Engineering**: Extracting meaningful features from the crime data, such as crime rates, common crime types, or proximity to crime hotspots.
3. **Data Imputation**: Handling missing or incomplete data in both datasets effectively, particularly where there are gaps in crime reporting or real estate transactions.

## 8. Conclusion

This project will provide insights into how crime rates impact housing prices in New York City by leveraging both **supervised** and **unsupervised** machine learning techniques. By integrating crime and housing data, we will analyze how real estate values are affected by crime patterns and develop predictive models to forecast future housing prices based on crime trends.

---

### Next Steps:
- **Step 1**: Clean and preprocess both crime and housing datasets.
- **Step 2**: Perform EDA to identify key trends and relationships between crime and housing.
- **Step 3**: Build machine learning models for predicting housing prices and clustering neighborhoods based on crime rates.
- **Step 4**: Visualize the results and insights using Tableau and Python visualization libraries.
