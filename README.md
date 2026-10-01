# ✈️ Flight Delay and Cancellation Analysis Using EDA

An exploratory data analysis project that studies airline departure delays, their operational patterns, and factors associated with flight punctuality.

## 📌 Project Overview

This project analyzes a real-world airline delay dataset containing **3,000,000 flight records and 32 features**. The main target variable is `DEP_DELAY`, representing departure delay in minutes.

The analysis focuses on understanding:
- How departure delays are distributed
- Differences in delay patterns across airlines
- The relationship between flight distance and delay
- How departure time affects delays
- Delay patterns across months and airlines
- The relationship between departure and arrival delays
- Routes and airlines associated with higher average delays

## 🎯 Objectives

1. Understand the structure and quality of the flight dataset.
2. Clean and prepare the data for analysis.
3. Handle missing values, cancelled flights, duplicates, and extreme delay values.
4. Perform univariate, bivariate, and multivariate EDA.
5. Identify operational patterns that may contribute to flight delays.
6. Summarize findings through pivot tables and visualizations.

## 📊 Dataset

**Dataset:** Airline Delay Dataset  
**Source:** Kaggle — Airline Delay Dataset  
**Records:** 3,000,000  
**Features:** 32  
**Target:** `DEP_DELAY`

`DEP_DELAY` is measured in minutes:
- Positive value → flight departed late
- Negative value → flight departed early

## 🧹 Data Preparation

The notebook includes the following preprocessing steps:

- Converted column names to lowercase for consistency.
- Removed cancelled flights because departure delay cannot be computed for them.
- Removed records where `dep_delay` was missing.
- Filled delay-reason columns with `0` where missing values represented no occurrence of that delay type.
- Removed `arr_delay` to reduce unnecessary noise for the selected analysis.
- Checked for duplicate records.
- Investigated extreme values in departure delay.

### Outlier Treatment

The dataset is naturally right-skewed. A strict IQR threshold produced an unrealistically low delay cutoff, so delays above that threshold were **not removed**.

Instead, extreme values were capped at the **99th percentile**, preserving realistic delay observations while reducing the influence of extreme values.

## 🔎 Exploratory Data Analysis

### Univariate Analysis

The project analyzes:
- Departure-delay distribution
- Flights by airline
- Flight-distance distribution

### Bivariate Analysis

The project explores:
- Airline vs. departure delay
- Flight distance vs. departure delay
- Departure time vs. departure delay

### Multivariate Analysis

The project includes:
- Correlation heatmap
- Airline and month vs. delay analysis
- Airline-level delay comparison
- Pivot tables for average delay by airline and month
- Top 10 worst routes

## 📈 Key Findings

Based on the notebook analysis:

- Most flights depart on time or with relatively small delays.
- Departure delay is strongly right-skewed.
- Some airlines show higher average delay and greater variability than others.
- Delays tend to increase later in the day.
- Flight distance shows little direct linear relationship with departure delay.
- Departure delay has a strong positive relationship with arrival delay.
- Late-aircraft-related delay shows a meaningful relationship with departure delay.
- Seasonal/monthly patterns are visible across airlines.
- The binary view of the target shows approximately **66% on-time/early flights and 34% delayed flights**.

## 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Exploratory Data Analysis
- Statistical analysis
- Data visualization

## 📂 Project Structure

```text
Flight-Delay-EDA/
│
├── Flight Delay-EDA project updated(1).ipynb
├── flights_sample_3m.csv
└── README.md
```

## ▶️ How to Run

1. Clone/download the project.
2. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Place the dataset in the location expected by the notebook, or update the `pd.read_csv()` path.
4. Open the notebook:

```bash
jupyter notebook
```

5. Run the cells from top to bottom.

## 💡 Business Applications

This analysis can support:
- Airline schedule planning
- Delay monitoring
- Operational performance analysis
- Airport congestion analysis
- Route-level performance studies
- Identifying recurring delay patterns

## 🚀 Future Improvements

- Build a machine-learning model to predict departure delays.
- Create an interactive Streamlit dashboard.
- Add airport-level congestion analysis.
- Perform time-series forecasting of delay trends.
- Develop airline-specific delay prediction models.

## 👩‍💻 Author

**Challa Swapna**

GitHub: `https://github.com/swapnachalla4826-sudo`
