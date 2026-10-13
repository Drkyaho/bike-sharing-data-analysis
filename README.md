# Bike Sharing Data Analysis 🚲

## About the Project

This project explores bike-sharing rental patterns using historical data from Capital Bikeshare. The goal is to understand how bike rental demand varies across seasons, working days, holidays, and weather conditions, and how these patterns can provide useful insights for operational planning.

I worked on this project as part of my data analysis learning journey, using Python for data preparation, exploratory data analysis (EDA), and visualization. I also developed an interactive dashboard with Streamlit to make the analysis easier to explore.

## Business Questions

Bike rental demand can change depending on the season, daily routines, and weather conditions. Understanding these patterns can help bike-sharing operators make better decisions about bicycle availability and operational planning.

This analysis focuses on the following questions:

1. How does bike rental demand vary across seasons?
2. How does rental demand differ between working days and non-working days?
3. Is there a difference in rental demand between holidays and non-holidays?
4. How are weather conditions associated with changes in bike rental demand?

## Dataset

This project uses the Bike Sharing Dataset from Capital Bikeshare, which contains historical rental records.

The analysis uses two datasets:

- **`day.csv`** — daily bike rental data.
- **`hour.csv`** — hourly bike rental data.

The datasets include information about rental dates, seasons, working days, holidays, weather conditions, temperature, humidity, wind speed, and the number of casual, registered, and total rentals.

## Project Workflow

### 1. Data Collection and Understanding

I loaded the daily and hourly datasets using Pandas to understand their structure, available variables, and relevance to the business questions.

### 2. Data Assessment and Preparation

Before analyzing the data, I examined its quality and consistency. The preparation process included:

- Checking missing values and duplicate records.
- Reviewing data types and converting date columns to datetime format.
- Converting categorical variables into appropriate data types where needed.
- Examining rental counts and relevant variables to understand the dataset before analysis.

These steps helped prepare the data for exploratory analysis and visualization.

### 3. Exploratory Data Analysis (EDA)

I used descriptive statistics and visualizations to explore rental patterns and compare demand across different conditions.

The analysis covered:

- Rental demand across seasons.
- Rental patterns on working days and non-working days.
- Differences between holidays and non-holidays.
- The relationship between weather conditions and rental demand.

Pandas and NumPy supported data manipulation and analysis, while Matplotlib and Seaborn were used to create visualizations.

### 4. Interactive Dashboard

I developed an interactive dashboard using Streamlit to present the analysis in a more accessible format.

The dashboard helps users explore bike rental patterns based on factors such as season, working days, holidays, and weather conditions without having to run through the entire notebook.

## Key Findings and Business Insights

### 1. Seasonal Rental Patterns

Rental demand varied across seasons. Fall recorded the highest rental demand, followed by summer, while spring recorded the lowest demand in the analyzed dataset.

**Business implication:** Historical seasonal patterns can help operators anticipate periods of higher or lower demand and plan bicycle availability accordingly.

### 2. Working Days and Non-Working Days

The analysis showed differences in average rental demand between working days and non-working days, with working days recording a slightly higher average in the descriptive comparison.

**Business implication:** Operators should consider rental patterns across the entire week when planning bicycle availability rather than focusing only on working days.

### 3. Holidays and Non-Holidays

Rental demand was lower on holidays than on non-holidays in the analyzed data.

One possible explanation is that travel routines may change during holidays, including changes in regular commuting activity. However, this analysis identifies a pattern and does not establish its underlying cause.

**Business implication:** Historical holiday patterns may help operators anticipate changes in demand and adjust operational planning.

### 4. Weather Conditions

The analysis explored how rental demand varied under different weather conditions. Less favorable weather was generally associated with lower rental activity.

**Business implication:** Weather conditions can be considered alongside historical rental patterns when planning bicycle availability and daily operations.

*Note: These findings describe patterns observed in the dataset. They should not be interpreted as proof of causation or statistical significance.*

## Tools and Technologies

- **Programming Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Interactive Dashboard:** Streamlit
- **Development Environment:** Jupyter Notebook, Anaconda, Shell/Terminal

## Project Structure

```text
bike-sharing-data-analysis/
├── dashboard/
│   ├── dashboard.py
│   ├── day_data.csv
│   └── Helper Functions Analysis.py
├── data/
│   ├── day.csv
│   └── hour.csv
├── notebook.ipynb
├── requirements.txt
├── url.txt
└── README.md
```

## Getting Started

Follow the instructions below to set up the environment and run the dashboard locally.

### Prerequisites

- Python 3.10
- Anaconda or a compatible Python environment
- Git (optional, for cloning the repository)

### 1. Clone the Repository

```bash
git clone https://github.com/Drkyaho/bike-sharing-data-analysis.git
cd bike-sharing-data-analysis
```

### 2. Set Up the Environment

**Option A: Using Anaconda**

Create and activate the environment:

```bash
conda create --name main-ds python=3.10
conda activate main-ds
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

**Option B: Using Shell/Terminal with Pipenv**

Create a project directory and navigate into it if you have not cloned the repository:

```bash
mkdir proyek_analisis_data
cd proyek_analisis_data
```

If you have already cloned the repository, run the following commands from the repository directory instead.

Install and activate the Pipenv environment:

```bash
pipenv install
pipenv shell
```

Install the project dependencies:

```bash
pip install -r requirements.txt
```

### 3. Run the Streamlit Dashboard

Navigate to the dashboard directory:

```bash
cd dashboard
```

Run the application:

```bash
streamlit run dashboard.py
```

Open the local URL displayed in the terminal to access the dashboard in your browser.

### 4. Explore the Notebook

Open `notebook.ipynb` in Jupyter Notebook or Google Colab to explore the data preparation, exploratory analysis, and visualizations.

## Dependencies

The following packages are listed in the project's `requirements.txt`:

- `Babel==2.17.0`
- `matplotlib==3.10.1`
- `pandas==2.2.3`
- `seaborn==0.13.2`
- `streamlit==1.42.2`

Other dependencies may be included in the environment or installed transitively as required by the project.

## What I Learned

Through this project, I gained hands-on experience in preparing datasets, assessing data quality, exploring trends, comparing groups, and communicating findings through visualizations.

I also learned to connect analytical questions with practical business considerations and to interpret observed patterns carefully rather than assuming that relationships automatically imply causation.

This project strengthened my foundation in exploratory data analysis and helped me practice presenting data in a way that can support more informed decisions.

---

*Developed as part of my data analysis learning journey.*
