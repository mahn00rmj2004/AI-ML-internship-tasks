# 🌍 Life Expectancy Dataset - Exploratory Data Analysis

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-brightgreen.svg)](https://pandas.pydata.org/)
[![Seaborn](https://img.shields.io/badge/Seaborn-Visualization-orange.svg)](https://seaborn.pydata.org/)
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Plotting-red.svg)](https://matplotlib.org/)
[![Kaggle](https://img.shields.io/badge/Dataset-Kaggle-20BEFF.svg)](https://www.kaggle.com/)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

&gt; **AI/ML Engineering Internship Task 1** | DevelopersHub Corporation  
&gt; **Objective:** Perform comprehensive data exploration and visualization on global Life Expectancy data  
&gt; **Dataset:** [Life Expectancy (WHO) - Kaggle](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who)

---

## 📋 Table of Contents

- [Overview](#overview)
- [Dataset Description](#dataset-description)
- [Technologies Used](#technologies-used)

---

## 🎯 Overview

This project demonstrates comprehensive data exploration and visualization techniques using the **Life Expectancy Dataset from Kaggle**. This real-world dataset contains health, economic, and demographic indicators from various countries over multiple years, providing rich opportunities for exploratory data analysis.

Through this analysis, I practiced essential data science workflows including data loading from external sources, handling missing values, statistical summarization, and creating meaningful visualizations to understand global health trends and their relationships with socioeconomic factors.

---

## 🌐 Dataset Description

| Attribute | Details |
|-----------|---------|
| **Dataset** | Life Expectancy (WHO) |
| **Source** | [Kaggle - WHO Statistical Data](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who) |
| **Samples** | ~2,938 observations (193 countries, 2000-2015) |
| **Features** | 22 columns (numeric & categorical) |
| **Target** | Life Expectancy (in years) |

**Key Features:**
- `Country` - Nation name
- `Year` - Year of observation (2000-2015)
- `Status` - Developed or Developing country
- `Life expectancy` - Target variable (life expectancy in years)
- `Adult Mortality` - Adult mortality rates (per 1000 population)
- `infant deaths` - Number of infant deaths per 1000 population
- `Alcohol` - Alcohol consumption per capita (liters)
- `percentage expenditure` - Expenditure on health (% of GDP)
- `Hepatitis B` - Hepatitis B immunization coverage (%)
- `Measles` - Measles reported cases (per 1000 population)
- `BMI` - Average Body Mass Index
- `under-five deaths` - Number of under-five deaths per 1000 population
- `Polio` - Polio immunization coverage (%)
- `Total expenditure` - Government health expenditure (% of total budget)
- `Diphtheria` - Diphtheria immunization coverage (%)
- `HIV/AIDS` - Deaths per 1000 live births HIV/AIDS (0-4 years)
- `GDP` - Gross Domestic Product per capita (USD)
- `Population` - Population size
- `thinness 1-19 years` - Prevalence of thinness (ages 10-19)
- `thinness 5-9 years` - Prevalence of thinness (ages 5-9)
- `Income composition of resources` - Human Development Index (0-1)
- `Schooling` - Number of years of schooling

---

## 🛠️ Technologies Used

```python
pandas        # Data manipulation and analysis
numpy         # Numerical computing
matplotlib    # Basic plotting and visualization
seaborn       # Statistical data visualization
warnings      # Warning management


## 🚀 Getting Started (Google Colab)

### Step 1: Download Dataset from Kaggle

1. **Create a Kaggle account** (if you don't have one)
2. **Download the dataset** from [Life Expectancy (WHO)](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who)
3. **Extract the CSV file** (`Life Expectancy Data.csv`)

### Step 2: Upload to Google Colab

#### Method 1: Direct Upload (Recommended)

```python
# Upload directly to Colab
from google.colab import files
import pandas as pd
import io

print("📤 Please upload the 'Life Expectancy Data.csv' file:")
uploaded = files.upload()

# Get filename and load data
filename = list(uploaded.keys())[0]
df = pd.read_csv(io.BytesIO(uploaded[filename]))

print(f"✅ Successfully loaded: {filename}")
print(f"📊 Dataset Shape: {df.shape}")