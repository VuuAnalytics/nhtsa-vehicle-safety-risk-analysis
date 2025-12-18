# NHTSA Vehicle Safety Risk Analysis

## Project Overview
This project analyzes 1M+ NHTSA vehicle safety complaints to identify the highest-risk vehicle components, recurring mechanical failure conditions, and manufacturer-level defect trends using severity-weighted risk scoring.

Rather than relying on raw complaint volume alone, this analysis incorporates injuries, fatalities, crashes, and fires to surface true safety risk and guide targeted interventions.

---

## Business Problem
Consumer vehicle complaints contain critical safety signals, but complaint volume alone does not reflect true risk. High-frequency issues may be low severity, while rare issues may pose extreme danger.

Automakers and regulators need a way to prioritize defects that cause the most harm, not just the most noise.

---

## Problem Statement
How can we pinpoint the components, failure conditions, and vehicle populations driving the most severe safety complaints so automakers can reduce monthly NHTSA complaints by 10 percent within one year?

---

## Data
- Source: National Highway Traffic Safety Administration (NHTSA)
- Records: 1M+ consumer vehicle complaints
- Time Range: 2015–2025

### Key Fields
- Manufacturer  
- Model  
- Model Year  
- Component  
- Complaint Description  
- Injuries  
- Deaths  
- Crashes  
- Fires  

---

## Methodology
- Cleaned and standardized 1M+ NHTSA complaint records using Python
- Engineered a severity-weighted risk index incorporating deaths, injuries, crashes, and fires
- Normalized results to avoid bias from vehicle age and raw complaint volume
- Performed component-level, model-year, and manufacturer-level risk analysis
- Extracted recurring mechanical failure themes using keyword analysis on complaint text

---

## Analytical Framework

### Branch 1 – Component Risk Interpretation
Identifies the highest-risk vehicle components using a weighted severity index that blends complaint volume with injuries, deaths, crashes, and fires.

**Key Findings**
- Air Bags show the highest severity per complaint due to injury and fatality concentration
- Engines have the highest overall risk due to massive complaint volume and chronic failures
- Electrical Systems consistently rank high across multiple severity dimensions

---

### Branch 2 – Recurring Mechanical Failure Conditions
Analyzes complaint text to identify recurring mechanical failure themes across high-risk components.

**Key Findings**
- Fail, Oil, Power, Stall, and Brake are the most common recurring failure themes
- The same failure conditions appear across multiple components, suggesting shared design or engineering weaknesses
- Normalized keyword rates reveal which failures persist beyond high complaint volume

---

### Branch 3 – Model Year Defect Patterns
Identifies model years and brand-model-year combinations with disproportionately high defect risk after normalizing for vehicle age.

**Key Findings**
- Normalization reveals true problem years, not just older vehicles with more time on the road
- Certain production years repeatedly surface across engine, electrical, and powertrain failures
- Highlights the worst model year for each high-risk component and the top 15 highest-risk combinations overall

---

### Branch 4 – Manufacturer Defect Trends
Determines the dominant defect component for each manufacturer and how much of the brand’s total complaint volume it represents.

**Key Findings**
- Ford, Hyundai, and Chevrolet are dominated by Engine-related defects
- Honda, Jeep, Volkswagen, and Mercedes-Benz show high dependency on Electrical System issues
- Subaru stands out with Visibility/Wiper dominance
- Tesla shows elevated Forward Collision Avoidance complaints, reflecting software-heavy defect patterns
- Many brands have a single component responsible for 20–30 percent of total complaints

---

## Overall Insight
Together, the four analytical branches form a unified strategy for reducing national complaint volume:

1. Identify the highest-risk components  
2. Identify recurring mechanical failure conditions  
3. Identify high-risk model years  
4. Identify each manufacturer’s dominant defect category  

This layered approach enables targeted, high-impact interventions rather than broad, unfocused recalls.

---

## Tools Used
- Python (Pandas, NumPy)
- Jupyter Notebook
- Data cleaning and feature engineering
- Exploratory analysis and visualization

---

## Outcome
This analysis produces ranked, severity-weighted safety risk insights suitable for:
- Executive and regulatory review
- Manufacturer defect prioritization
- Model-year-specific recalls
- Supplier and engineering corrective actions
- Downstream dashboard and reporting applications

By focusing on the right components, vehicles, and failure conditions, automakers can realistically reduce monthly NHTSA complaints by 10 percent within one year.
