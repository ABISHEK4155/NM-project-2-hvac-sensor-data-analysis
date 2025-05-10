

# HVAC Sensor Data Analysis

**By ABISHEK V**
2nd Year B.E. Mechanical Engineering
ARM College of Engineering & Technology
Course: Data Analysis in Mechanical Engineering

---

## Introduction

This project focuses on analyzing sensor data from an HVAC (Heating, Ventilation, and Air Conditioning) system. The main goal is to understand how different factors like temperature, humidity, air flow, CO₂ levels, occupancy, and energy consumption interact with each other. By studying this data, we can find useful patterns that help in making HVAC systems more energy efficient and comfortable for indoor environments.

This analysis can help in:

* Detecting trends in HVAC performance.
* Spotting times or conditions that lead to high energy use.
* Assisting in decisions for better system maintenance or automation.

---

## About the Dataset

The dataset contains time-based sensor readings from an HVAC system. Below is a summary of the features included:

| Feature Name              | Description                                 |
| ------------------------- | ------------------------------------------- |
| Date\_Logged              | Time when the data was recorded             |
| Temperature (C)           | Room temperature in Celsius                 |
| Humidity (%)              | Relative humidity inside the room (%)       |
| Air\_Flow (CFM)           | Air flow rate in cubic feet per minute      |
| CO2\_Level (ppm)          | CO₂ concentration in parts per million      |
| Occupancy                 | Number of people in the room at that time   |
| Energy\_Consumption (kWh) | Energy used by HVAC system in kilowatt-hour |

---

## Data Preprocessing

To get the dataset ready for analysis, the following steps were taken:

1. **Importing and Reviewing the Data**
   The dataset was loaded using Python’s pandas library. I explored the basic structure and checked for any obvious issues.

2. **Handling Date and Time**
   The `Date_Logged` column was converted into proper datetime format so that I could analyze changes over time.

3. **Dealing with Missing Data**
   Some columns like `CO2_Level` and `Air_Flow` had missing values. These were filled in using the average of each column.

4. **Creating New Features**
   I created two new columns to help with time-based analysis:

   * **Hour**: to see trends across the day
   * **DayOfWeek**: to check for differences between weekdays and weekends

---

## Exploratory Data Analysis (EDA)

I used graphs and plots to understand how different factors are related. Some of the key observations include:

* **Daily Trends**

  * Energy consumption shows a pattern, usually increasing during daytime work hours.
  * CO₂ and temperature also seem to increase with occupancy.

* **Correlation Checks**

  * There’s a noticeable link between energy use and both temperature and airflow.
  * CO₂ levels are strongly connected to the number of people in the room.

* **Data Distributions**

  * Histograms and box plots showed some skewed data and possible outliers, especially in energy usage.

---

## Key Findings

Here are some of the most important things I learned from the analysis:

* **CO₂ Levels Depend on Occupancy**
  As more people enter the room, CO₂ levels rise quickly.

* **Air Flow Adjusts Automatically**
  Air flow increases when more people are present, which shows that the HVAC system adjusts based on demand.

* **Energy Use Peaks at Specific Times**
  The system tends to use the most energy between 9 AM and 6 PM, which matches typical office hours.

* **Stable Indoor Conditions**
  Temperature and humidity didn’t vary too much, suggesting that the system works well in keeping the environment consistent.

---

## What’s Next

In future work, I plan to:

* Use methods like the IQR technique to find and remove any extreme or faulty sensor data.
* Try building simple models to predict energy consumption or identify abnormal HVAC behavior.

---

## Tools and Technologies Used

* **Python (Pandas, NumPy)** – for loading and cleaning data
* **Matplotlib, Plotly** – to create graphs and visualizations
* **Jupyter Notebook** – used as the development environment

