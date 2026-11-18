# Bike Sharing Data Analysis 🚲

## About the Project

This project analyzes historical bike-sharing rental data from Capital Bikeshare to understand how rental demand varies across different conditions, particularly seasons, working days, and holidays.

The analysis focuses on identifying rental patterns through data preparation, exploratory data analysis (EDA), descriptive statistics, and data visualization. The objective is to translate historical rental data into insights that can support operational planning and better bicycle availability management.

This project was developed as part of my data analytics learning journey using Python and its data analysis libraries.

## Business Questions

This analysis addresses two main business questions:

1. How does the season affect the total number of bike rentals?
2. Do holidays and working days influence bike rental demand?

Additional exploratory analysis examines rental patterns across years, months, weekdays, and weather conditions.

## Dataset

This project uses the Bike Sharing Dataset from Capital Bikeshare, consisting of two datasets:

| Dataset | Description | Records |
|---|---|---:|
| `day.csv` | Daily bike rental records | 731 |
| `hour.csv` | Hourly bike rental records | 17,379 |

The datasets contain information about:

- Date, season, year, and month.
- Holiday and working-day indicators.
- Weekday and hourly information.
- Weather conditions, temperature, humidity, and wind speed.
- Casual, registered, and total bike rentals.

The main target variable for this analysis is `cnt`, representing the total number of bike rentals.

## Project Workflow

### 1. Data Gathering

Loaded the daily and hourly datasets using Pandas to understand their structure, variables, and relevance to the business questions.

### 2. Data Assessment

Examined the datasets to identify potential data quality issues through:

- Checking dataset structures and data types.
- Identifying missing values.
- Checking duplicate records.
- Reviewing descriptive statistics.
- Validating total rental counts by comparing `cnt` against the sum of `casual` and `registered`.

The assessment confirmed that both datasets contained no missing values or duplicate records, and their total rental counts were consistent.

### 3. Data Cleaning and Preparation

Prepared the datasets for further analysis by:

- Converting date columns (`dteday`) into datetime format.
- Converting categorical variables, including season, year, month, holiday, weekday, working day, and weather conditions, into appropriate categorical data types.
- Mapping numerical category codes into descriptive labels to improve readability during analysis.

### 4. Exploratory Data Analysis (EDA)

Performed exploratory analysis using descriptive statistics and data visualization to identify rental patterns and relationships across different variables.

The analysis covered:

- **Seasonal Patterns:** Comparing average rental demand across four seasons.
- **Yearly Trends:** Examining differences in rental demand between 2011 and 2012.
- **Monthly Patterns:** Identifying months with higher and lower average rental activity.
- **Weekly Patterns:** Comparing rental demand across weekdays.
- **Weather Conditions:** Exploring how weather conditions relate to rental demand.
- **Holiday Patterns:** Comparing average rentals on holidays and non-holidays.
- **Working-Day Patterns:** Examining differences between working days and non-working days.
- **Weather Characteristics:** Exploring temperature and humidity distributions across seasons.

### 5. Visualization and Explanatory Analysis

Created visualizations to communicate the findings and answer the main business questions.

The visualizations include:

- Histograms to examine rental count distributions.
- Boxplots to compare rental distributions across seasons.
- Correlation heatmaps to explore relationships between numerical variables.
- Bar charts to compare average rental demand across seasons, holidays, and working days.

## Key Findings and Business Insights

### 1. Seasonal Rental Patterns

Fall recorded the highest average daily rental demand, followed by summer, winter, and spring.

| Season | Average Rentals |
|---|---:|
| Fall | 5,644 |
| Summer | 4,992 |
| Winter | 4,728 |
| Spring | 2,604 |

**Business Insight:**

Historical seasonal patterns can help bike-sharing operators anticipate periods of higher and lower demand and adjust bicycle availability accordingly.

### 2. Working Days and Non-Working Days

Working days recorded a slightly higher average rental demand than non-working days.

| Day Type | Average Rentals |
|---|---:|
| Working Days | 4,585 |
| Non-Working Days | 4,330 |

The difference is relatively small in the descriptive comparison.

**Business Insight:**

Operators should consider rental demand throughout the week rather than assuming that working days always generate substantially higher demand.

### 3. Holidays and Non-Holidays

Average rental demand was lower on holidays compared with non-holidays.

| Day Type | Average Rentals |
|---|---:|
| Non-Holidays | 4,527 |
| Holidays | 3,735 |

**Business Insight:**

Historical holiday patterns can help operators anticipate potential changes in rental demand and adjust operational planning accordingly.

### 4. Weather Conditions

The analysis showed differences in average rental demand across weather conditions.

- Clear or partly cloudy conditions recorded the highest average rental demand.
- Misty and cloudy conditions recorded lower average demand.
- Light rain and snow conditions recorded the lowest average rental demand.

**Business Insight:**

Weather conditions can be considered alongside historical rental patterns when planning bicycle availability and daily operations.

**Note:** These findings represent descriptive patterns observed in the dataset. They do not establish causation or statistical significance.

## Tools and Technologies

| Category | Tools |
|---|---|
| Programming Language | Python |
| Data Manipulation | Pandas, NumPy |
| Data Visualization | Matplotlib, Seaborn |
| Development Environment | Jupyter Notebook, Anaconda |

## Project Structure

```text
bike-sharing-data-analysis/
│
├── data/
│   ├── day.csv
│   └── hour.csv
│
├── notebook.ipynb
├── requirements.txt
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.x
- Jupyter Notebook
- Git (optional, for cloning the repository)

### 1. Clone the Repository

```bash
git clone https://github.com/Drkyaho/bike-sharing-data-analysis.git
cd bike-sharing-data-analysis
```

### 2. Install Dependencies

Install the required Python libraries:

```bash
pip install -r requirements.txt
```

Alternatively, install them individually:

```bash
pip install numpy pandas matplotlib seaborn jupyter
```

### 3. Run the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `notebook.ipynb` and run the cells sequentially to explore the data preparation, exploratory analysis, visualizations, and findings.

## What I Learned

Through this project, I gained practical experience in:

- Assessing data quality and preparing datasets for analysis.
- Working with daily and hourly datasets using Pandas.
- Performing exploratory data analysis to identify patterns and trends.
- Applying descriptive statistics to compare rental demand across different categories.
- Creating visualizations to communicate analytical findings.
- Translating data observations into practical business insights.

This project strengthened my understanding of the data analysis workflow, from data preparation and exploration to visualization and business-oriented interpretation.

---

*Developed as part of my Data Analytics learning journey.*
