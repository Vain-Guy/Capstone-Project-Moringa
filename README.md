# Aircraft Risk Assessment Analysis

## Project Overview

This project aims to support strategic procurement in the aviation industry by identifying **low-risk aircraft models** using historical accident data. The analysis is driven by the business need to reduce exposure to safety risks while investing in new aircraft for commercial and private operations.

## Business Understanding

### Problem Statement

The company lacks knowledge about the safety performance of different aircraft models. Without this, it may invest in aircraft with poor safety records, risking:

* Financial loss,
* Reputational damage,
* Regulatory hurdles.

### Objectives

* Identify aircraft makes and models with the **lowest incident frequency** and **injury severity**.
* Evaluate patterns based on **manufacturer**, **flight purpose**, **engine type**, and **weather conditions**.
* Generate **three actionable recommendations** for procurement.

### Success Criteria

* Delivery of **3 business-oriented recommendations**.
* An interactive dashboard to explore risk profiles.
* A well-documented Jupyter Notebook for stakeholders.

## Dataset Description

* **Source**: U.S. National Transportation Safety Board (NTSB)
* **Time Range**: 1962–2023
* **Records**: 88,889 rows × 31 columns
* **Format**: CSV

### Key Features

| Column Name             | Description                                       |
| ----------------------- | ------------------------------------------------- |
| `make`                  | Aircraft manufacturer                             |
| `model`                 | Aircraft model                                    |
| `make_model`            | Combined identifier of make and model             |
| `injury_severity`       | Level of injury/fatalities                        |
| `aircraft_damage`       | Severity of damage (e.g., Substantial, Destroyed) |
| `weather_condition`     | Visual vs Instrument meteorological conditions    |
| `purpose_of_flight`     | Business, Commercial, Instructional, etc.         |
| `broad_phase_of_flight` | Flight stage when accident occurred               |
| `engine_type`           | Type of engine (e.g., Reciprocating, Turbo Fan)   |
| `country`               | Location of incident                              |

## Data Preparation

### Cleaning Steps

* Standardized key categorical fields (`make`, `model`) using `.str.strip()` and case formatting.
* Created `make_model` for precise risk grouping.
* Addressed missing values via custom imputation or placeholders.
* Removed duplicate and irrelevant rows.

### Feature Engineering

* Engineered composite variables like `make_model`.
* Derived columns for visualization and risk ranking.

## Analysis Process

### 1. **Initial Data Exploration**

* Shape, null values, and datatype checks.
* Basic descriptive statistics.

### 2. **Univariate Analysis**

* Distribution of injuries, damage, and model frequencies.

### 3. **Bivariate & Multivariate Analysis**

* Cross-tabulations and visualizations:

  * `make_model × injury_severity`
  * `engine_type × aircraft_damage`
  * `purpose_of_flight × weather_condition`

### 4. **Risk Ranking**

* Aggregated aircraft models by severity and frequency of incidents.
* Ranked safest aircraft based on combined risk score logic.

## Visualizations & Insights

* Bar plots, pie charts, heatmaps (Seaborn & Matplotlib)
* Interactive timelines and line plots (Plotly)
* Custom dashboards for stakeholder exploration (optional extension)

## Project Structure

```
├── notebook.ipynb            # Main analysis notebook
├── Data/
│   └── AviationData.csv      # Raw dataset
└── README.md                 # Project documentation

## Author
Norman Mwapea Kodi
*Data Analyst | Ahnjin Analytics
