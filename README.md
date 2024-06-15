# This repo contains two projects.
1. Project1: Melatonin Product Reviews: Data Cleaning and Analysis [Find in the miniproject.ipynb file]
2. Project 2: Population Data Cleaning and Preprocessing [Find in the info6105 folder]

# Project 1: Melatonin Product Reviews: Data Cleaning and Analysis

## Introduction
This project involves loading, cleaning, merging, and analyzing review data from multiple melatonin products with varying doses. The goal is to understand customer sentiment and identify key themes in the reviews.

## Data Preparation and Merging
- **Loading Data:** The data was loaded from multiple CSV files, each representing different melatonin products with varying doses.
- **Merging Data:** The files were merged into a single DataFrame to streamline analysis. Each file's dose information was manually specified and added to the DataFrame.

### Files and Doses
- `B07N46LTJJ_ZzzQuilPureZzzsMelatoninSleepAidGummies-2mg.csv`: 2mg
- `B07PF1SN5B_vitafusionMaxStrengthMelatoninGummySupplements-10mg.csv`: 10mg
- `B08CGYFB2Q_VitamaticMelatonin20mgTablets.csv`: 20mg
- `B079TD7HG2_NatrolMelatoninSleepAidGummy-10mg.csv`: 10mg
- `B08451719W_CarlyleMelatonin12mgFastDissolve300Tablets.csv`: 12mg

### Combined Data Columns
- **Product Title:** Identifies the product.
- **Review Rating:** Numerical rating given by the reviewer.
- **Review Text:** Text of the review.
- **Review Header:** Summary or title of the review.
- **Dose:** Melatonin dosage of the product.

## Sentiment Analysis
### Rating-Based Sentiment Categorization
- Reviews were classified into Positive, Neutral, or Negative based on review ratings:
  - Positive: Ratings 4-5
  - Neutral: Rating 3
  - Negative: Ratings 1-2

### TextBlob Analysis
- Utilized TextBlob to derive sentiment from the review texts, providing deeper insights into customer perceptions.

### Sentiment Distribution
- **Positive Reviews:** 5914
- **Negative Reviews:** 1226
- **Neutral Reviews:** 570
- Visualized the distribution of sentiments using a bar chart.

## Text Analysis Using TF-IDF
- Applied Term Frequency-Inverse Document Frequency (TF-IDF) to identify and score the most relevant words within the review texts.
- Highlighted key terms that are most influential in the reviews.

### Key Terms Analysis
- **Top Terms:**
  - Sleep, Great, Good, Works, Work, Taste, Product, Melatonin, Asleep, Night, Like, Well, Take, Gummies, Help, Flavor, Get, Really

### Visualization of Key Terms
- Created a word cloud to visualize the most frequently mentioned terms in the reviews, highlighting prominent themes.

## Conclusion
The project successfully loaded, cleaned, and merged review data from multiple melatonin products. Sentiment analysis and text analysis provided valuable insights into customer perceptions and key themes in the reviews. The cleaned and processed data is now ready for further analysis and visualization.

# Project 2: Population Data Cleaning and Preprocessing

## Introduction
This project involves cleaning and preprocessing population data for various states to make it suitable for analysis and visualization. The goal is to transform raw data into a format that is easy to analyze and derive insights from.

## Rationale
1. **Renaming Unnamed Column:** The first column lacked a clear name, making it difficult to reference. Naming it 'Category' clarifies its role as a descriptor for each row.
2. **Handling Missing Values:** Missing data can distort analyses. Removing rows where all state columns are null helps maintain data integrity without losing too much information.
3. **Data Types Conversion:** The dataset contained numeric values in string format. Converting them to numeric types is essential for any mathematical or statistical analysis.
4. **Reshaping Data:** The dataset was in a wide format, which can be unwieldy for analysis. Reshaping it into a long format makes it easier to manipulate and analyze, especially for state-wise comparisons.

## Methods and Tools
### Libraries and Functions
- **Pandas Library:** Used for data manipulation and cleaning.
  - `.rename()` to rename columns.
  - `.dropna()` to handle missing values.
  - `.melt()` to reshape the data.
- **Custom Function:** A custom function was created to convert percentage strings to float values.

### Process
1. **Loading Data:** The dataset was loaded from a CSV file.
2. **Renaming Columns:** The unnamed first column was renamed to 'Category'.
3. **Converting Data Types:** Numeric values were converted from string format to appropriate numeric types.
4. **Handling Missing Values:** Rows with all state columns null were removed.
5. **Reshaping Data:** The data was reshaped from a wide format to a long format for easier analysis.

## Results and Output
- **Cleaned Data:** The dataset is now free of formatting issues and in a suitable shape for analysis. Each row represents a unique data point with a clear category, state, and numerical value.
- **Reshaped Data:** The dataset has been transformed from wide to long format, making it easier to manipulate and analyze. This format facilitates state-wise comparisons and other analyses.

## Data Overview
The dataset includes various demographic metrics for different states, such as:
- **Total Population**
- **Gender Distribution (Male, Female)**
- **Median Age**
- **Race Distribution (e.g., White, Black or African American, Asian)**
- **Economic Indicators (e.g., Employed, Unemployed, Below Poverty Level)**

### Key Findings
1. **Total Population:** Distribution analysis showed a right-skewed distribution, indicating that most states have smaller populations, while a few have significantly larger populations.
2. **Gender Distribution:** Both male and female population percentages showed normal distributions centered around 50%, suggesting a roughly equal gender distribution across states.
3. **Median Age:** The histogram for median age indicated a relatively normal distribution, with most states having a median age clustered around the central value.
4. **Economic Indicators:** Histograms for employment and poverty levels showed variations in employment rates and economic disparities across states.

## Conclusion
Feel free to expand on these projects as you my see fit.
