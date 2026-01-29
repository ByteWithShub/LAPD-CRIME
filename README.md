# LAPD Crime Data Analysis & Forecasting

This project explores Los Angeles Police Department (LAPD) crime data to uncover temporal patterns, victim trends, area-wise risk, and crime severity using exploratory data analysis, feature engineering, and forecasting techniques.

Beyond basic crime counts, the project introduces a Harm-Weighted Crime Index (HCI) to measure not just how often crime occurs, but how severe it is across areas and premises.

---

### Project Objectives

- Clean and preprocess raw LAPD crime data  
- Engineer date/time and victim-related features  
- Perform Exploratory Data Analysis (EDA)  
- Analyze crime trends by:
  - Time (hour, day, month)
  - Area
  - Premise
  - Victim age & gender  
- Build a Harm-Weighted Crime Index (HCI)  
- Identify high-risk locations and micro-time “hot windows”  
- Perform crime forecasting (Phase 3)

---

### Dataset

Source: Kaggle  
Dataset is downloaded directly inside the notebook using:
kagglehub.dataset_download("candacegostinski/crime-data-analysis")

The dataset contains:

- Crime type & description  
- Date & time  
- Area name  
- Premise description  
- Victim age, sex, descent  
- Weapon information  
- Modus operandi codes  

---

### Data Cleaning & Feature Engineering

Key preprocessing steps:

- Removed redundant identifiers and highly sparse columns  
- Handled missing values in victim attributes  
- Converted date/time into usable features:
  - Hour
  - Day of week
  - Month  
- Created age groups for victims  
- Mapped crime descriptions into broader crime categories  
- Simplified premise types into logical groups  

Special handling:

Records with Hour = 12 were excluded from micro-time analysis since 12:00 appeared to be a default placeholder for unknown times.

---

### Exploratory Data Analysis

### Time-Based Analysis
- Crime trends by hour, day, and month  
- Peak activity windows  

### Area & Premise Analysis
- Crime volume by LAPD area  
- Crime severity by premise type  

### Victim Analysis
- Age group vs crime category  
- Gender distribution  
- Exposure patterns  

---

### Harm-Weighted Crime Index (HCI)

Instead of relying only on crime counts, severity weights are assigned to each crime category to compute:

- Total incidents  
- Total harm score  
- Average harm per incident  

This highlights areas with fewer crimes but higher severity.

---

### Phase 3: Crime Forecasting

Time-series forecasting models crime trends to estimate future activity and support proactive decision-making.

---

### Tech Stack

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Plotly  
- Scikit-learn  

---

### Repository Contents

LAPD_CRIME.ipynb  
README.md  

---

### Key Takeaways

- Property theft dominates across age groups  
- Violent crimes cluster in specific areas and evening hours  
- Younger victims show higher exposure to harassment-related offenses  
- Severity-weighted analysis provides deeper insight than raw counts  
- Some premises have fewer incidents but much higher harm per crime  

---

Author: Shubhangi Singh  
GitHub: https://github.com/ByteWithShub
