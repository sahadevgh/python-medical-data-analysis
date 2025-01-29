# Medical Data Analysis

## Overview
This project was created as part of the **Application of Python Programming Assessment** for the **CSSD 601: Advanced Computation and Programming Using Python** course at **Ghana Communication Technology University (GCTU)**. The project focuses on analyzing patient vital signs using Python, identifying potential health trends, detecting anomalies, and generating statistical insights.

## Features
- **Data Loading:** Reads patient medical data from a CSV file.
- **Statistical Analysis:** Computes averages for key vitals (blood pressure, heart rate, body temperature, etc.).
- **Abnormal Reading Detection:** Flags vital signs that fall outside standard medical thresholds.
- **Trend Visualization:** Generates time-series plots for analyzing trends.
- **Report Generation:** Summarizes findings in a structured report.

## Dataset Structure
The dataset includes the following fields:
| Column Name | Description |
|-------------|-------------|
| Patient ID | Unique identifier for each patient |
| Age | Patient's age |
| Gender | Patient's gender (M/F) |
| Blood Pressure | Systolic blood pressure measurement (mmHg) |
| Heart Rate | Heartbeats per minute (bpm) |
| Body Temperature | Body temperature in Fahrenheit (°F) |
| Respiratory Rate | Breaths per minute (bpm) |
| Oxygen Saturation | Percentage of oxygen in the blood (%) |
| Date | Date of measurement |

## Standard Thresholds for Abnormal Readings
| Vital Sign | Normal Range | Abnormal Thresholds |
|------------|--------------|---------------------|
| Blood Pressure | 90/60 - 120/80 mmHg | Low: <90/60, High: >140/90 |
| Heart Rate | 60 - 100 bpm | Low: <60, High: >100 |
| Body Temperature | 97 - 99°F | Hypothermia: <96°F, Fever: >100.4°F |
| Respiratory Rate | 12 - 20 bpm | Low: <12, High: >20 |
| Oxygen Saturation | 95 - 100% | Low: <90% |

## Usage (Jupyter Notebook)
1. **Install Dependencies:**
   ```python
   !pip install pandas numpy matplotlib
   ```
2. **Load the Dataset and Run Analysis in Jupyter Notebook:**
   ```python
   import pandas as pd
   import numpy as np
   import matplotlib.pyplot as plt

   # Load the dataset
   medical_data = pd.read_csv("medical_data.csv")

   # Perform analysis...
   ```
3. **Output:**
   - Console output of statistics and flagged abnormalities.
   - Visual trend graphs for blood pressure and heart rate.
   - A structured report saved as a text file.

## Example Output
```plaintext
Healthcare Data Analysis Report
=================================
1. Average Vitals:
   Blood Pressure: 125 mmHg
   Heart Rate: 85 bpm
   Body Temperature: 98.3°F
   Respiratory Rate: 16 bpm
   Oxygen Saturation: 96%

2. Abnormal Readings:
   - 15 cases of high blood pressure
   - 8 cases of high heart rate
   - 5 cases of hypothermia

3. Trends:
   - Blood Pressure: Increasing trend in elderly patients
   - Heart Rate: Fluctuations observed in younger patients
```

## Contributing
Contributions are welcome! Feel free to submit a pull request or open an issue for suggestions.

## License
This project is licensed under the MIT License.