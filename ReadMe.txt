Folder Structure:
Base folder -> datasets
	    -> code 

Within the Datasets folder, we have the follwing CSV files:
1. city_day
2. data_cleaned
3. Filled_data

The dataset contains 29,531 records spread over 16 features, representing daily air quality metrics for a number of Indian cities over some years.
Critical pollutants for study are PM2.5, PM10, NOx, and others, which are essential to get the composite AQI and AQI Bucket metrics calculated.

Within the Code folder, we have the following files:
1. AIT614_Sec005_Team8_Databricks1
2. AIT614_Sec005_Team8_JupyterNotebook
3. AIT614_Sec005_Team8_EDA
4. AIT614_Sec005_Team8_MLModels

Pre-requisites:
Databricks
Jupyter Notebook

Ensure you have a Python environment with libraries such as pandas, matplotlib, sklearn, numpy, pyspark and seaborn installed.

Section 1) How to Run AIT614_Sec005_Team8_Databricks1:

Step 1: Create a Cluster in databricks.
Step 2: Load 'AIT614_Sec005_Team8_Databricks1' file into Databricks.
Step 3: Upload the 'city_day' dataset to Databricks DBFS using spark library.
Step 4: Replace the dataframe 'df1' with the new dataframe.
Step 5: Run individual code cells in their respective order. You get the cleaned dataset.

Section 2) How to Run AIT614_Sec005_Team8_JupyterNotebook:

Step 1: For this file, use any python environment IDE like JupyterNotebook, VS Code, Pycharm, Collab (JupyterNotebook is preferred).
Step 2: Load 'AIT614_Sec005_Team8_JupyterNotebook' file into the Python Environment IDE.
Step 3: Upload the 'data_cleaned' dataset from the datasets folder using pandas. Replace the file path with the path of the dataset from your system.
Step 4: Run individual code cells in their respective order. You get the filled dataset.

Section 3) How to Run AIT614_Sec005_Team8_EDA:

Step 1: Create a Cluster in databricks.
Step 2: Load 'AIT614_Sec005_Team8_EDA' file into Databricks.
Step 3: Upload the 'Filled_data' dataset to Databricks DBFS using spark library.
Step 4: Replace the dataframe 'df1' with the new dataframe.
Step 5: Run individual code cells in their respective order. You get the graphs.


Section 4) How to Run AIT614_Sec005_Team8_MLModels:

Step 1: Create a Cluster in databricks.
Step 2: Load 'AIT614_Sec005_Team8_MLModels' file into Databricks.
Step 3: Upload the 'Filled_data' dataset to Databricks DBFS using spark library.
Step 4: Replace the dataframe 'df1' with the new dataframe.
Step 5: Run individual code cells in their respective order. You get the model results.

