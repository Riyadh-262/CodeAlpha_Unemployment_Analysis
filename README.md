Unemployment Analysis with Python
CodeAlpha Internship --- Task 2

This project explores unemployment trends in India using Python and the
supplied unemployment dataset. It examines changes over time, compares
rural and urban unemployment, investigates the period from March 2020
onward as the COVID period, and compares average unemployment rates
across regions.
Project Objectives
- Clean and prepare the unemployment dataset.
- Explore key statistical properties of the data.
- Visualize monthly unemployment trends.
- Compare rural and urban unemployment rates.
- Compare average unemployment before and during the COVID period.
- Identify regions with the highest and lowest average unemployment
  rates.
Dataset
File: Unemployment in India.csv

The original CSV contains 768 rows and 7 columns. After removing fully
empty rows, duplicate rows, and records missing required analysis
fields, the notebook reports a cleaned dataset of 740 rows and 7
columns.
  Column                                      Description
  Region                                    Indian state or region

  Date                                      Observation date

  Frequency                                 Reporting frequency

  Estimated Unemployment Rate (%)           Estimated unemployment rate

  Estimated Employed                        Estimated number of employed people

  Estimated Labour Participation Rate (%)   Estimated labour force
participation rate
Area                                      Rural or Urban classification
The data analyzed in the notebook spans May 2019 to June 2020.
Workflow and Methodology
1. Load the data
The notebook loads the CSV file into a pandas DataFrame.
2. Data cleaning
- Removes whitespace from column names.
- Drops fully empty rows and duplicate records.
- Converts Date into a datetime value using the %d-%m-%Y format.
- Removes extra whitespace from Area and Region.
- Converts the unemployment-rate column to numeric values.
- Drops records missing the date, region, area, or unemployment rate.
The notebook's recorded cleaned dataset has 740 rows and no missing
values in its remaining columns.
3. Exploratory data analysis
Uses describe() to inspect the numerical distribution and summary
statistics.
4. Monthly unemployment trend
Groups records by date and calculates the mean estimated unemployment
rate for each date. A line chart is generated and saved as
monthly_unemployment.png.
5. Rural versus urban comparison
Groups the data by date and area, then plots rural and urban
unemployment rates over time. The chart is saved as
rural_vs_urban.png.
6. COVID-period comparison
The notebook labels dates before 1 March 2020 as Pre-COVID and dates
from 1 March 2020 onward as COVID Period. It calculates and visualizes
the mean unemployment rate for each group. The chart is saved as
covid_impact.png.
7. Regional comparison
Calculates the average unemployment rate for each region, sorts the
results, and visualizes them in a bar chart. The chart is saved as
regional_unemployment.png.
8. Key insights
Prints the five regions with the highest and lowest average unemployment
rates.
Key Findings from the Notebook
Overall statistics
- Cleaned observations: 740
- Mean estimated unemployment rate: 11.79%
- Median estimated unemployment rate: 8.35%
- Maximum recorded estimated unemployment rate: 76.74%
Pre-COVID versus COVID period
  Period                                 Average unemployment rate
  Pre-COVID (before 1 March 2020)                            9.51%
COVID Period (1 March 2020 onward)                        17.77%

The average in the notebook's COVID-period group is higher than the
pre-COVID average. This is a descriptive comparison; it does not by
itself establish that COVID-19 was the sole cause of the increase.
Regions with highest average unemployment
  Region               Average rate
  Tripura                    28.35%
Haryana                    26.28%
Jharkhand                  20.58%
Bihar                      18.92%
Himachal Pradesh           18.54%
Regions with lowest average unemployment
  Region          Average rate
  Meghalaya              4.80%
Odisha                 5.66%
Assam                  6.43%
Uttarakhand            6.58%
Gujarat                6.66%

These figures are the outputs recorded in the supplied notebook.
Technologies Used
- Python
- pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook / Kaggle Notebooks
How to Run
Kaggle Notebooks
1. Upload unemployment-analysis-with-python.ipynb to Kaggle or open
   it in a Kaggle Notebook.
2. Add the Unemployment in India.csv dataset to the notebook.
3. Confirm the dataset path. The supplied notebook currently uses:
   df = pd.read_csv("/kaggle/input/datasets/riyadhdata262/unemployment-in-india-dataset/Unemployment in India.csv")
4. If your Kaggle dataset path is different, update the path in the
   CSV-loading cell.
5. Run all cells from top to bottom.
Run Locally
1. Keep the notebook and CSV file in the same folder.
2. Install the dependencies:
   pip install numpy pandas matplotlib seaborn jupyter
3. Change the CSV-loading line in the notebook to:
   df = pd.read_csv("Unemployment in India.csv")
4. Start Jupyter:
   jupyter notebook
5. Open unemployment-analysis-with-python.ipynb and run all cells.
Generated Visualizations
Running the notebook generates these image files:
- monthly_unemployment.png
- rural_vs_urban.png
- covid_impact.png
- regional_unemployment.png
Project Structure
unemployment-analysis/
├── Unemployment in India.csv
├── unemployment-analysis-with-python.ipynb
├── README.md
├── PROJECT_DESCRIPTION.md
├── monthly_unemployment.png
├── rural_vs_urban.png
├── covid_impact.png
└── regional_unemployment.png
The four PNG files are generated when the notebook is executed.
Limitations
- The dataset covers May 2019 to June 2020, so it does not describe
  current unemployment conditions.
- The COVID comparison is a simple before/after grouping based on 1
  March 2020, not a causal-impact study.
- The notebook performs descriptive analysis and visualization; it
  does not build a forecasting or predictive model.
- The notebook does not perform a dedicated seasonal decomposition or
  formal statistical significance test.

Author
Riyadh Hossain

Prepared for CodeAlpha Internship --- Task 2: Unemployment Analysis
with Python.
