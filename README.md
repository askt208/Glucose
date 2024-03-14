# Glucose 
Glucose assignment for Programming III

# Continuous glucose records
This repository contains the analysis of the contibuous continuous glucose datasets.
Purpose: to investigate the glucose level of a subject.

# Methodology
1. Data inspection: clean and process the data for analysis
2. Data and visual explorattion: data distributions and acossiation of different variables
3. Imputing: linear interpolation
4. Smoothing: moving windows
5. Statistical analysis: moving windows, find peaks
6. Visualization: line chatrs, interactive bokeh plot

## Verion
Python 3.11.5
Bokeh 3.2.1
Jupyter Notebook 6.5.4

# Data file
All data files are not included in this repository.
Description of each data file
 1. glucose.csv
    This file contains data of one case which is measured by the sensor, FreeStyle LibreLink device.
    This file contains several types of records. We are interested in the records that measure the continuous glucose values(mmol/L). 
    The data file can be found at assemblix2019:/data/datasets/Programming/glucose.csv
 Data description
 1. ID of the row.
 2. Date and time that indicates when the record was taken.
 3. Type of register. The type of registers can take the following values: 0: automatic glucose value register, saved each 15 minutes by the device. 1: manual blood glucose value register, 
    saved in the record after a read by the patient (for calibration purpose) 2: register of insulin without a numeric value. 3: register of carbohydrates without a numeric value. 4: 
    register of insulin done with a numeric value. 5: register of carbohydrates with a numeric value.
 4. Blood glucose value in rows with register type 0 (mg/dl).
 5. Blood glucose value in rows with register type 1 (mg/dl).
 6. Rapid insulin register without a numeric value in rows with register type 2.
 7. Carbohydrates without a numeric value in rows with register type 3.
 8. Units of rapid insulin entered by the patient in rows with register type 4.
 9. Units of carbohydrates entered by the patient in rows with register type 5.

    
# Conclusion
1. The glucose level reached the highest level at 00:00, and reached lowest level between 6am and 12pm. The subject may have the risk of extreme hypoglycemia in the morning.
2. The glucose level reached the lowest peak between 7am to 9am, and reached highest peak between 10pm and 11pm.
3. The pattern of glucose levels does not look different.

# Files
1. glucose_assignment.ipynb
    Jupyter notebook, to perform the complete analysis of the data
    
2. config.yaml
    The configuration file contains data path.

# Author
Mary(Pei-Shan) Wu
p.wu.2@st.hanze.nl

# References
[1] Elouafiq, I. Data & Experiments
[2] Clarke W, Kovatchev B. Statistical tools to analyze continuous glucose monitor data. Diabetes Technol Ther. 2009 Jun;11 Suppl 1(Suppl 1):S45-54. doi: 10.1089/dia.2008.0138. PMID: 19469677; PMCID: PMC2903980.

