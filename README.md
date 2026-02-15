# Data_Analysis_Jet_Airline_Safety
Summative Lab

# Aviation Accident Safety Analysis

## Project Overview
This project analyzes U.S. aviation accident data to provide **safety-oriented recommendations** for aircraft makes and models. The client requires **separate recommendations for small and large airplanes**, with safety measured through passenger injury severity and aircraft destruction outcomes.

Airplanes are split using a **passenger threshold of 20**:
- **Small airplanes:** ≤ 20 passengers  
- **Large airplanes:** > 20 passengers  

---

## Data & Methods
- Cleaned dataset: `AviationData_Cleaned.csv`
- Cleaning and feature engineering performed in `Aviation_Accidents_Cleaning_Completed.ipynb`
- Analysis performed in `Aviation_Accidents_Data_Analysis_Completed.ipynb`

### Key Safety Metrics
- **Serious/Fatal Injury Fraction (`SeriousOrFatal.Rate`)**  
  Estimated as the fraction of passengers seriously or fatally injured per event.
- **Destroyed Fraction (`Was.Destroyed`)**  
  Binary indicator of whether the aircraft was destroyed in the accident.

All comparisons use **grouped statistical summaries (mean, count)** following the **split–apply–combine paradigm**, with minimum sample-size thresholds applied to reduce noise.

---

## Recommendations

### Small Airplanes (≤ 20 passengers)

**Recommended Makes (low injury severity and low destruction rates):**
- GRUMMAN ACFT ENG COR–SCHWEIZER  
- BOEING  
- STINSON  
- AVIAT AIRCRAFT INC  
- MAULE  

**Example Safer Models / Plane Types (≥10 events):**
- MAULE M-5-210C  
- DIAMOND DA 20 C1  
- CESSNA 172SP  
- CESSNA 180J  
- CESSNA A185E  

These makes and models exhibit comparatively low average serious/fatal injury fractions and relatively low rates of aircraft destruction.

---

### Large Airplanes (> 20 passengers)

**Recommended Makes:**
- BOEING  
- MCDONNELL DOUGLAS  
- EMBRAER  
- AIRBUS  

Only a limited number of manufacturers meet stable sample-size thresholds in the large-aircraft subset, but these makes consistently show low average injury severity.

**Example Safer Models / Plane Types (≥10 events):**
- BOEING 777  
- BOEING 757  
- BOEING 787  
- BOEING 737-7H4  
- BOMBARDIER CL-600-2B19  

---

## Factors Affecting Injury and Damage Outcomes

### 1. Weather Condition
Grouped analysis by weather category shows meaningful variation in both injury severity and aircraft destruction rates. Poorer weather conditions are generally associated with higher risk, though results are interpreted alongside sample size and operational context.

### 2. Phase of Flight
Accident severity differs across flight phases. Certain phases (e.g., takeoff/climb and approach/landing) show higher average injury and destruction rates, reflecting reduced margins and increased pilot workload.

---

## Summary
- **Small airplanes:** Several makes and models demonstrate favorable safety profiles, though distributions show occasional high-severity outliers.
- **Large airplanes:** Fewer makes meet stability thresholds, but major transport-category manufacturers perform well on average.
- **Weather conditions and phase of flight** are both strongly associated with injury severity and aircraft destruction outcomes.

This analysis is descriptive and intended to support comparative safety assessment rather than causal inference.

---

## Reproducibility
1. Run `Aviation_Accidents_Cleaning_Completed.ipynb`
2. Run `Aviation_Accidents_Data_Analysis_Completed.ipynb`
3. Review grouped statistics and distributions used to support recommendations
