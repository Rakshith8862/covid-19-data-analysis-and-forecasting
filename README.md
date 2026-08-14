# covid-19-data-analysis-and-forecasting
COVID-19 Data Analysis and Time Series Forecasting using Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, and Prophet. Includes data cleaning, exploratory data analysis, interactive visualization, country-level analysis, and 14-day COVID-19 case forecasting.

# 🦠 COVID-19 Data Analysis & Forecasting with Python

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Plotly](https://img.shields.io/badge/Plotly-Interactive%20Visualization-3F4F75?logo=plotly)
![Prophet](https://img.shields.io/badge/Prophet-Time%20Series%20Forecasting-orange)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![License](https://img.shields.io/badge/License-MIT-green)

## 📌 Project Overview

This project analyzes the spread and impact of **COVID-19** using Python-based data analysis, visualization, and time-series forecasting techniques.

The project uses historical COVID-19 data containing information about:

* Confirmed cases
* Deaths
* Recovered cases
* Active cases
* Countries and regions
* Geographic coordinates
* WHO regions
* Dates
* Province/State information

The analysis explores how COVID-19 cases changed over time, compares countries based on their COVID-19 statistics, visualizes geographical differences, identifies countries with the highest number of active cases, and uses **Facebook Prophet** to forecast confirmed cases into the future.

The original project objective is to visualize the impact of COVID-19, analyze infection and recovery trends, and predict future cases based on historical trends.

---

## 🎯 Project Objectives

The main objectives of this project are:

1. Load and understand the COVID-19 dataset.
2. Perform initial data exploration.
3. Examine the structure and statistical properties of the dataset.
4. Clean and standardize important column names.
5. Analyze COVID-19 statistics on the first and last available dates.
6. Aggregate COVID-19 cases country-wise.
7. Compare COVID-19 deaths across countries.
8. Visualize geographical COVID-19 statistics using interactive Plotly maps.
9. Analyze confirmed cases over time.
10. Identify the top 20 countries with the highest active cases.
11. Analyze confirmed, recovered, and active cases as time series.
12. Build a time-series forecasting model using Prophet.
13. Forecast future confirmed COVID-19 cases.
14. Visualize the forecast and its components.

---

# 📊 Dataset

The project uses a COVID-19 dataset containing worldwide COVID-19 statistics.

The dataset contains:

* **49,068 records**
* **10 columns**
* Data from **January 22, 2020 to July 27, 2020**

The dataset columns are:

| Column           | Description                                  |
| ---------------- | -------------------------------------------- |
| `Province/State` | Province or state associated with the record |
| `Country/Region` | Country or region                            |
| `Lat`            | Latitude                                     |
| `Long`           | Longitude                                    |
| `Date`           | Date of the observation                      |
| `Confirmed`      | Cumulative confirmed COVID-19 cases          |
| `Deaths`         | Cumulative deaths                            |
| `Recovered`      | Cumulative recovered cases                   |
| `Active`         | Active COVID-19 cases                        |
| `WHO Region`     | WHO geographical region                      |

The dataset is represented in the repository by:

```text
covid_19 data.csv
```

Example dataset structure:

```text
Province/State,Country/Region,Lat,Long,Date,Confirmed,Deaths,Recovered,Active,WHO Region
,Afghanistan,33.93911,67.709953,2020-01-22,0,0,0,0,Eastern Mediterranean
,Albania,41.1533,20.1683,2020-01-22,0,0,0,0,Europe
,Algeria,28.0339,1.6596,2020-01-22,0,0,0,0,Africa
```

---

# 🗂️ Project Structure

Recommended GitHub repository structure:

```text
COVID-19-Analysis/
│
├── 📓 Covid_19_project.ipynb
│
├── 📊 covid_19 data.csv
│
├── 📄 README.md
│
└── 📁 images/
    ├── covid-map-first-day.png
    ├── covid-map-last-day.png
    ├── confirmed-cases-trend.png
    ├── top-20-active-cases.png
    ├── prophet-forecast.png
    └── prophet-components.png
```

### File descriptions

| File                     | Description                                       |
| ------------------------ | ------------------------------------------------- |
| `Covid_19_project.ipynb` | Complete Python analysis and forecasting notebook |
| `covid_19 data.csv`      | COVID-19 dataset used for the analysis            |
| `README.md`              | Project documentation                             |
| `images/`                | Optional screenshots/visualizations for GitHub    |

---

# 🛠️ Technologies Used

## Programming Language

* Python

## Data Analysis

* NumPy
* Pandas

## Data Visualization

* Matplotlib
* Seaborn
* Plotly Express

## Time-Series Forecasting

* Prophet

## Development Environment

* Jupyter Notebook
* JupyterLab
* Google Colab
* VS Code

---

# 📦 Python Libraries

The project uses the following major Python libraries:

```text
numpy
pandas
seaborn
matplotlib
plotly
prophet
```

---

# 💻 Installation Guide

## 1. Install Python

Make sure Python 3.x is installed on your computer.

Check your Python version:

```bash
python --version
```

or:

```bash
python3 --version
```

---

# 2. Clone the Repository

Open your terminal or command prompt and run:

```bash
git clone https://github.com/YOUR_USERNAME/COVID-19-Analysis.git
```

Move into the project directory:

```bash
cd COVID-19-Analysis
```

Replace:

```text
YOUR_USERNAME
```

with your GitHub username.

---

# 3. Create a Virtual Environment

Creating a virtual environment is recommended so that project dependencies remain isolated.

### Windows

```bash
python -m venv venv
```

Activate it:

```bash
venv\Scripts\activate
```

### macOS/Linux

```bash
python3 -m venv venv
```

Activate it:

```bash
source venv/bin/activate
```

---

# 4. Install Required Libraries

Install the required packages:

```bash
pip install numpy pandas seaborn matplotlib plotly prophet jupyter
```

You can also install them individually:

```bash
pip install numpy
pip install pandas
pip install seaborn
pip install matplotlib
pip install plotly
pip install prophet
pip install jupyter
```

---

# 5. Verify the Installation

Run:

```bash
python -c "import numpy, pandas, seaborn, matplotlib, plotly; from prophet import Prophet; print('All libraries installed successfully!')"
```

If the installation is successful, you should see:

```text
All libraries installed successfully!
```

---

# ▶️ How to Run the Project

There are two recommended ways to run this project.

---

## Option 1 — Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open:

```text
Covid_19_project.ipynb
```

Run the notebook cells from top to bottom.

---

## Option 2 — Google Colab

You can also upload the notebook to Google Colab.

Steps:

1. Open Google Colab.
2. Upload `Covid_19_project.ipynb`.
3. Upload `covid_19 data.csv`.
4. Update the CSV path in the notebook.
5. Run the cells sequentially.

---

# ⚠️ Important: Update the Dataset Path

The original notebook was created in Google Colab and contains a path similar to:

```python
df = pd.read_csv('/content/covid_19_clean_complete (1) (1).csv')
```

This path will generally **not work on another computer**.

For a GitHub repository, place the CSV in the same directory as the notebook:

```text
COVID-19-Analysis/
│
├── Covid_19_project.ipynb
└── covid_19 data.csv
```

Then change the loading code to:

```python
import pandas as pd

df = pd.read_csv("covid_19 data.csv")
```

If the dataset is inside a folder:

```text
COVID-19-Analysis/
│
├── Covid_19_project.ipynb
└── data/
    └── covid_19 data.csv
```

Use:

```python
df = pd.read_csv("data/covid_19 data.csv")
```

---

# 🔎 Step 1 — Import Libraries

The project begins by importing the required Python libraries:

```python
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import plotly.express as px
```

These libraries are used for:

* Numerical operations
* Data manipulation
* Data analysis
* Static visualization
* Interactive visualization

---

# 📥 Step 2 — Load the Dataset

The COVID-19 CSV file is loaded using Pandas:

```python
df = pd.read_csv("covid_19 data.csv")
```

Check the dataset:

```python
df
```

---

# 🧾 Step 3 — Understand the Dataset

The project uses several Pandas functions to understand the dataset.

### Dataset information

```python
df.info()
```

This provides:

* Number of rows
* Number of columns
* Column names
* Non-null values
* Data types
* Memory usage

The dataset contains:

```text
49068 rows
10 columns
```

---

## Dataset Shape

```python
df.shape
```

Expected result:

```text
(49068, 10)
```

---

## Statistical Summary

```python
df.describe()
```

This provides statistical information for numerical columns, including:

* Count
* Mean
* Standard deviation
* Minimum
* 25th percentile
* Median
* 75th percentile
* Maximum

---

# ✏️ Step 4 — Rename Columns

The notebook optionally standardizes the column names.

Original names:

```text
Province/State
Country/Region
Date
Confirmed
Deaths
Recovered
Active
```

They are renamed to:

```text
state
country
date
confirmed
deaths
recovered
active
```

Code:

```python
df.rename(
    columns={
        'Country/Region': 'country',
        'Date': 'date',
        'Province/State': 'state',
        'Confirmed': 'confirmed',
        'Deaths': 'deaths',
        'Recovered': 'recovered',
        'Active': 'active'
    },
    inplace=True
)
```

This makes the dataset easier to work with in Python.

---

# 📅 Step 5 — Analyze the First Available Date

The project identifies the first date available in the dataset.

```python
top_firstday = df[df['date'] == df['date'].min()]
```

The first available date is:

```text
2020-01-22
```

The data can then be aggregated country-wise:

```python
new_df_firstday = (
    top_firstday
    .groupby('country')[['confirmed', 'recovered', 'active', 'deaths']]
    .sum()
    .reset_index()
)
```

This creates a country-level summary for the first available date.

---

# 📅 Step 6 — Analyze the Last Available Date

The project also identifies the final date available in the dataset:

```python
top_lastday = df[df['date'] == df['date'].max()]
```

The final available date is:

```text
2020-07-27
```

Country-level aggregation:

```python
new_df_lastday = (
    top_lastday
    .groupby('country')[['confirmed', 'recovered', 'active', 'deaths']]
    .sum()
    .reset_index()
)
```

This allows the first and last available dates to be compared.

---

# 🔍 Step 7 — Check for Duplicate Records

The notebook checks for duplicate rows in the last-day dataset:

```python
top_lastday.duplicated().sum()
```

This helps identify whether duplicate records exist for the final observation date.

---

# 🌍 Step 8 — COVID-19 Deaths by Country

The project uses **Plotly Express** to create an interactive world map.

```python
fig = px.choropleth(
    new_df_lastday,
    locations='country',
    locationmode='country names',
    color='deaths',
    hover_name='country',
    range_color=[1, 50000],
    color_continuous_scale='Peach',
    title='Total Number of deaths country wise on 27th July'
)

fig.show()
```

The map allows users to interactively explore COVID-19 deaths by country.

---

# 🌍 Step 9 — First-Day COVID-19 Map

A similar choropleth map is created for the first available date.

```python
fig = px.choropleth(
    new_df_firstday,
    locations='country',
    locationmode='country names',
    color='deaths',
    hover_name='country',
    range_color=[1, 50000],
    color_continuous_scale='Viridis',
    title='Total Number of deaths country wise on 22nd January'
)

fig.show()
```

This provides a geographical view of deaths at the beginning of the dataset's time period.

---

# 📆 Step 10 — Convert Date Column

The original date column is converted into a Pandas datetime format:

```python
df['date'] = pd.to_datetime(df['date'])
```

The project then extracts the date portion:

```python
df['date'] = df['date'].dt.date
```

This makes the date easier to use for daily aggregation and time-series analysis.

---

# 📈 Step 11 — Confirmed Cases Over Time

The project aggregates confirmed cases by date:

```python
total_confirmeddeaths = (
    df.groupby('date')['confirmed']
      .sum()
      .reset_index()
)
```

Despite the variable name `total_confirmeddeaths` in the original notebook, this calculation represents **total confirmed cases**, not deaths.

The result is visualized using Matplotlib:

```python
plt.figure(figsize=(12, 8))

plt.bar(
    total_confirmeddeaths['date'],
    total_confirmeddeaths['confirmed'],
    color='red'
)

plt.xlabel('Date')
plt.ylabel('Confirmed Cases')
plt.xticks(rotation=45)

plt.show()
```

This visualization shows how confirmed COVID-19 cases changed over the available period.

---

# 🏆 Step 12 — Top 20 Countries by Active Cases

The project identifies the top 20 countries with the highest number of active cases on the final available date.

```python
top_20_country = (
    top_lastday
    .groupby('country')['active']
    .sum()
    .reset_index()
    .sort_values(by='active', ascending=False)
    .head(20)
)
```

The resulting dataset contains:

```text
20 countries
```

---

## 📊 Visualizing the Top 20 Countries

Seaborn is used to create a horizontal bar chart:

```python
plt.figure(figsize=(20, 50))

plt.title(
    'Top 20 countries having most active cases on 27th July'
)

sns.barplot(
    x=top_20_country.active,
    y=top_20_country.country
)

plt.xlabel('Active Cases')
plt.ylabel('Country')

plt.xticks(rotation=90)

plt.show()
```

This visualization makes it easier to compare countries based on their active COVID-19 cases.

---

# 📊 Step 13 — Time-Series Dataset Creation

The project creates three daily time-series datasets:

### Confirmed cases

```python
confirmed_cases = (
    df.groupby('date')
      .sum()['confirmed']
      .reset_index()
)
```

### Recovered cases

```python
recovered_cases = (
    df.groupby('date')
      .sum()['recovered']
      .reset_index()
)
```

### Active cases

```python
active_cases = (
    df.groupby('date')
      .sum()['active']
      .reset_index()
)
```

These datasets are used to understand the evolution of COVID-19 statistics over time.

---

# 🤖 Step 14 — Prophet Time-Series Forecasting

The project uses **Prophet** for time-series forecasting.

Import Prophet:

```python
from prophet import Prophet
```

Prophet requires two important columns:

```text
ds → date
y  → value being predicted
```

Therefore, the confirmed-case dataset is transformed:

```python
confirmed_cases.columns = ['ds', 'y']

confirmed_cases['ds'] = pd.to_datetime(
    confirmed_cases['ds']
)
```

---

# 🧠 Step 15 — Create the Forecasting Model

A Prophet model is created:

```python
model = Prophet(interval_width=0.95)
```

The `interval_width=0.95` setting specifies a 95% uncertainty interval for the forecast.

---

# 🏋️ Step 16 — Train the Model

The model is trained using the historical confirmed-case data:

```python
model.fit(confirmed_cases)
```

The model learns the historical time-series pattern from the available data.

---

# 🔮 Step 17 — Generate Future Dates

The project generates future dates using:

```python
future = model.make_future_dataframe(
    periods=14,
    freq='D'
)
```

The model is configured to forecast:

```text
14 future days
```

with:

```text
D = Daily frequency
```

---

# 📈 Step 18 — Generate Predictions

The trained Prophet model generates predictions:

```python
future = model.predict(future)
```

The forecast includes several important columns, including:

```text
yhat
yhat_lower
yhat_upper
```

Where:

| Column       | Meaning                    |
| ------------ | -------------------------- |
| `yhat`       | Forecasted value           |
| `yhat_lower` | Lower uncertainty estimate |
| `yhat_upper` | Upper uncertainty estimate |

---

# 🔢 Step 19 — Convert Forecast Values to Integers

The notebook converts the prediction values to integers:

```python
future[['yhat', 'yhat_lower', 'yhat_upper']] = (
    future[['yhat', 'yhat_lower', 'yhat_upper']]
    .astype(int)
)
```

The forecast can then be viewed using:

```python
future[['yhat', 'yhat_lower', 'yhat_upper']]
```

---

# 📉 Step 20 — Forecast Visualization

Prophet's built-in plotting functionality is used:

```python
confirmed_cases_plot = model.plot(future)
```

This visualization displays:

* Historical confirmed cases
* Forecasted cases
* Forecast uncertainty

---

# 📊 Step 21 — Forecast Components

The project also visualizes the components learned by Prophet:

```python
confirmed_cases_plot = model.plot_components(future)
```

This helps inspect the underlying components of the forecast.

---

# 🔄 Complete Workflow

The complete project workflow can be summarized as:

```text
                ┌─────────────────────┐
                │   COVID-19 Dataset  │
                │       CSV File      │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │     Load Data       │
                │       Pandas        │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   Data Inspection   │
                │ info / shape /      │
                │ describe / head     │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │   Data Preparation  │
                │ Rename columns      │
                │ Convert dates       │
                └──────────┬──────────┘
                           │
             ┌─────────────┼──────────────┐
             ▼             ▼              ▼
       First-Day       Last-Day       Time-Series
        Analysis       Analysis         Analysis
             │             │              │
             ▼             ▼              ▼
       Country-wise    Country-wise    Daily Cases
        Statistics     Statistics       Trends
             │             │              │
             └─────────────┼──────────────┘
                           ▼
                ┌─────────────────────┐
                │   Visualization     │
                │ Matplotlib /        │
                │ Seaborn / Plotly    │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Prophet Forecasting │
                │    14 Future Days   │
                └──────────┬──────────┘
                           │
                           ▼
                ┌─────────────────────┐
                │ Forecast & Component│
                │   Visualization     │
                └─────────────────────┘
```

---

# 📌 Key Analysis Performed

## 1. Dataset Exploration

The project examines:

* Dataset dimensions
* Data types
* Missing values
* Numerical statistics
* Dataset structure

---

## 2. First vs Last Date Analysis

The project extracts:

```text
First available date → 2020-01-22
Last available date  → 2020-07-27
```

Country-level statistics are generated for both dates.

---

## 3. Geographic Analysis

Interactive Plotly choropleth maps are used to visualize COVID-19 deaths across countries.

The maps allow users to:

* Hover over countries
* Compare countries
* Explore geographical differences
* Examine COVID-19 statistics interactively

---

## 4. Trend Analysis

Daily confirmed COVID-19 cases are aggregated and visualized to identify the overall growth trend.

---

## 5. Top Country Analysis

The project identifies the:

```text
Top 20 countries by active COVID-19 cases
```

on the last available date.

---

## 6. Forecasting

Prophet is used to forecast:

```text
Confirmed COVID-19 cases
```

for:

```text
14 future days
```

based on historical trends.

---

# 📷 Suggested GitHub Visualizations

For a more professional GitHub repository, save the major charts generated by the notebook into an `images/` directory.

Recommended images:

```text
images/
│
├── dataset-overview.png
├── deaths-first-day-map.png
├── deaths-last-day-map.png
├── confirmed-cases-trend.png
├── top-20-active-cases.png
├── prophet-forecast.png
└── prophet-components.png
```

You can then display them in this README using:

```markdown
## 🌍 COVID-19 Deaths by Country

![COVID-19 Deaths Map](images/deaths-last-day-map.png)
```

For the forecasting output:

```markdown
## 🔮 COVID-19 Forecast

![COVID-19 Forecast](images/prophet-forecast.png)
```

---

# 🚀 How Another User Can Use This Project

A user can reproduce the analysis on their own computer by following these steps:

### Step 1

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/COVID-19-Analysis.git
```

### Step 2

Enter the project:

```bash
cd COVID-19-Analysis
```

### Step 3

Create a virtual environment:

```bash
python -m venv venv
```

### Step 4

Activate the environment.

Windows:

```bash
venv\Scripts\activate
```

macOS/Linux:

```bash
source venv/bin/activate
```

### Step 5

Install dependencies:

```bash
pip install numpy pandas seaborn matplotlib plotly prophet jupyter
```

### Step 6

Start Jupyter:

```bash
jupyter notebook
```

### Step 7

Open:

```text
Covid_19_project.ipynb
```

### Step 8

Make sure the dataset path is correct:

```python
df = pd.read_csv("covid_19 data.csv")
```

### Step 9

Run the notebook cells sequentially.

---

# 🧪 Reproducing the Analysis with a Different Dataset

This project can be adapted to another COVID-19 dataset if it contains equivalent fields.

The main required variables are:

```text
Country/Region
Date
Confirmed
Deaths
Recovered
Active
```

If your dataset uses different column names, modify the column-renaming section.

For example:

```python
df.rename(
    columns={
        'Country': 'country',
        'Date': 'date',
        'ConfirmedCases': 'confirmed',
        'Deaths': 'deaths',
        'RecoveredCases': 'recovered',
        'ActiveCases': 'active'
    },
    inplace=True
)
```

The dataset should also contain a valid date column for time-series forecasting.

---

# ⚠️ Important Notes and Limitations

## Historical Dataset

This project uses a historical COVID-19 dataset covering January 22, 2020 through July 27, 2020.

Therefore, the analysis is a **historical data-analysis and forecasting project**, not a current COVID-19 monitoring system.

---

## Forecast Interpretation

Prophet predictions are based on historical patterns.

The forecast should not be interpreted as a guaranteed future outcome.

COVID-19 case numbers can be affected by many factors, including:

* Testing rates
* Reporting practices
* Government policies
* Public behavior
* Vaccination
* Variants
* Healthcare capacity
* Data-quality changes

These factors are not explicitly modeled in the notebook.

---

## Dataset Quality

The dataset contains country-level and province/state-level observations.

Some `Province/State` values are missing, while other fields are populated.

Therefore, aggregation should be performed carefully when adapting the project to other datasets.

---

# 🧩 Possible Improvements

The current project can be extended in several ways.

## 1. Improve Data Cleaning

Add:

* Missing-value analysis
* Duplicate detection across the complete dataset
* Outlier analysis
* Data validation
* Automated preprocessing

---

## 2. Add More Visualizations

Additional visualizations could include:

* Recovered vs confirmed cases
* Death rate
* Recovery rate
* Active case percentage
* Country comparison
* WHO region comparison
* Daily new cases
* Daily new deaths
* Daily recoveries

---

## 3. Improve Forecasting

Instead of forecasting only confirmed cases, separate Prophet models could be developed for:

```text
Confirmed Cases
Recovered Cases
Deaths
Active Cases
```

---

## 4. Add Model Evaluation

Forecast performance could be evaluated using:

* MAE
* MSE
* RMSE
* MAPE

This would provide a quantitative assessment of forecasting performance.

---

## 5. Build an Interactive Dashboard

The analysis could be converted into a dashboard using:

* Streamlit
* Dash
* Power BI

Possible dashboard filters:

```text
Country
Date
WHO Region
Province/State
```

---

## 6. Automate Data Updates

A future version could automatically obtain new COVID-19 data and refresh:

```text
Data → Analysis → Visualization → Forecast
```

---

# 📚 Skills Demonstrated

This project demonstrates practical experience with:

### Python

* Python programming
* Data manipulation
* Data processing

### Pandas

* Data loading
* Data inspection
* GroupBy
* Aggregation
* Sorting
* Date conversion
* DataFrame manipulation

### NumPy

* Numerical computing

### Matplotlib

* Static charts
* Bar charts
* Trend visualization

### Seaborn

* Statistical visualization
* Bar plots

### Plotly

* Interactive choropleth maps
* Geographic visualization

### Time-Series Analysis

* Date-based aggregation
* Historical trend analysis
* Forecasting

### Prophet

* Time-series model creation
* Model fitting
* Future dataframe generation
* Forecast generation
* Uncertainty intervals
* Forecast visualization
* Component analysis

---

# 💼 Project Relevance for Data Analyst Roles

This project demonstrates a complete data-analysis workflow:

```text
Raw Data
   ↓
Data Loading
   ↓
Data Inspection
   ↓
Data Cleaning
   ↓
Data Transformation
   ↓
Aggregation
   ↓
Exploratory Data Analysis
   ↓
Visualization
   ↓
Time-Series Analysis
   ↓
Forecasting
   ↓
Business/Analytical Insights
```

The project therefore demonstrates practical skills that are useful for a Data Analyst role, particularly:

* Data cleaning
* Exploratory data analysis
* Data visualization
* Trend analysis
* Time-series analysis
* Statistical thinking
* Python programming
* Data storytelling

---

# 📝 Project Summary

**COVID-19 Analysis with Python** is a data-analysis and forecasting project that examines the worldwide spread of COVID-19 using historical data.

The project uses **Pandas and NumPy** for data manipulation, **Matplotlib and Seaborn** for static visualizations, **Plotly** for interactive geographical analysis, and **Prophet** for time-series forecasting.

The analysis compares COVID-19 statistics across countries, examines confirmed-case trends, identifies countries with high active-case counts, and forecasts confirmed cases for the following 14 days based on historical trends.

---

# 👨‍💻 Author

**Rakshith S**

Data Analyst | Python | SQL | Power BI | Excel | Data Science

📍 Bengaluru, India

---

# ⭐ If You Found This Project Useful

If you found this project useful or interesting:

* ⭐ Star the repository
* 🍴 Fork the repository
* 🐛 Report issues
* 💡 Suggest improvements
* 🔗 Share the project

---

# 📄 License

This project is intended for educational and portfolio purposes.

You may modify and extend the project for learning and experimentation.

---

# 🙏 Acknowledgements

The project follows the original project requirements for analyzing COVID-19 trends using Python, including Pandas for data accumulation and analysis, Plotly for interactive visualization, and Prophet for time-series modeling.

---

# 🔗 Repository

```text
https://github.com/YOUR_USERNAME/COVID-19-Analysis
```

Replace `YOUR_USERNAME` with your GitHub username before publishing the repository.
