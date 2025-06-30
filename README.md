# Aircraft Risk Profiling for Aviation Investment

## Overview

This project supports a strategic aviation initiative by providing data-driven insights into aircraft safety. By analyzing over 60 years of historical accident data from the National Transportation Safety Board (NTSB), I identify low-risk aircraft models suited for commercial and private deployment.

The aim is to reduce investment risk and operational hazards by recommending aircraft with superior safety performance.

## Business Understanding

A company is entering the aviation sector and must select aircraft models for its fleet. However, without knowledge of historical accident patterns and aircraft safety records, the organization risks acquiring models associated with frequent or severe accidents.

### Business Problem
There is no existing framework within the organization to assess aircraft risk. A poor investment decision could result in:

- Financial loss  
- Regulatory complications  
- Reputational damage  

### Objective
To provide three actionable, data-backed recommendations on the safest aircraft models using historical accident data.

### Goals
- Identify aircraft with low fatality and damage rates
- Compare risk across manufacturers and flight contexts
- Guide procurement through evidence-based analysis

## Data Understanding and Analysis

### Data Source
- **Provider**: National Transportation Safety Board (NTSB)
- **Format**: CSV
- **Size**: 88,889 records, 31 columns
- **Time Span**: 1962–2023

### Key Variables
| Column | Description |
|--------|-------------|
| `make`, `model` | Manufacturer and model |
| `aircraft_damage` | Degree of damage incurred |
| `injury_severity`, `total_fatal_injuries`, `total_uninjured` | Impact on passengers and crew |
| `purpose_of_flight` | Reason for the flight (e.g., Personal, Business) |
| `broad_phase_of_flight` | Phase during which the incident occurred |
| `weather_condition` | Meteorological conditions at time of event |
| `engine_type`, `number_of_engines` | Aircraft specifications |
| `amateur_built` | Whether aircraft was home-built |

### Data Quality Summary
- **Missing Values**: Found across several columns, handled through context-aware cleaning
- **Inconsistent Categorical Values**: Standardized for clarity and grouping
- **Outliers**: Identified and reviewed for fields like fatalities, number of engines and date entries

### Analytical Approach
1. **Data Cleaning**: Null handling, deduplication, normalization
2. **Exploratory Data Analysis (EDA)**:
   - Accidents by model and make
   - Fatality rates by flight phase and weather
   - Uninjured survival trends by flight purpose
3. **Risk Metrics Construction**: Combining severity and frequency
4. **Ranking and Recommendations**: Aircraft models evaluated for procurement suitability

## Conclusion

This analysis offers three primary business recommendations:

1. **Prioritize aircraft models with minimal fatality and damage records** over long operational histories.
2. **Avoid aircraft associated with recurring high-severity incidents**, especially during critical flight phases like landing and takeoff.
3. **Favor aircraft used successfully in business and commercial contexts**, with high rates of uninjured outcomes.

The project delivers:
- A fully annotated Jupyter Notebook for technical review  
- A Tableau dashboard for executive exploration *(link to be added)*  
- A concise report suitable for strategic decision-making  

**Author**: Norman Mwapea 

E-mail: normanmwaps@gmail.com  
Tools Used: Python, Pandas, Matplotlib, Seaborn, Plotly, Tableau, Jupyter Notebook

