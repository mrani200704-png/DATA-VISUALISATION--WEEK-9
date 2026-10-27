# 🏡 House Sales Data Understanding, Cleaning & Feature Engineering

## 📌 Project Overview

This project focuses on understanding, cleaning, and analyzing the **King County House Sales Dataset** using Python. The dataset contains historical house sales information from King County, Washington, USA.

Real-estate prices depend on several factors, including the number of bedrooms and bathrooms, living area, lot size, construction year, renovation history, and geographical location. However, raw datasets may contain missing values, duplicate records, invalid entries, and extreme values that can affect analysis.

This project applies **Exploratory Data Analysis (EDA), Data Cleaning, Feature Engineering, Statistical Analysis, and Data Visualization** to prepare the dataset for property valuation analysis.

## 🎯 Objectives

- Understand the structure and characteristics of the dataset.
- Identify and handle missing values and duplicate records.
- Detect invalid and inconsistent property records.
- Convert sale dates into appropriate datetime formats.
- Create meaningful features from existing columns.
- Calculate price per square foot for living area and lot size.
- Detect potential outliers using the Interquartile Range (IQR) method.
- Visualize house prices and property characteristics.
- Analyze relationships between property features and sale prices.
- Prepare a clean dataset for further analysis and predictive modeling.

## 📂 Dataset Description

- **Dataset Name:** King County House Sales Dataset
- **Source:** Kaggle
- **Location:** King County, Washington, USA
- **Data Type:** Historical real-estate sales data

The dataset includes house sale prices, property characteristics, construction details, renovation information, and geographical coordinates.

### Important Columns

| Column Name | Description |
|---|---|
| `date` | Date of property sale |
| `price` | Sale price of the property |
| `bedrooms` | Number of bedrooms |
| `bathrooms` | Number of bathrooms |
| `sqft_living` | Interior living area in square feet |
| `sqft_lot` | Total land area in square feet |
| `grade` | Construction and design quality grade |
| `condition` | Overall condition of the property |
| `yr_built` | Year the property was constructed |
| `yr_renovated` | Year of renovation, if recorded |
| `waterfront` | Indicates waterfront access |
| `lat` | Latitude of the property |
| `long` | Longitude of the property |

**Note:** Download the dataset from Kaggle and place the CSV file in the project folder before running the analysis.

## 🛠️ Technologies Used

- **Python** – Programming language
- **Pandas** – Data manipulation and cleaning
- **NumPy** – Numerical calculations
- **Matplotlib** – Data visualization
- **Seaborn** – Statistical visualization
- **Jupyter Notebook / Google Colab / VS Code** – Development environments

## ⚙️ Project Workflow

### 1. Data Collection and Understanding

- Load the dataset using Pandas.
- Inspect the number of rows and columns.
- Examine column names and data types.
- Generate descriptive statistics.
- Understand the distribution of prices and property characteristics.

### 2. Data Cleaning and Preprocessing

- Identify missing values in relevant columns.
- Check and handle duplicate records.
- Investigate invalid bedroom and bathroom values.
- Validate sale prices, living areas, and lot sizes.
- Convert the sale date into datetime format.
- Correct data types where necessary.
- Investigate unusual records before correcting or excluding them.

### 3. Feature Engineering

New features are created to improve the analysis.

| New Feature | Description |
|---|---|
| `sale_year` | Year in which the property was sold |
| `sale_month` | Month in which the property was sold |
| `property_age` | Approximate age of the property at the time of sale |
| `is_renovated` | Indicates whether a renovation year is recorded |
| `years_since_renovation` | Approximate years since renovation at the time of sale |
| `price_per_sqft_living` | Sale price divided by living area |
| `price_per_sqft_lot` | Sale price divided by lot size |

These features help analyze the relationship between property characteristics, renovation history, and sale prices.

### 4. Price per Square Foot Analysis

- Calculate the price per square foot of living area.
- Calculate the price per square foot of lot size.
- Validate area values before performing division.
- Compare properties based on their unit valuation.
- Investigate unusually high or low valuation metrics.

### 5. Outlier Detection

The **Interquartile Range (IQR)** method is used to identify potential outliers.

The formulas are:

- IQR = Q3 − Q1
- Lower Bound = Q1 − 1.5 × IQR
- Upper Bound = Q3 + 1.5 × IQR

Box plots are used to examine extreme values in house prices and derived valuation features.

Potential outliers are investigated rather than automatically removed because some expensive properties may represent genuine high-value real estate.

### 6. Data Visualization

The following visualizations are included in the analysis.

| Chart Type | Columns | Purpose |
|---|---|---|
| Histogram | `price` | Understand the distribution of house prices |
| Histogram | `sqft_living` | Examine living area distribution |
| Box Plot | `price` | Identify potential extreme sale prices |
| Box Plot | `price_per_sqft_living` | Examine extreme living-area valuations |
| Box Plot | `price_per_sqft_lot` | Examine extreme lot-size valuations |
| Bar Chart | `bedrooms`, `price` | Compare average prices by bedroom count |
| Scatter Plot | `sqft_living`, `price` | Explore the relationship between living area and price |
| Bar Chart | `sale_year`, `price` | Examine annual average sale prices |

### 7. Feature and Data Quality Analysis

- Compare prices across different property age groups.
- Examine price differences between renovated and non-renovated properties.
- Investigate unusual room counts and area values.
- Review missing-value and duplicate-handling decisions.
- Assess the suitability of engineered features for further analysis.

## 📊 Expected Insights

The project aims to identify:

- The distribution and variation of house sale prices.
- The relationship between living area and sale price.
- Differences in average prices across bedroom counts.
- Annual changes in average sale prices.
- Potential valuation differences between older and newer properties.
- Possible associations between renovation history and house prices.
- Unusual property valuations that require further investigation.

These are analysis objectives, not predetermined findings. Actual insights will depend on the results obtained from the dataset.

## 📁 Project Structure

```text
House-Sales-Data-Analysis/
│
├── data/
│   └── kc_house_data.csv
│
├── notebooks/
│   └── house_sales_analysis.ipynb
│
├── output/
│   ├── cleaned_house_sales.csv
│   └── visualizations/
│
├── README.md
└── requirements.txt
```

*The folders and filenames above are a suggested structure. Adjust them to match the files in your repository.*

## 🚀 Installation and Execution

### Step 1: Clone the Repository

```bash
git clone <your-repository-url>
cd House-Sales-Data-Analysis
```

### Step 2: Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

Alternatively, if a `requirements.txt` file is available:

```bash
pip install -r requirements.txt
```

### Step 3: Download the Dataset

Download the King County House Sales Dataset from Kaggle and place `kc_house_data.csv` inside the `data` folder.

### Step 4: Run the Analysis

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Run the cells in `house_sales_analysis.ipynb` in sequence.

### Step 5: Review the Results

Inspect the cleaned dataset, engineered features, statistical summaries, visualizations, and documented data-quality decisions.

## 📈 Expected Outcome

The project produces a cleaned and structured dataset with meaningful derived features, statistical summaries, and visualizations. The prepared data can support further exploratory analysis and future property price prediction models.

## ⚠️ Limitations

- The dataset represents historical sales from a specific geographical region.
- Historical prices may not reflect current market values.
- Extreme values may represent genuine luxury properties rather than data errors.
- Missing or unrecorded renovation years may limit renovation analysis.
- Correlations between property characteristics and prices do not necessarily indicate causation.
- The project focuses on data preparation and analysis; predictive modeling is not required for its main objectives.

## 🏁 Conclusion

This project demonstrates the importance of data cleaning, exploratory data analysis, feature engineering, and outlier investigation in real-estate valuation.

By transforming raw house sales data into a structured dataset, the analysis helps reveal patterns in property prices and characteristics. The resulting dataset can be used for further statistical analysis and future machine learning applications.

## 👩‍💻 Author

**Maharani Magarasi V.**


---

