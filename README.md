# Aviation Accident Analysis: Aircraft Safety Assessment (1983–2023)

## 1. Project Overview

This project analyzes aviation accident data to assess the safety performance of different aircraft manufacturers and models.

The analysis is conducted from the perspective of an aviation insurance company seeking to identify aircraft with relatively low rates of total destruction and serious or fatal injuries in recorded accidents.

The project was completed as part of the Moringa School Data Science Bootcamp.

## 2. Business Problem

An aviation insurance company requires evidence-based recommendations about the relative safety of professionally manufactured aircraft.

The analysis addresses the following questions:

- Which aircraft manufacturers have the lowest observed serious and fatal injury rates?
- Which aircraft models have the lowest destruction rates?
- How do safety outcomes differ between small and large aircraft?
- What accident-related factors, including weather conditions and flight phases, are associated with injury severity?
- Which aircraft manufacturers and models warrant further consideration by the insurer?

## 3. Dataset Description

The project uses historical aviation accident records from the AviationData dataset.

The analysis focuses on accidents occurring from 1983 onward, consistent with the client's assumed maximum aircraft model lifetime of 40 years.

Following initial data cleaning, the dataset contains:

- **66,851 accident records**
- **28 columns**
- Aircraft manufacturer and model information
- Aircraft damage and injury severity
- Engine characteristics
- Weather conditions
- Purpose and phase of flight

The cleaned dataset is saved as `data/AviationData_Cleaned.csv`.

## 4. Tools and Technologies

- **Python:** Data analysis and processing
- **Pandas:** Data cleaning, filtering, grouping, and aggregation
- **NumPy:** Numerical calculations
- **Matplotlib and Seaborn:** Data visualization
- **Jupyter Notebook and VS Code:** Development environment
- **Git and GitHub:** Version control and project documentation

## 5. Data Cleaning and Preparation

The cleaning process included:

1. Filtering records to the relevant analysis period.
2. Inspecting missing values and inconsistent data types.
3. Standardizing aircraft manufacturer and model names.
4. Removing aircraft manufacturers with fewer than 50 records during initial preparation.
5. Creating a combined aircraft manufacturer/model identifier.
6. Constructing a binary variable identifying destroyed aircraft.
7. Estimating total aircraft occupants and serious/fatal injury fractions.
8. Standardizing selected categorical variables, including engine type, weather conditions, and flight phase.
9. Removing selected columns with substantial missing information.
10. Saving the cleaned dataset for exploratory analysis.

Missing values were not automatically replaced with zero, since unknown information should not be interpreted as a confirmed absence of injuries or damage.

## 6. Exploratory Data Analysis

The analysis investigates aircraft safety using:

- Mean serious/fatal injury fraction
- Aircraft destruction rate
- Number of recorded accidents
- Manufacturer and model comparisons
- Small versus large aircraft comparisons
- Weather conditions and flight phases

Descriptive statistics, grouped aggregations, and visualizations are used to identify patterns in accident outcomes.

## 7. Key Findings

### Small Aircraft

Among the manufacturers examined, Aviat Aircraft Inc, Waco, Maule, Grumman Acft Eng Cor-Schweizer, and Diamond Aircraft Ind Inc showed relatively favorable observed injury outcomes.

Selected findings include:

| Manufacturer | Mean serious/fatal injury rate | Destruction rate |
|---|---:|---:|
| Aviat Aircraft Inc | 16.4% | 4.0% |
| Waco | 18.3% | 3.2% |
| Maule | 19.3% | 4.1% |
| Grumman Acft Eng Cor-Schweizer | 20.7% | 1.7% |
| Diamond Aircraft Ind Inc | 22.9% | 5.6% |

These results describe accident outcomes within the analyzed dataset rather than overall aircraft accident probabilities.

### Large Aircraft

The analysis also compared selected large-aircraft manufacturers.

| Manufacturer | Mean serious/fatal injury rate | Destruction rate |
|---|---:|---:|
| Embraer | 8.6% | 14.8% |
| Boeing | 9.2% | 16.5% |
| Airbus | 13.5% | 23.5% |

Embraer had the lowest observed mean serious/fatal injury fraction among these manufacturers, while Boeing had a larger injury sample.

### Individual Aircraft Models

Selected models with comparatively low observed serious/fatal injury fractions included:

- Diamond DA 20 C1
- Cessna 180J
- Piper PA-20
- Boeing 777
- Boeing 757
- Boeing 767

These model-level findings should be interpreted cautiously because some models have relatively few recorded accidents.

## 8. Data Visualizations

The project uses visualizations to communicate differences in aircraft safety outcomes, including:

- Comparisons of serious/fatal injury rates by aircraft manufacturer
- Aircraft destruction rate comparisons
- Distribution plots for aircraft injury outcomes
- Model-level safety comparisons
- Analysis of weather conditions and flight phases

These visualizations are available in the data analysis notebook.

## 9. Business Recommendations

Based on the observed accident outcomes:

1. **Small aircraft:** Consider further investigation of Aviat, Maule, and Grumman aircraft, while reviewing model-specific differences and sample sizes.
2. **Large aircraft:** Consider Embraer and Boeing for further evaluation based on the observed injury outcomes, while accounting for missing damage information and sample size.
3. **Model-level evaluation:** Assess individual models rather than relying exclusively on manufacturer-level averages.
4. **Insurance risk assessment:** Combine accident severity findings with aircraft utilization, fleet exposure, maintenance records, operating environment, and other risk factors before making underwriting decisions.

## 10. Limitations

This analysis has several limitations:

- Accident records do not provide total flight hours or departures for each aircraft model.
- Observed injury rates are conditional on a recorded accident.
- Missing aircraft category and damage information may introduce selection bias.
- Some aircraft models have relatively small samples.
- Aircraft age, maintenance, pilot experience, and operating conditions may influence accident outcomes.
- Historical accident patterns do not necessarily predict future aircraft safety performance.

Consequently, the findings should be treated as comparative historical evidence rather than definitive safety rankings.

## 11. Project Files

| File | Description |
|---|---|
| `Aviation_Accidents_Cleaning.ipynb` | Data cleaning and feature engineering |
| `Aviation_Accidents_Data_Analysis.ipynb` | Exploratory analysis, visualizations, and recommendations |
| `data/AviationData_Cleaned.csv` | Cleaned aviation accident dataset |
| `README.md` | Project documentation |

## 12. Conclusion

This project demonstrates how Python-based data cleaning, exploratory data analysis, and visualization can support aviation insurance risk assessment.

The results identify meaningful differences in observed accident severity across aircraft manufacturers and models. However, the analysis also highlights the importance of sample size, missing information, and exposure-adjusted safety measures.

The findings provide an initial evidence base for further aircraft safety evaluation and insurance underwriting decisions.

---

**Project:** Summative Lab — Data Analysis Jet Airline Safety

**Program:** Moringa School Data Science Bootcamp

**Author:** Diana Nashipae John