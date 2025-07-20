# Air Quality Index Analysis  
**How healthy is the air we breathe?**


## Table of Contents  
1. [Introduction](#introduction)  
2. [Objectives](#objectives)  
3. [Dataset](#dataset)  
4. [System Architecture](#system-architecture)  
5. [Data Preprocessing](#data-preprocessing)  
6. [Analytics Methods](#analytics-methods)  
7. [Installation](#installation)  
8. [Usage](#usage)  
9. [Results](#results)  
10. [Future Work](#future-work)  
11. [Contributing](#contributing)  
12. [License](#license)  
13. [Acknowledgements](#acknowledgements)  

---

## Introduction  
Air quality reflects how clean or polluted the air is, based on key pollutants (PM₁₀, PM₂.₅, NO₂, SO₂, CO). Poor air quality is linked to respiratory and cardiovascular issues and even ecosystem damage. This project leverages big‑data tools and predictive algorithms to fill gaps in historical records and uncover trends in urban and seasonal air quality across major Indian cities.

## Objectives  
- **Enhance understanding** of temporal and spatial air quality patterns influenced by urbanization, seasonality, and policy changes.  
- **Improve data integrity** by imputing and predicting missing values using median imputation and regression models.  
- **Develop predictive models** (e.g., Linear Regression, Random Forest) to forecast AQI values and evaluate performance via RMSE and R².

## Dataset  
- **Source:** Publicly available daily air quality records for multiple Indian cities (2015–2020).  
- **Size:** 29,531 records across 16 features (e.g., City, Date, AQI, PM₂.₅, PM₁₀, NOₓ, SO₂, CO, O₃, benzene, toluene).  
- **Key variables:**  
  - `City` (for spatial analysis)  
  - `Date` (for temporal trends)  
  - Pollutant concentrations (for composite AQI calculation)

## System Architecture  
1. **Data Ingestion:** CSV files loaded into PySpark DataFrames.  
2. **Preprocessing & Cleaning:**  
   - Standardize column names and data types.  
   - Handle missing values (median + regression imputation).  
3. **Modeling:**  
   - Feature selection based on pollutant health impact.  
   - Train/test split (80/20).  
   - Model training with Spark MLlib.  
4. **Evaluation & Visualization:**  
   - Compute RMSE, MAE, R².  
   - Generate plots in Jupyter Notebook for exploratory analysis.  

## Data Preprocessing  
1. **Load & Inspect:** Read CSVs, display schema, calculate missing‑value percentages.  
2. **Rename & Convert:** Harmonize column names; cast to appropriate types (e.g., `Date` → `DateType`).  
3. **Imputation:**  
   - Median imputation for simple gaps.  
   - Regression models to predict missing pollutant values.  

## Analytics Methods  
- **Descriptive Statistics:** Summary metrics (mean, median, std. dev.) for pollutants.  
- **Time Series Analysis:** Seasonal and trend decomposition of AQI.  
- **Correlation Analysis:** Relationships between AQI and meteorological factors.  
- **Predictive Modeling:**  
  - **Linear Regression** for baseline performance (R² ≈ 0.86, RMSE ≈ 52.6).  
  - **Random Forest** for non‑linear relationships (R² ≈ 0.89, MAE ≈ 25.9).

## Installation  

```bash
# 1. Clone this repository
git clone https://github.com/ka312/Air_quality_analysis.git
cd Air_quality_analysis

# 2. Create & activate a virtual environment
python3 -m venv venv
source venv/bin/activate   # on Windows: venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt
```

## Usage  

### Running the Analysis

1. **Exploratory Data Analysis (EDA):**
   ```bash
   jupyter notebook Code/AIT614_Sec005_Team8_EDA.ipynb
   ```

2. **Machine Learning Models:**
   ```bash
   jupyter notebook Code/AIT614_Sec005_Team8_MLModels.ipynb
   ```

3. **Databricks Implementation:**
   ```bash
   jupyter notebook Code/AIT614_Sec005_Team8_Databricks1.ipynb
   ```

### Data Files

The project includes the following datasets in the `Datasets/` folder:
- `city_day.csv` - Raw air quality data
- `data_cleaned.csv` - Cleaned and processed data
- `Filled_data.csv` - Data with imputed missing values

## Results  

### Key Findings

1. **Temporal Patterns:** Air quality shows clear seasonal variations with higher pollution levels during winter months.

2. **Spatial Distribution:** Urban areas consistently show higher AQI values compared to rural regions.

3. **Model Performance:**
   - Linear Regression: R² = 0.86, RMSE = 52.6
   - Random Forest: R² = 0.89, MAE = 25.9

4. **Pollutant Correlations:** Strong correlations observed between PM₂.₅ and PM₁₀ with overall AQI.

### Visualizations

The notebooks include comprehensive visualizations for:
- Time series plots of AQI trends
- Correlation matrices between pollutants
- Geographic distribution of air quality
- Model performance comparisons

## Future Work  

- **Real-time Monitoring:** Implement streaming data pipelines for live air quality monitoring.
- **Advanced Models:** Explore deep learning approaches (LSTM, GRU) for time series forecasting.
- **Geographic Expansion:** Extend analysis to include more cities and regions.
- **Policy Impact Analysis:** Study the effectiveness of environmental policies on air quality improvements.

## Contributing  

We welcome contributions! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Contribution Guidelines

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## Acknowledgements  

- **Data Source:** Public air quality datasets from Indian government sources
- **Tools & Libraries:** PySpark, Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

